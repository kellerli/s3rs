**This project is moved to gitlab** [gitlab repo link](https://gitlab.com/yanganto/s3rs)

s3rs 
---
a **S3** **R**ich **S**upport client
- multi config
- AWS4, AWS2 support
- TODO: implent region support (currently use us-east-1)and virtual-hosted-style

current status:  

| function                          | descrrption                                 | CEPH | AWS |
|-----------------------------------|---------------------------------------------|------|-----|
| la                                | list all objects                            | O    | ?   |
| ls                                | list bucket                                 | O    | O   |
| ls [bucket]                       | list objects in the bucket                  | O    | ?   |
| ls s3://[bucket]                  | list objects in the bucket                  | O    | ?   |
| mb [bucket]                       | create bucket                               | O    | ?   |
| rb [bucket]                       | delete bucket                               | O    | ?   |
| put [file] s3://[bucket]/[object] | upload the file sepcific object name        | O    | ?   |
| put [file] s3://[bucket]          | upload the file use file name as objec name | O    | ?   |
| put test s3://[bucket]/[object]   | upload a test file sepcific object name     | O    | ?   |
| get s3://[bucket]/[object] file   | download objec                              | O    | ?   |
| get s3://[bucket]/[object]        | download objec in current folder            | O    | ?   |
| cat s3://[bucket]/[object]        | show the object content                     | O    | ?   |
| del s3://[bucket]/[object]        | delete the object                           | O    | ?   |
| /uri?query                        | give the orignal url                        | O    | ?   |
|-----------------------------------|---------------------------------------------|------|-----|
| s3\_type [ceph/aws/aws4/aws2]     | change the api for different S3 providor    |      |     |
| log [trace/debug/info/erro]       | change the log level                        |      |     |
|                                   | - Debug: for auth signature hash info       |      |     |
|                                   | - Info: for Http header and body            |      |     |

| s3 type           | auth type | format | virtual-hosted–style path-style |
|-------------------|-----------|--------|---------------------------------|
| ceph              | aws4      | json   | path style                      |
| aws/aws4(default) | aws4      | xml    | path style                      |



# Build Environment
Please download and install Rust and Cargo (Rust package manager)
- [Install Rust](https://www.rust-lang.org/en-US/install.html)
- [Install Cargo](https://crates.io/)

Clone the code
`git clone https://github.com/yanganto/s3rs.git`

# Build
- `cargo build --release`
- The excutable binary will in `./target/release/s3rs`

# Install from cargo
`cargo install s3rs`

# Demo
- A short demo [video](https://youtu.be/DnWQbDmBFpg)

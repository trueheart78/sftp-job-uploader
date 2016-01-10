# Job Uploader

Built for Ruby v2.0

## Installation

Please run `gem install bundler`, followed by `bundle install`

### SQLite

OS X: `brew install sqlite`

Ubuntu: `sudo apt-get install sqlite`

## Usage

Call the script passing in a directory to watch, a filetype to watch, and the connection details for the remote server.

```bash
ruby lib/watch.rb /dir/to/watch mp3 user@sftp-locale.com:~/path/
```

## Logs

The database stores logged file transfer details.

```bash
ruby lib/history.rb
```

## Notes

- Built around the idea of connecting to a server over SFTP (SSH)
- Initial setup will utilize key-based access
- Watches a passed dir for files
- Uploads a file that hasn't been changed in 5 minutes
- Uploads a custom XML file once the watched file is complete
- Stores data regarding upload history in a database 

# serverless-ami-generation-backup

Auto AMI Generation Backup using Lambda.
Made with reference to http://pict3.hatenablog.com/entry/2015/12/09/104015

## Usage

Node Version: 4.3.2

1. Install Serverless Framework.

```bash
npm install -g serverless
```

2. Set up aws cli configure used by Serverless Framework.
Reference to https://serverless.com/framework/docs/providers/aws/guide/credentials/

3. Get this project

```bash
$ git clone git@github.com:tutida/serverless-auto-ami-generation-backup.git
$ cd 'project-path'
```

4. Run Serverless Framewrok with option --schefule

```bash
# ex1. daily
serverless deploy --schedule 'cron(0 2 * * ? *)' -v

# ex2. rate
serverless deploy --schedule 'rate(30 minutes)' -v
```

## Memo

Install node.js(v4.3.2) by nodebrew and update npm.

```bash
# get nodebrew
$ curl -L git.io/nodebrew | perl - setup
$ export PATH=$HOME/.nodebrew/current/bin:$PATH
$ source ~/.bashrc

# install node.js(v4.3.2)
$ nodebrew install-binary v4.3.2 --v8-options=--harmony
$ nodebrew use v4.3.2

# npm update
$ npm update -g
```

Install aws cli

```bash
$ sudo yum --enablerepo=epel -y install python-pip
$ sudo pip install awscli
```
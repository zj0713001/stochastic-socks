# Intro

Socks 5 tunnel with a bit crypto / obfuscation.

For every data chunk, a random initial vector is generated, which grants the stochastic behavior.

A delimiter is inserted after the ciphered data chunk, it helps decoding and may be used to perform [poison attack](http://arxiv.org/pdf/1206.6389.pdf) on machine learning routers in the future.

# Install

Requires [Ruby](http://ruby-lang.org) 1.9+ and a OS X / BSD / Linux server

```bash
gem ins zscan
gem ins eventmachine
cp config.yml.example config.yml
# edit config
vi config.yml
```

# Use

On server

```bash
ruby server.rb
```

On local

```bash
ruby local.rb
```

# Test

Prepare gems

```bash
gem ins rspec
gem ins pry
```

Then

```bash
ruby spec.rb
```

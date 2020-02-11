# t-SNE

High performance t-SNE for Ruby, powered by [Multicore t-SNE](https://github.com/DmitryUlyanov/tsne)

## Installation

Add this line to your application’s Gemfile:

```ruby
gem 'tsne'
```

## Getting Started

Prep your data

```ruby
x = Numo::DFloat.cast([[0, 0, 0], [0, 1, 1], [1, 0, 1], [1, 1, 1]])
```

Run

```ruby
tsne = TSNE.new
tsne.fit_transform(x)
```

Get Kullback-Leibler divergence

```ruby
tsne.kl_divergence
```

## Parameters

```ruby
TSNE.new(
  n_components: 2,
  perplexity: 30.0,
  early_exaggeration: 12,
  learning_rate: 200,
  n_iter: 1000,
  n_iter_early_exag: 250,
  verbose: 0,
  random_state: -1,
  angle: 0.5,
  n_jobs: 1,
  cheat_metric: true
)
```

## History

View the [changelog](https://github.com/ankane/tsne/blob/master/CHANGELOG.md)

## Contributing

Everyone is encouraged to help improve this project. Here are a few ways you can help:

- [Report bugs](https://github.com/ankane/tsne/issues)
- Fix bugs and [submit pull requests](https://github.com/ankane/tsne/pulls)
- Write, clarify, or fix documentation
- Suggest or add new features

To get started with development:

```sh
git clone https://github.com/ankane/tsne.git
cd tsne
bundle install
bundle exec rake vendor:all
bundle exec rake test
```
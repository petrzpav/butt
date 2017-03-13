# Bash Unit Testing Tool

[![Build Status](https://travis-ci.org/InternetGuru/butt.svg?branch=master)](https://travis-ci.org/InternetGuru/butt)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> Command line tool to support programmers in testing their commands.

Bash Unit Testing Tool runs and evaluates a set of commands according to expected results. It can serve as CI component of Bash scrip development. It is an alternative to [bats][bats] command with following improvements:

- predefined comparison (assert) functions,
- distinguish standard and error output,
- verbose mode,
- advanced user functions support.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [Donations](#donations)
  - [Donors](#donors)
- [License](#license)

## Install

TODO improve installation
TODO requirements

### Single file script

1. Download latest distribution `omgf.sh` [manually][latest] or use following commands (it requires `jq` and `curl`)

   ```shell
   GF_VERSION="$(curl https://api.github.com/repos/InternetGuru/omgf/releases/latest -s | jq -r .tag_name)"
   curl -OL https://github.com/InternetGuru/omgf/releases/download/$GF_VERSION/omgf.sh
   ```

2. Make file executable

   ```shell
   chmod +x omgf.sh
   ```

### From distribution package

1. Download latest distribution `omgf-[version]-linux.tar.gz` [manually][latest] or use following commands (it requires `jq` and `curl`)

   ```shell
   GF_VERSION="$(curl https://api.github.com/repos/InternetGuru/omgf/releases/latest -s | jq -r .tag_name)"
   curl -OL https://github.com/InternetGuru/omgf/releases/download/$GF_VERSION/omgf-${GF_VERSION:1}-linux.tar.gz
   ```

2. Extract files and install omgf

   ```shell
   tar -xvzf omgf-${GF_VERSION:1}-linux.tar.gz
   pushd omgf-${GF_VERSION:1}-linux
   ./install
   popd
   ```

Tip: Specify installation variables. E.g. `PREFIX="~/.omgf" ./install`

### From source

```shell
git clone https://github.com/InternetGuru/omgf.git
pushd omgf
./configure && make && compiled/install
popd
```

- Make dist package from source

   `./configure && make dist`

- Tip: Specify variables

   E.g. `./configure && PREFIX=/usr SYSTEM=ubuntu make dist`

- Tip: Install rst2man

   `apt-get install python-docutils` or `pip install docutils`

## Usage

> See [man page][man] for more informations and examples.

```shell
# TODO usage
```

## Maintainers

-  Pavel Petržela pavel.petrzela@internetguru.cz
-  Jiří Pavelka jiri.pavelka@internetguru.cz

## Contribute

Pull requests are wellcome, don't hesitate contribute.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## Donation

If you find this program useful, please **send a donation** to its developers to support their work. If you use this program at your workplace, please suggest that the company make a donation. We appreciate contributions of any size. Donations enable us to spend more time working on this package, and help cover our infrastructure expenses.

If you’d like to make a donation of any value, please send it to the following PayPal address:

[PayPal Donation](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=UZHQ28P4VYHWY)

Since we aren’t a tax-exempt organization, we can’t offer you a tax deduction. But for all donations over 50 USD, we’d be happy to recognize your contribution on this README file (including manual page) for the next release.

We are also happy to consider making particular improvements or changes, or giving specific technical assistance, in return for a substantial donation over 100 USD. If you would like to discuss this possibility, write us at info@internetguru.cz.

Another possibility is to pay a software maintenance fee. Again, write us about this at info@internetguru.cz to discuss how much you want to pay and how much maintenance we can offer in return.

Thanks for your support!

### Donors

- [Faculty of Information Technology, CTU Prague](https://www.fit.cvut.cz/en)

## License

GNU Public License version 3, see [LICENSE][license]


[butt]: https://github.com/InternetGuru/butt
[latest]: https://github.com/InternetGuru/butt/releases/latest
[license]: https://raw.githubusercontent.com/InternetGuru/butt/master/LICENSE
[man]: https://github.com/InternetGuru/omgf/blob/master/butt.1.rst
[bats]: https://github.com/sstephenson/bats
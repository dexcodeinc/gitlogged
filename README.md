# Gitlogged

This gem provides git reporting per author grouped by date.

## Installation

Install the latest stable release:

```
$ gem install gitlogged
```

In Rails, add it to your Gemfile:

```
group :development do
  gem 'gitlogged'
end
```

## Getting started

To get the git stats for the day, run:

```
$ gitlogged
```

This will return the following sample output:

```
Armin Primadi (1):
      Fix git summarizer script (by default git --before and --after offset the date by current hour, which is not what we want)

Budi (1):
      disabled setup invoice from document (Invoice Processing - new)

Yunan (3):
      fix edit qr (#4420) & add react attachment on qr
      fix blank row suppliers on qr (#4448)
      fix toggle hide form edit (#4447)
```

You can also specify a date to `gitlogged` which will return the commit stats for that date:

```
$ gitlogged 2016-04-01
```

Or you can also specify a date range to `gitlogged` which will return the commit stats grouped by date:

```
$ gitlogged 2016-04-25 2016-04-26
```

Which return this sample output:

```
################################################################

Date: 2016-04-25

Yunan (4):
      fix attachment form for IE (#4407)
      fix (#4406)
      fix merge & indentation attachment form
      fix (#4394) unexpected after edit wo

gilang (1):
      #4404 fix orders cart


################################################################
################################################################

Date: 2016-04-26

Armin Primadi (2):
      Fix document approval logs controller
      Adding git tool to generate summary on what each devs are doing on a given day for reporting purpose

Budi (1):
      remove validation user for Invoice Processing feature

Yunan (3):
      fix attachment in edit mode (#4405) && (#4430)
      fix label attachment on IE (#4407)
      fix void method (#4427)

gilang (2):
      Fix show products list in discussion summary
      #4437 define CApproved_NR status id in order


################################################################
```

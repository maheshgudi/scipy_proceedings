# SciPy Proceedings

## Instructions for Reviewers

- Click on the Pull Requests Tab and browse to find the papers assigned to you
- After reading the paper, you can start the review conversation by simply commenting
  on the paper, taking into consideration
  [this set of suggested review criteria](https://github.com/scipy-conference/scipy_proceedings/blob/master/review_criteria.md).
- Please submit a comprehensive review by **June 21st.**
- Authors will then respond to the comments and/or modify the paper to address the comments. 
- This will begin an iterative review process where authors and reviewers can discuss the
  evolving submission.
- Reviewers may also apply one of the labels 'needs-more-review', 'pending-comment', or 
  'unready' to flag the current state of the review process.
- Only once a reviewer is satisfied that the review process is complete and the submission should
  be accepted to the proceedings, should they affix the 'ready' label. 
- Reviewers should come to a final 'ready', 'unready' decision before **July 7th** at 18:00 PST.

## Instructions for Authors

Submissions must be received by **June 6th** at 23:59 PST, but modifications are
allowed during the open review period which ends July 8th at 18:00 PST.  Submissions are
considered received once a Pull Request has been opened following the procedure
outlines below.

Papers are formatted using reStructuredText and the compiled version should be
no longer than 8 pages, including figures.  Here are the steps to produce a
paper:

- Fork the
  [scipy_proceedings](https://github.com/scipy-conference/scipy_proceedings)
  repository on GitHub.

- Check out the 2017 branch (``git checkout 2017``).

- Create a new environment (using your choice of environment manager, e.g., ``pyenv`` or ``conda``).

- Install/update the required python libraries (``pip install -U -r requirements.txt``).

- An example paper is provided in ``papers/00_vanderwalt``.  Create a new
  directory ``papers/firstname_surname``, copy the example paper into it, and
  modify to your liking.

- Run ``./make_paper.sh papers/firstname_surname`` to compile your paper to
  PDF (requires LaTeX, docutils, Python--see below).  The output appears in
  ``output/firstname_surname/paper.pdf``.

- Once you are ready to submit your paper, file a pull request on GitHub.
  **Please ensure that you file against the correct branch**--your branch
  should be named 2017, and the pull-request should be against our 2017
  branch.

- Please do not modify any files outside of your paper directory.

## Schedule Summary

Authors may make changes to their submisions throughout the review process.

There are many different styles of review (some do paragraph comments, others
do 'code review' style line edits) and the process is open.

We encourage authors and reviewers to work together iteratively to make each 
others papers the best they can be.
Combine the best principles of open source development and academic publication.

These dates are the tentative timeline for 2017:

- May 4th - Authors invited to submit full papers
- June 6th - Initial submissions due
- June 7th - Reviewers assigned
- June 21st - Reviews due
- June 21st -July 7th: Authors revise papers based on reviews
- July 7th - Acceptance/rejection of papers
- July 8th - Papers must be camera-ready
- July 10-16th - Conference
- July 20th - Publication

## General Guidelines

- All figures and tables should have captions.
- Figures and tables should be positioned inline, close to their explanatory text.
- License conditions on images and figures must be respected (Creative Commons,
  etc.).
- Code snippets should be formatted to fit inside a single column without
  overflow.
- Avoid custom LaTeX markup where possible.

## Review Criteria

A small subcommittee of the SciPy 2017 organizing committee has created [this
set of suggested review
criteria](https://github.com/scipy-conference/scipy_proceedings/blob/master/review_criteria.md)
to help guide authors and reviewers alike. Suggestions and amendments to these
review criteria are enthusiastically welcomed via discussion or pull request.

## Other markup

Please refer to the example paper in ``papers/00_vanderwalt`` for
examples of how to:

 - Label figures, equations and tables
 - Use math markup
 - Include code snippets

## Requirements

 - Install the requirements in the requirements.txt file: `pip install -r requirements.txt`
 - IEEETran (often packaged as ``texlive-publishers``, or download from
   [CTAN](http://www.ctan.org/tex-archive/macros/latex/contrib/IEEEtran/)) LaTeX
   class
 - AMSmath LaTeX classes (included in most LaTeX distributions)
 - alphaurl (often packaged as ``texlive-bibtex-extra``, or download from
   [CTAN](https://www.ctan.org/pkg/urlbst)) urlbst BibTeX style

### Debian-like distributions:

```
sudo apt-get install python-docutils texlive-latex-base texlive-publishers \
                     texlive-latex-extra texlive-fonts-recommended \
                     texlive-bibtex-extra
```

Note you will still need to install `docutils` with `pip` even on a Debian system.

### Fedora

On Fedora, the package names are slightly different:

```
su -c `dnf install python-docutils texlive-collection-basic texlive-collection-fontsrecommended texlive-collection-latex texlive-collection-latexrecommended texlive-collection-latexextra texlive-collection-publishers texlive-collection-bibtexextra`
```

## Build Server

There will be a server online building the open pull requests 
[here](http://zibi.bids.berkeley.edu:7001). You should be able to pull a built PDF 
for review from there.

TODO: update server link

## For organizers

To build the whole proceedings, see the Makefile in the publisher directory.

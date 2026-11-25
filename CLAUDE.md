# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project status

Early-stage repository: so far it holds only `README.md` and `.gitignore`. There is no source code, dependency manifest, build system, or test suite yet. Update this file once those exist (commands for env setup, running the simulation, and running a single test).

## Purpose

xzsim is a web app for 2D reservoir flow simulation on a vertical XZ cross-section (in the spirit of Petrel/INTERSECT). Core domain concepts: wells, zones, rock types, and relative permeabilities. Project docs and commit messages are written in Spanish.

## Conventions implied by `.gitignore`

- **Language/tooling:** Python, with virtual environments in `.venv/` or `venv/`, and Jupyter notebooks expected (`.ipynb_checkpoints/` is ignored). Secrets go in `.env`.
- **Data lives outside the repo.** Large datasets are kept on a NAS, not in git: `data/` and all `*.las` (well logs), `*.segy`/`*.sgy` (seismic), `*.csv` and `*.xlsx` files are ignored. Don't commit data files or add sample data in these formats; code should read them from a configurable external path.
- Development happens on Windows.

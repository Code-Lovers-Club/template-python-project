.DEFAULT_GOAL := help

.PHONY: help
help:
	@awk 'BEGIN {FS = ":.*?## "} /^[a-zA-Z_-]+:.*?## / {printf "\033[36m%-20s\033[0m %s\n", $$1, $$2}' $(MAKEFILE_LIST)

# General
.PHONY: init
init: ## Initialize your python project
	@git init -b main \
	&& pip install -U pip poetry poetry-plugin-up pre-commit\
	&& poetry install --no-root \
	&& pre-commit install \
	&& curl https://raw.githubusercontent.com/Code-Lovers-Club/branch-color/main/install.sh --output /tmp/install-branch-color.sh
	/bin/bash /tmp/install-branch-color.sh
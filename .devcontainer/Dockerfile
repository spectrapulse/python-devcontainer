ARG VARIANT="3.10-bullseye"
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${VARIANT}

ARG USERNAME=vscode

# Ensure gpnupg2 is installed for signing commits
RUN apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y --no-install-recommends gnupg2

# Install poetry and nox
COPY requirements.txt /tmp/pip-tpm/requirements.txt
RUN pip3 --disable-pip-version-check --no-cache-dir install -r /tmp/pip-tpm/requirements.txt \
    && rm -rf /tmp/pip-tmp

# Add configuration for poetry
RUN mkdir -p /home/${USERNAME}/.config/pypoetry \
    && chown ${USERNAME}:${USERNAME} /home/${USERNAME}/.config -R
COPY --chown=${USERNAME}:${USERNAME} poetry_config.toml /home/${USERNAME}/.config/pypoetry/config.toml

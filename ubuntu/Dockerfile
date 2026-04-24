FROM ubuntu:24.04

RUN apt-get update

# Create a general purpose account
# --inactive will expire the password after specified days of inactivity

RUN groupadd --gid 1001 gp_group && \
    useradd --comment "General Purpose account" \
            --create-home \
            --inactive 1 \
            #--password "$GP_USER_PASSWORD" \\
            --shell /bin/bash \
            --gid 1001 \
            --uid 1001 \
            gp_user

USER gp_user

WORKDIR /home/gp_user

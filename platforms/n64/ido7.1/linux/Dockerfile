# NOTE: This file is generated automatically via template.py. Do not edit manually!


FROM alpine:3.18 AS base

RUN mkdir -p /compilers/n64/ido7.1

RUN wget -O ido-7.1-recomp-linux.tar.gz "https://github.com/decompals/ido-static-recomp/releases/download/v1.2/ido-7.1-recomp-linux.tar.gz"
RUN tar xvzf ido-7.1-recomp-linux.tar.gz -C /compilers/n64/ido7.1
RUN wget -O /compilers/n64/ido7.1/cc-irix4 "https://gist.githubusercontent.com/jtl3d/a3d54c4d2eadfedc7d4287e489dba902/raw/8dafb02ff809734d95c23dab00cb9fcf58c974d8/cc-irix4"
RUN wget -O /compilers/n64/ido7.1/OCC-irix4 "https://gist.githubusercontent.com/jtl3d/6048d3165ca1c54456edb7ffd6e1a5b9/raw/737cbea0d39762c891a25215ac59270aa65dc78e/OCC-irix4"

RUN chown -R root:root /compilers/n64/ido7.1/
RUN chmod +x /compilers/n64/ido7.1/*


FROM scratch AS release

COPY --from=base /compilers /compilers

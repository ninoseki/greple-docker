FROM perl:5.28

RUN cpanm App::Greple && cpanm App::Greple::msdoc

ENTRYPOINT ["greple"]

CMD ["--usage"]

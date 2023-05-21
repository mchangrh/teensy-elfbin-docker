# nasm builder
FROM alpine:latest as builder
RUN wget http://timelessname.com/elfbin/helloworld.tar.gz && tar -xvf helloworld.tar.gz
RUN chmod +x hello
FROM scratch
COPY --from=builder hello hello
CMD ["/hello"]
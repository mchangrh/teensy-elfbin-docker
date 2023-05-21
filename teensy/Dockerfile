# nasm builder
FROM alpine:latest as builder
RUN apk add --no-cache nasm
COPY tiny.asm tiny.asm
RUN nasm -f bin -o teensy tiny.asm
RUN chmod +x teensy
RUN wc -c teensy
FROM scratch
COPY --from=builder teensy teensy
CMD ["/teensy"]
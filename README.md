# crons

Agendador dos crons dos apps da K.

## Por que este repositório é PÚBLICO de propósito

O GitHub cobra minutos de Actions **apenas em repositório privado**.
Em repositório público os minutos são **ilimitados e grátis**.

Os crons já pararam duas vezes por cota estourada (jul/2026 e ago/2026),
e nas duas vezes a sincronização morreu em silêncio. Este repo existe
para que isso não possa acontecer de novo.

## Regras (não violar)

1. **Nunca colocar código ou dado aqui.** Só arquivos de agendamento.
2. **Nunca imprimir o corpo da resposta** de uma chamada. O log deste
   repositório é visível para qualquer pessoa na internet. Só o código
   HTTP (`200`, `500`) pode aparecer.
3. Os segredos ficam em **GitHub Secrets** — continuam protegidos mesmo
   com o repositório público, e o GitHub os mascara no log.
4. Todo trabalho de verdade acontece na Vercel, do outro lado do `curl`.

## O que roda aqui

| Workflow | App | Frequência |
|---|---|---|
| `drak-djen.yml` | DraK | 5x/dia (06,09,12,15,18 BRT) |
| `maildash-kiwify.yml` | MailDash | a cada 3h |
| `maildash-resend.yml` | MailDash | a cada 4h |
| `maildash-digistore.yml` | MailDash | a cada 3h |

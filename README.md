# p2p-transfer

P2P-передача файлов между двумя машинами через relay на Go (в духе magic-wormhole).

## Возможности (план)

- relay-сервер с WebSocket;
- комната с коротким кодом для соединения;
- сквозное шифрование (XChaCha20-Poly1305);
- передача больших файлов чанками;
- прогресс-бар;
- докачка/возобновление при обрыве.

## Стек

- Язык: Go
- Планируемые библиотеки: `gorilla/websocket`, `golang.org/x/crypto`

## Сборка и запуск

```bash
go build -o bin/p2p-transfer .
./bin/p2p-transfer send ./file.zip   # выдаст код комнаты
./bin/p2p-transfer recv XXXX-XXXX
```

## Лицензия

MIT

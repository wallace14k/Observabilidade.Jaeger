para testar o Jeager basta apenas subir a seguinte imagem


version: '3.7'

services:
  jaeger:
    image: jaegertracing/all-in-one
    ports:
      - "5775:5775/udp"
      - "6831:6831/udp"
      - "6832:6832/udp"
      - "5778:5778"
      - "16686:16686"   # UI do Jaeger
      - "14268:14268"   # Enviar spans do Jaeger
      - "14250:14250"   # Coletor do Jaeger
      - "9411:9411"     # Compatibilidade com Zipkin

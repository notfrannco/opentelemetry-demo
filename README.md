# Elastic Stack on Docker
## Elastic Agent, Fleet, and Elastic APM


![arquitecturadelelasticstack](https://github.com/notfrannco/opentelemetry-demo/assets/19764680/eec88277-96dc-4727-9cb3-8ec975f85e9e)
#### Overview de la arquitectura general
<br />**Setup Certificate**: Configura los certificados autofirmados que se utilizaran para la comunicacio tls entre los distintos componentes del stack.
<br />**Elasticsearch**: Levanta un servidor elasticsearch a ser utilizado para la demo.
<br />**Setup Certificate**: Levanta un servidor kibana para la visualizacion de los distintos dashboard que se analizaran en la demo.
<br />**Metricbeat y Filebeat**: Levanta los dos beat para prueba de integracion "legacy", es recomendado utilizar Fleet en las versiones de elasticstack 8+
<br />**Logstash**: Servidor de logstash que se utilizaran a futuro para filtro especifico de datos.
<br />**Fleet Server**: Nueva forma de administrar los agentes de elastic stack
<br />**Web APP**: Web demo para demostracion de la APM (http://192.168.100.71:8000/).
<br />**OBS**: Este docker compose esta basada en un blog oficial hecho por la comunidad de elastic stack, realice varios cambios para ajustar a mis necesidades especficas para la demo
<br />**Blog 1**: https://www.elastic.co/blog/getting-started-with-the-elastic-stack-and-docker-compose
<br />**Blog 2**: https://www.elastic.co/blog/getting-started-with-the-elastic-stack-and-docker-compose-part-2
 
# Opentelemtery-demo 
demo oficial de la coumindad de Opentelemtry, modifique la version de docker-compose, para mas detalle del codigo de los microservicios visitar la doc oficial
<br />**code**: https://github.com/javaducky/opentelemetry-demo/tree/main 
<br /> **doc of docker-compose version**: https://opentelemetry.io/docs/demo/docker-deployment/

## Opentelemtery URls
| Funcion | URL |
| ------ | ------ |
|   **Web STore**     |   http://192.168.100.71:8080/      |
|     **Grafana**   |  http://192.168.100.71:8080/grafana/       |
|  **Load Generator UI** |     http://192.168.100.71:8080/loadgen/        |
|   **Jaeger UI**     |   http://192.168.100.71:8080/jaeger/ui/      |


## Que es Opentelemetry?
<br /> Opentelementry es un projecto opensource mantenida por la [CNCF](https://www.cncf.io/projects/), y su objetivo es estandarizar el el shipping the telementry data ([traces](https://opentelemetry.io/docs/concepts/signals/traces/), [metrics](https://opentelemetry.io/docs/concepts/signals/metrics/), [logs](https://opentelemetry.io/docs/concepts/signals/logs/))

## Como funciona Opentelemetry?
<br /> Opentelemetry provee una collecion de [APIs, SDKs](https://opentelemetry.io/docs/languages/), para estandarizar la ingesta, transformacion y envio de datos a un backend de nuestra preferencia

<br /><br /><br />**Diagrama de Arquitectura 1**:
![opentelemetrystack](https://github.com/notfrannco/opentelemetry-demo/assets/19764680/5f28ff9c-283f-43c7-9050-25f16087f49f)


<br /><br /><br />**Diagrama de Arquitectura 2**: [source](https://www.aspecto.io/blog/opentelemetry-collector-guide/)
![opentelemetryarchitecture](https://github.com/notfrannco/opentelemetry-demo/assets/19764680/3b8021ba-cc69-4bfc-9df6-2aa6fa67a356)


<br /><br /><br />**Diagrama de Arquitectura 3 (Implementacion con Elastic Stack)**: [source](https://www.elastic.co/blog/native-opentelemetry-support-in-elastic-observability)
![exampleintegrationwithelastic](https://github.com/notfrannco/opentelemetry-demo/assets/19764680/cace1c2a-2aa5-4627-bc25-1471c7d76e05)


## Opentelemetry Observaciones
<br />**Pros**:
- Vendor Netural
- Rapida adopcion por la comunidad, en [2023](https://www.cncf.io/blog/2023/10/27/october-2023-where-we-are-with-velocity-of-cncf-lf-and-top-30-open-source-projects/) se posiciono como el 2 proyecto mas activo de la [CNCF](https://www.cncf.io/) solo detras de kubernetes

<br />**Cons**:
- El proyecto es relativamente nuevo (2019) por ende no hay documentacion extensa disponible
- Complejidad de adopcion alta
  -  Nuevos terminos y conceptos que se necesitan aprender y profundizar.
  -  compllejo y tedioso para los que lo implementan (la parte de desarrollo, SDK), sencillo para los que los consumen (monitoring tools integration, la parte "DevOps")



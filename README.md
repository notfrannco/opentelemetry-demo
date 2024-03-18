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


## Demos featuring the Astronomy Shop

We welcome any vendor to fork the project to demonstrate their services and
adding a link below. The community is committed to maintaining the project and
keeping it up to date for you.

|                                                                                                                   |                                                                   |                                                                                              |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [AlibabaCloud LogService](https://github.com/aliyun-sls/opentelemetry-demo)                                       | [Grafana Labs](https://github.com/grafana/opentelemetry-demo)     | [New Relic](https://github.com/newrelic/opentelemetry-demo)                                  |
| [AppDynamics](https://www.appdynamics.com/blog/cloud/how-to-observe-opentelemetry-demo-app-in-appdynamics-cloud/) | [Helios](https://otelsandbox.gethelios.dev)                       | [Sentry](https://github.com/getsentry/opentelemetry-demo)                                    |
| [Aspecto](https://github.com/aspecto-io/opentelemetry-demo)                                                       | [Honeycomb.io](https://github.com/honeycombio/opentelemetry-demo) | [Splunk](https://github.com/signalfx/opentelemetry-demo)                                     |
| [Coralogix](https://coralogix.com/blog/configure-otel-demo-send-telemetry-data-coralogix)                         | [Instana](https://github.com/instana/opentelemetry-demo)          | [Sumo Logic](https://www.sumologic.com/blog/common-opentelemetry-demo-application/)          |
| [Datadog](https://github.com/DataDog/opentelemetry-demo)                                                          | [Kloudfuse](https://github.com/kloudfuse/opentelemetry-demo)      | [TelemetryHub](https://github.com/TelemetryHub/opentelemetry-demo/tree/telemetryhub-backend) |
| [Dynatrace](https://www.dynatrace.com/news/blog/opentelemetry-demo-application-with-dynatrace/)                   | [Lightstep](https://github.com/lightstep/opentelemetry-demo)      | [Uptrace](https://github.com/uptrace/uptrace/tree/master/example/opentelemetry-demo)         |
| [Elastic](https://github.com/elastic/opentelemetry-demo)                                                          |                                                                   |                                                                                              |
|                                                                                                                   |                                                                   |                                                                                              |





|                                                                                                                   |                                                                   |                                                                                              |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| [Wes Store](http://192.168.100.71:8080/)                                       |                                
| [Grafana](http://192.168.100.71:8080/grafana/) |                            
| [Load Generator UI](http://192.168.100.71:8080/loadgen/)                                                       |
| [Jaeger UI](http://192.168.100.71:8080/jaeger/ui/)                         | 





## Contributing

To get involved with the project see our [CONTRIBUTING](CONTRIBUTING.md)
documentation. Our [SIG Calls](CONTRIBUTING.md#join-a-sig-call) are Mondays at
8:15 AM PST and anyone is welcome.

## Project leadership

[Maintainers](https://github.com/open-telemetry/community/blob/main/community-membership.md#maintainer)
([@open-telemetry/demo-maintainers](https://github.com/orgs/open-telemetry/teams/demo-maintainers)):

- [Austin Parker](https://github.com/austinlparker), Lightstep
- [Carter Socha](https://github.com/cartersocha), Lightstep
- [Juliano Costa](https://github.com/julianocosta89), Dynatrace
- [Pierre Tessier](https://github.com/puckpuck), Honeycomb

[Approvers](https://github.com/open-telemetry/community/blob/main/community-membership.md#approver)
([@open-telemetry/demo-approvers](https://github.com/orgs/open-telemetry/teams/demo-approvers)):

- [Mikko Viitanen](https://github.com/mviitane), Dynatrace
- [Penghan Wang](https://github.com/wph95), AppDynamics
- [Reiley Yang](https://github.com/reyang), Microsoft
- [Ziqi Zhao](https://github.com/fatsheep9146), Alibaba

Emeritus:

- [Michael Maxwell](https://github.com/mic-max)
- [Morgan McLean](https://github.com/mtwo)

### Thanks to all the people who have contributed

[![contributors](https://contributors-img.web.app/image?repo=open-telemetry/opentelemetry-demo)](https://github.com/open-telemetry/opentelemetry-demo/graphs/contributors)

[docs]: https://opentelemetry.io/docs/demo/
# opentelemetry-demo

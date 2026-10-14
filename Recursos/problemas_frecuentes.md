# FAQ de problemas frecuentes
## 1. Mi nodo no aparece

Puede no aparecer en la aplicación, en la red RF o en un mapa de la comunidad. Primero distinguí dónde falta.

### Si no aparece en la aplicación

- Verificá que el celular esté conectado al nodo correcto.
- Probá Bluetooth, Wi‑Fi, USB o la interfaz web.
- Reiniciá el nodo y la aplicación.
- Revisá si el nodo quedó en otro modo de conexión.
- Desactivá temporalmente el ahorro de energía.
- Desactivá y reactivá el Bluetooth.

### Si no aparece en la red

- Confirmá región, frecuencia, canal y PSK.
- Verificá la antena, el pigtail y el cable.
- Revisá que el nodo tenga el canal primario de la zona.
- Acercate con el nodo a una zona donde sepas que hay cobertura de la malla.
- Consultá los mapas comunitarios para identificar zonas o nodos activos.
- Probá enviar un mensaje desde esa zona de cobertura.
- Tené paciencia: la información propia del nodo no siempre se transmite inmediatamente. Según la cobertura y el tráfico, puede tardar bastante tiempo, incluso horas.

En CABA y AMBA, para una prueba básica, suele utilizarse MediumFast. Otras zonas pueden usar configuraciones diferentes.

### Si no aparece en un mapa comunitario

Eso no significa necesariamente que esté fallando. Los mapas pueden depender de acceso y alcance de la malla, GPS, ubicación fija, MQTT y servidores específicos. Un nodo puede funcionar correctamente por RF y no aparecer en ningún mapa.

Además, la información del nodo —posición, telemetría, nombre y otros datos— puede tardar en propagarse. Que no aparezca inmediatamente no significa que la configuración esté mal.

---

## 2. Mi mensaje no llega

Las causas más comunes son:

- Falta de cobertura.
- Antena incorrecta, floja o dañada.
- Región o frecuencia diferentes.
- Canal o PSK distintos.
- Nodo receptor apagado o dormido.
- Exceso de distancia.
- Pocos nodos intermedios.

### Prueba recomendada si tenés un solo nodo

1. Acercate a una zona con cobertura conocida.
2. Consultá los mapas o preguntá en el grupo qué nodos suelen estar activos allí.
3. Verificá región, frecuencia, canal y PSK.
4. Enviá un mensaje corto desde esa ubicación.
5. Observá si aparecen nodos o confirmaciones de recepción.
6. Esperá un tiempo prudente: algunas informaciones propias del nodo pueden tardar en transmitirse o aparecer.

Si el nodo funciona en una zona con cobertura pero no desde tu casa, probablemente el problema sea de alcance, altura, antena o ubicación.

---

## 3. Funcionaba y dejó de funcionar

Revisá qué cambió desde la última vez que funcionó:

- Firmware.
- Canal o región.
- Antena.
- Alimentación.
- Batería.
- Ubicación.
- Ahorro de energía.
- Aplicación o modo de conexión.

Probá reiniciar el nodo, la aplicación y, si corresponde, la base de datos de nodos. Si el problema comenzó después de actualizar, compará con otra versión estable.

---

## 4. No puedo conectar el nodo al celular

Probá lo siguiente:

- Cerrá y volvé a abrir la aplicación.
- Reiniciá el nodo.
- Desactivá y volvé a activar el Bluetooth o Wi‑Fi.
- Acercá el celular.
- Confirmá que el nodo no esté conectado a otro teléfono.
- Verificá si está configurado en modo Bluetooth o Wi‑Fi.
- Probá la interfaz web o USB.
- Revisá si el ahorro de energía está desconectando el nodo.

---

## 5. ¿El problema es la antena?

Es una de las primeras cosas que conviene revisar.

Comprobá:

- Frecuencia correcta para la región.
- Antena firmemente conectada.
- Pigtail y conectores.
- Cable sin cortes.
- Posición vertical.
- Distancia respecto de objetos metálicos.
- Ubicación y altura.

Si podés, probá otra antena o compará el nodo desde una zona con cobertura conocida.

---

## 6. El nodo aparece, pero no transmite o no retransmite

Revisá:

- Rol configurado.
- Canal primario.
- Cantidad de hops (7 hops es lo que solemos utilizar).
- Antena.
- Cobertura.
- Ahorro de energía.
- Saturación de la red.

Para una prueba inicial, llevá el nodo a una zona donde haya cobertura conocida y enviá mensajes cortos. Primero confirmá que el nodo puede escuchar o transmitir por RF antes de modificar configuraciones más avanzadas.

Recordá que la información propia del nodo no necesariamente aparece de inmediato: los datos de posición, telemetría o estado pueden tardar en propagarse, a veces durante horas.

---

## 7. ¿Qué lugar ocupa MQTT?

En la comunidad, MQTT se reserva para casos puntuales o necesidades personales. Como regla general, se recomienda mantenerlo apagado para evitar tráfico innecesario por Internet que termine ocupando tiempo de aire en la red RF.

Si usás MQTT intencionalmente, revisá:

- Servidor o broker.
- Usuario y contraseña.
- Topic.
- Uplink y downlink.
- Ignore MQTT.
- Filtros de tráfico.

Si un problema parece relacionado con MQTT, compará el comportamiento con MQTT apagado y verificá primero que la configuración básica por RF funcione. No actives MQTT solamente para intentar que el nodo aparezca en un mapa.

---

## 8. El GPS o la ubicación no aparecen

Verificá:

- Que el equipo tenga GPS o que esté habilitado el uso de la ubicación del teléfono.
- Que el GPS tenga vista despejada del cielo.
- Que haya pasado suficiente tiempo para obtener señal.
- Que la posición fija esté correctamente configurada, si corresponde.
- Que desde la aplicación del teléfono esté habilitado compartir la ubicación.
- Que en la configuración del canal esté habilitado el uso de ubicación.
- Que hayas seleccionado el rango o alcance de difusión de la ubicación para ese canal.
- Que la privacidad no limite la publicación.

La ubicación y otros datos propios del nodo pueden tardar bastante en transmitirse y aparecer, incluso horas según la cobertura y el tráfico de la red.

Una ubicación que no aparece en un mapa no prueba que el GPS esté roto: puede tratarse de permisos del teléfono, rango de difusión, filtros, demoras o de que el nodo no publica por MQTT.

---

## 9. El nodo se reinicia, se desconecta o pierde autonomía

Revisá:

- Batería y nivel de carga.
- Cableado y conectores.
- Consumo real.
- Panel solar y controlador.
- Ahorro de energía.
- GPS y pantalla.
- Temperatura.
- Calidad de la batería.

Probá el nodo con una fuente o batería confiable y compará su comportamiento con el sistema solar desconectado.

---

## 10. La configuración quedó confusa o nada coincide

Cuando se hicieron muchos cambios, puede ser difícil saber qué está fallando.

Antes de borrar todo:

1. Guardá capturas de la configuración.
2. Anotá modelo y versión de firmware.
3. Probá una configuración mínima.
4. Llevá el nodo a una zona con cobertura conocida.
5. Usá el canal local.
6. Mantené MQTT apagado salvo que tengas un motivo específico para usarlo.
7. Cambiá un solo parámetro por vez.
8. Esperá el tiempo suficiente para que la información propia del nodo se propague.

Como último recurso, hacé un borrado completo, reinstalá el firmware y configurá el nodo desde cero.

---

## Qué información pasar cuando pedís ayuda

Indicá:

- Modelo exacto.
- Región y frecuencia.
- Canal y PSK.
- Rol.
- Tipo de antena.
- Ubicación y altura.
- Forma de conexión al nodo.
- Qué esperabas que ocurriera.
- Qué ocurre realmente.
- Desde qué zona hiciste la prueba.
- Cuánto tiempo esperaste.
- Qué pruebas ya realizaste.

Una buena descripción sería:

> “Tengo un nodo Heltec v3 configurado en MediumFast, MQTT apagado y antena externa. Desde mi casa no veo nodos ni recibo mensajes.”
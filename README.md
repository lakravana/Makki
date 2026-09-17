# MAKKI — Constructor de guion narrativo (método McKee)

MAKKI es una aplicación web que acompaña a un guionista desde una idea suelta hasta un guion
con formato de industria, siguiendo el método de Robert McKee (*Story*): un protagonista se
define por sus contradicciones bajo presión, una historia se estructura en escenas que cambian
de valor, y el subtexto —lo que no se dice— vale más que el diálogo que lo dice todo.

La app traduce eso en **5 módulos secuenciales**. Cada uno se apoya en el anterior, todos
escriben sobre un único documento —la **Biblia de Datos**— y el paso siguiente no se abre hasta
que el anterior se sostiene, no solo hasta que está relleno. Para verlo en marcha, aquí abajo
recorremos los 5 módulos con un proyecto real y completo que trae la propia app: **El turno de
noche**, un cortometraje de 40 minutos.

> *Una enfermera de urgencias descubre que el compañero que le salvó la carrera está robando
> morfina, y tiene que elegir entre denunciarlo o seguir debiéndole todo.*

---

## Módulo 1 — Cimientos: el vértice y la idea controladora

Todo guion empieza eligiendo **qué clase de historia** se va a contar. MAKKI representa esto
como un triángulo con tres vértices —Arquitrama, Minitrama, Antitrama— y un pin que se arrastra
dentro: la posición fija los tres porcentajes (siempre suman 100) y enciende un conjunto de
reglas que van a condicionar los módulos siguientes.

*El turno de noche* se fijó en **62 % Arquitrama / 30 % Minitrama / 8 % Antitrama**: una historia
de causa-efecto clásica, con un protagonista activo y un final cerrado.

Después, un asistente de tres pasos construye la **idea controladora** — la tesis moral que la
historia entera demuestra. Se elige un valor humano (aquí, **Lealtad**) y su cadena de
negatividad:

```
Lealtad → Deslealtad → Traición → Traición vivida y contada como lealtad
```

...y de ahí sale la frase que cierra el módulo:

> **Idea controladora:** *"La traición se disfraza de lealtad cuando alguien confunde deber un
> favor con deberlo todo."*

Esta frase no es decorativa: los módulos 2 a 5 tienen que demostrarla, y la app lo comprueba.

---

## Módulo 2 — Sistema Solar Dramático: protagonista y antagonismo

Aquí se construye al protagonista, no con una lista de rasgos, sino con **pares polares de
conducta bajo presión**: cómo actúa hacia fuera frente a lo que resiste por dentro. Ada, la
protagonista, tiene dos:

| Polo A (conducta visible) | Polo B (resistencia oculta) |
|---|---|
| Firme delante de un paciente que se muere | Incapaz de negarle nada a quien la avaló |
| Escrupulosa con todo lo que firma | Mentirosa con su hermana para que no se preocupe |

El resto del reparto no se añade suelto: cada personaje nace como un "asteroide errante" y hay
que **enganchar un vector** desde él hasta uno de esos polos, explicando qué actitud usa y qué
fricción concreta genera. Así entra **Vidal**, el mentor:

> Vinculado al polo B de Ada ("incapaz de negarle nada a quien la avaló"), actitud *tienta*:
> *"Le recuerda quién firmó su informe cuando iba a perder la plaza, y cobra cada vez que lo
> hace."*

Si dos secundarios tiran del mismo polo con la misma actitud, la app lo marca como **colisión de
frecuencia** y obliga a fusionarlos o diferenciarlos — no deja avanzar con dos personajes que
cumplen exactamente la misma función.

---

## Módulo 3 — Macroestructura: de la chispa a los tres actos

El incidente incitador es el suceso que rompe el equilibrio inicial. La app pide el *status quo*,
el suceso, y los dos deseos —consciente e inconsciente— del protagonista:

> **Suceso:** El recuento de farmacia no cuadra y su firma es la única que hay debajo.
> **Deseo consciente:** dejar su nombre fuera del expediente.
> **Deseo subconsciente:** dejar de deberle nada a Vidal.

De ahí la app genera sola la **Pregunta Dramática Mayor** —*"¿Conseguirá Ada dejar su nombre
fuera del expediente?"*— usando la plantilla del módulo 1. A partir de aquí, un secuenciador de
tres pistas reparte las secuencias por acto sobre una curva de tensión que **tiene que subir**:
si tres secuencias seguidas no escalan el riesgo, salta una alerta de progresión plana.

| Secuencia | Acto | Riesgo | Qué prueba antes y por qué ya no sirve |
|---|---|---|---|
| La firma que no leyó | I | 1 | — (es la primera) |
| Preguntar de frente | II | 3 | El recuento ya está firmado: hacer como si nada la deja dentro |
| El cerco administrativo | II | 5 | Él no va a contestar: cada pregunta es otra deuda |
| Buscar la prueba | II | 7 | La inspección se ha llevado el parte: esperar ya cuesta la plaza |
| Darle una salida | III | 8 | Ya tiene la prueba: seguir buscando solo retrasa la decisión |
| La declaración | III | 10 | Él ha pedido tiempo en vez de devolverlo: no hay salida limpia |

El desenlace cierra con una **Crisis** (elegir entre dos males, no entre bueno y malo), un
**Clímax** irreversible y una **Resolución** — en este caso, Ada firma que el error fue suyo,
delante de Vidal.

---

## Módulo 4 — Micro-gestor de escenas: escena por escena

Cada escena de las 12 que tiene el corto pasa por el mismo embudo de 5 pasos: **fuerzas en
choque → valor de entrada → beats → valor de salida → el abismo**. La primera escena, *"El
cambio de turno"*:

- **Fuerzas excluyentes:** Ada quiere *terminar el turno sin firmar nada más*; la fuerza
  antagónica es *conseguir su firma en el recuento de farmacia*. Solo una puede ganar.
- **Beats**, con su subtexto marcado aparte —lo que el beat *hace* sin decirlo:
  1. Ada ficha con dos minutos de retraso → *disculpándose sin decir nada*
  2. Vidal le acerca el parte con un bolígrafo encima → *poniendo el camino fácil*
  3. Ada firma sin bajar la vista → *devolviendo un favor viejo*
- **Valor de entrada:** Lealtad (+) → **valor de salida:** Lealtad (−). La escena cambia de
  carga (ΔV = 1); si entrara y saliera igual, la app la bloquearía por "no-acontecimiento".
- **El abismo:** esperaba que el recuento fuera el de siempre; la realidad es que faltan cuatro
  ampollas y su firma ya está debajo.

Un medidor de **ratio de subtexto** exige que al menos el 60 % de los beats digan una cosa
mientras pasa otra — por debajo de eso, la escena se bloquea: el diálogo estaría explicando lo
que ya se ve.

---

## Módulo 5 — Formato y exportación: los 4 gates

El último módulo no deja saltar directamente a escribir el guion final. Hay **cuatro
candados en cadena**, y cada uno exige que el anterior esté cerrado:

1. **Step outline** — una tarjeta por escena, prosa sin diálogo, máximo dos frases:
   *"Ada firma el recuento de farmacia sin leerlo porque se lo pide Vidal."*
2. **Tratamiento** — la misma historia en prosa de presente, momento a momento, con el subtexto
   tácito obligatorio.
3. **Escenas maestras** — formato real de guion (slug lines, acción sin términos de cámara
   obsoletos, diálogo con parentéticos), con un monitor que avisa si cinco escenas seguidas
   miden lo mismo en página.
4. **Linter de subtexto** — cuatro comprobaciones automáticas (diálogo "en la nariz", exposición
   sin munición, parlamentos sin interrupción, frases predecibles) más el **Guion Mudo**: esconde
   el diálogo entero para comprobar si el conflicto se entiende solo con la acción.

Con los cuatro gates cerrados se desbloquea la exportación: **PDF** con formato de industria
(Courier 12, A4, páginas numeradas), `.fountain`, `.fdx`, texto plano, la **Biblia de
Desarrollo** completa y un **informe de telemetría dramática** del proyecto entero. Y, si se
quiere, el **prompt maestro** para un agente de IA: traduce toda la Biblia —vértice, idea
controladora, antagonismo, estructura, escena por escena— a instrucciones, para generar una
primera versión del guion que sí respeta lo que se construyó en los cuatro módulos anteriores.

---

## Probarlo sin instalar nada

No hace falta cuenta ni base de datos para recorrer los 5 módulos: entrando directamente en la
app sin pasar por el instalador se activa el **modo invitado** — el proyecto vive en el
navegador y se puede exportar igual. Desde la portada, **"Ver un ejemplo terminado"** carga
*El turno de noche* tal y como se ha descrito arriba, con los cuatro gates ya cerrados.

---

## Por qué está construida así

**El % de progreso y las alertas que bloquean son dos cosas distintas.** Se puede llegar al
  100 % de campos rellenos y seguir bloqueado porque la historia no se sostiene (dos personajes
  cumpliendo la misma función, una escena que no cambia nada, un clímax que no contradice al
  final). El servidor recalcula las alertas en cada guardado, así que el bloqueo no depende de
  que el navegador coopere.

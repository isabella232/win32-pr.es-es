---
title: Mouse y punteros
description: El mouse es el dispositivo de entrada principal que se usa para interactuar con los objetos de Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6462c69216ee9acb5149a01a805503cea721bb1c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104003295"
---
# <a name="mouse-and-pointers"></a>Mouse y punteros

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El mouse es el dispositivo de entrada principal que se usa para interactuar con los objetos de Windows. La funcionalidad del mouse también puede abarcar otros dispositivos señaladores, como los tableros de bola, los paneles táctiles y los palos integrados en los equipos portátiles, los lápices usados con la tecnología táctil y la tableta de Windows y, en equipos con pantallas táctiles, incluso el dedo de un usuario.

> [!NOTE]
> Las instrucciones relacionadas con la [accesibilidad](inter-accessibility.md), el [lápiz](inter-pen.md)y la [entrada táctil](inter-touch.md) se presentan en artículos independientes.

Al mover físicamente el mouse, se mueve el puntero gráfico (también denominado cursor) en la pantalla. El puntero tiene varias formas para indicar su comportamiento actual.

![captura de pantalla de cinco punteros de mouse típicos ](images/inter-mouse-image1.png)

*Punteros de mouse típicos*

Los dispositivos de mouse suelen tener un botón primario (normalmente el botón izquierdo), un botón secundario (normalmente el derecho) y una rueda del mouse entre los dos. Al colocar el puntero y hacer clic en los botones primario y secundario del mouse, los usuarios pueden seleccionar objetos y realizar acciones en ellos. Para la mayoría de las interacciones, al presionar un botón del mouse mientras el cursor está sobre un destino se indica el destino seleccionado y al soltar el botón se realiza cualquier acción asociada con el destino.

Todos los punteros, excepto el puntero ocupado, tienen una zona activa de un solo píxel que define la ubicación exacta de la pantalla del mouse. La zona activa determina qué objeto se ve afectado por las acciones del mouse. Los objetos definen una zona activa, que es el área donde se considera que la zona activa está sobre el objeto. Normalmente, la zona activa coincide con los bordes de un objeto, pero puede ser más grande para facilitar la realización de la intención del usuario.

El símbolo de intercalación es la barra vertical parpadeante que se muestra cuando el usuario escribe en un cuadro de texto u otro editor de texto. El símbolo de intercalación es independiente del puntero (de forma predeterminada, Windows oculta el puntero mientras el usuario está escribiendo).

![captura de pantalla de un cuadro de texto con cursor ](images/inter-mouse-image2.png)

*Símbolo de intercalación*

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="the-mouse-is-intuitive"></a>El mouse es intuitivo

El mouse ha sido un dispositivo de entrada correcto porque es fácil de usar para la mano habitual. La interacción basada en punteros se ha realizado correctamente porque es intuitiva y permite una amplia variedad de experiencias.

**Se dice que los objetos de interfaz de usuario (UI) bien diseñados tienen la rentabilidad, que son propiedades visuales y de comportamiento de un objeto que sugieren cómo se utiliza.** El puntero actúa como un proxy para la mano, lo que permite a los usuarios interactuar con objetos de pantalla de forma muy similar a como lo harían con objetos físicos. Los seres humanos tienen una descripción INNATE de cómo funciona la mano, por lo que si se produce algo parecido, se intenta insertarlo. Si parece que se puede capturar, intentamos captarla. Por lo tanto, los usuarios pueden averiguar cómo usar los objetos con un bajo nivel de atención simplemente mirando a ellos y probando.

![captura de pantalla de un botón y un control deslizante](images/inter-mouse-image3.png)

*Los botones y los controles deslizantes tienen una alta prestación*

Por el contrario, los objetos con un precio deficiente son más difíciles de averiguar. Estos objetos suelen requerir una etiqueta o una instrucción para explicarlos.

![captura de pantalla del icono de texto de vínculo y de Internet Earth](images/inter-mouse-image4.png)

*el texto del vínculo y los iconos tienen un bajo precio*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Algunos aspectos del uso del mouse no son intuitivos

**Hacer clic con el botón derecho, hacer doble clic y hacer clic con los modificadores de tecla Mayús o Ctrl son tres interacciones de mouse que no son intuitivas**, ya que no tienen homólogos reales. A diferencia de los métodos abreviados de teclado y las teclas de acceso, estas interacciones del mouse normalmente no están documentadas en ninguna parte de la interfaz de usuario. Esto sugiere que no es necesario hacer clic con el botón derecho, hacer doble clic y modificadores de teclado para realizar tareas básicas, especialmente por parte de usuarios inexpertos. También sugiere que estas interacciones avanzadas deben tener un comportamiento coherente y predecible para usarse de forma eficaz.

### <a name="single-click-or-double-click"></a>¿Un solo clic o doble clic?

Si hace doble clic, se usa con tanta frecuencia en el escritorio de Windows que es posible que no parezca una interacción avanzada. Por ejemplo, la apertura de carpetas, programas o documentos en el panel archivo del explorador de Windows se realiza haciendo doble clic en. Al abrir un acceso directo en el escritorio de Windows, también se usa el doble clic. Por el contrario, la apertura de carpetas o programas en el menú Inicio requiere un solo clic.

Los objetos seleccionables usan un solo clic para realizar la selección, por lo que requieren un doble clic para abrir, mientras que los objetos no seleccionables requieren un solo clic para abrirse. Esta distinción no es entendida por muchos usuarios (al hacer clic en el icono de un programa, al hacer clic en un icono de programa, a la derecha) y, como resultado, algunos usuarios solo mantienen el clic en los iconos hasta que obtienen lo que quieren.

### <a name="direct-manipulation"></a>Manipulación directa

Interactuar con objetos directamente se denomina manipulación directa. Señalar, hacer clic, seleccionar, mover, cambiar el tamaño, dividir, desplazar, desplazarse y hacer zoom son manipulaciones directas comunes. Por el contrario, interactuar con un objeto a través de la ventana Propiedades u otro cuadro de diálogo podría describirse como manipulación indirecta.

**Sin embargo, cuando hay manipulación directa, puede haber una manipulación accidental y, por tanto, la necesidad de forgiveness.** Forgiveness es la capacidad de revertir o corregir fácilmente una acción no deseada. Para realizar manipulaciones directas permisivo, se proporciona la función de deshacer, se proporcionan buenos comentarios visuales y se permite a los usuarios corregir errores fácilmente. Asociado con forgiveness impide que se produzcan acciones no deseadas en el primer lugar, lo que puede hacer mediante el uso de controles restringidos y confirmaciones para acciones o comandos de riesgo que tienen consecuencias no deseadas.

### <a name="standard-mouse-button-interactions"></a>Interacciones del botón estándar del mouse

Las interacciones estándar del mouse dependen de diversos factores, como la tecla del mouse, el número de veces que se hace clic en él, su posición durante los clics y si se presionó algún modificador de teclado. Este es un resumen de cómo estos factores suelen afectar a la interacción:

- Para la mayoría de los objetos, al hacer doble clic se realiza un solo clic a la izquierda y se ejecuta el comando predeterminado. El comando predeterminado se identifica en el menú contextual.
- En algunos tipos de objetos seleccionables, cada clic expande el efecto del clic. Por ejemplo, si se hace un solo clic en un cuadro de texto, se establece la ubicación de entrada, al hacer doble clic en se selecciona una palabra, y al hacer triple clic en se selecciona una oración o un párrafo.
- Al hacer clic con el botón secundario, se muestra el menú contextual de un objeto.
- Mantener el mouse mientras el puntero se mantiene al pasar el puntero.
- Mantener el mouse mientras se presionan los botones del mouse indica hacer clic y seleccionar un solo objeto. Mover el mouse indica movimiento, cambio de tamaño, división, arrastre y selección de varios objetos.
- La tecla Mayús extiende la selección de forma contigua.
- La tecla Ctrl amplía la selección alternando el estado de selección del elemento en el que se hizo clic sin que ello afecte a la selección de otros objetos.

### <a name="simple-mouse-interactions"></a>Interacciones de mouse simples

En la tabla siguiente se describen las interacciones y los efectos comunes del mouse.

| Acción simple | Interacción | Efecto típico |
|:---|:---|:---|
| Señala<br/>          | Colocar el puntero en un objeto específico sin hacer clic en ningún botón del mouse.<br/>                                                                                                                                                                                                                                      | Destino muestra su estado de activación y las prestaciones dinámicas.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Mantiene<br/>          | Coloque el puntero en un objeto específico sin hacer clic en ningún botón del mouse y sin mover al menos un segundo.<br/>                                                                                                                                                                                             | Destino muestra la información sobre herramientas, el recuadro informativo o el equivalente.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Pulse<br/>          | Coloque el puntero en un objeto específico y no seleccionable y presione y suelte un botón del mouse sin mover. Hacer clic en surte efecto en la versión del botón del mouse para que los usuarios puedan cancelar el clic moviendo el mouse fuera del destino. Por lo tanto, la acción del mouse solo indica el destino seleccionado.<br/> | Para un solo clic con el botón principal, active el objeto. Para hacer doble clic con el botón principal, active el objeto y ejecute el comando predeterminado. Para el botón secundario, muestre el menú contextual del objeto.<br/>                                                                                                                                                                                         |
| Seleccionar<br/>         | Coloque el puntero en un objeto seleccionable específico y presione y suelte el botón del mouse.<br/>                                                                                                                                                                                                                        | Para un solo clic con el botón principal, seleccione el objeto. Si los usuarios arrastran el mouse, seleccione un intervalo contiguo de objetos. Para hacer doble clic con el botón principal, seleccione el objeto y ejecute el comando predeterminado.<br/> En el caso de texto, el botón principal derecho establece el punto de inserción, el segundo selecciona palabra en el punto de inserción y el tercer clic selecciona la oración o el párrafo.<br/> |
| Si presiona<br/>          | Coloque el puntero en un objeto específico y presione un botón del mouse sin soltar.<br/>                                                                                                                                                                                                                              | En el caso de las funciones de repetición automática (como presionar una flecha de desplazamiento para el desplazamiento continuo), se activan de forma repetida. De lo contrario, indica el inicio de un movimiento, cambio de tamaño, división o arrastre, a menos que vaya seguido de una versión sin mover.<br/>                                                                                                                                                                                               |
| Rueda<br/>          | Mueva la rueda del mouse.<br/>                                                                                                                                                                                                                                                                                                  | La ventana se desplaza verticalmente en dirección del movimiento de la rueda del mouse.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Formas de puntero

En la tabla siguiente se describen las formas y los usos de los punteros comunes.

| Forma | Nombre | Cuándo se usa |
|:---|:---|:---|
| ![captura de pantalla de un puntero con forma de flecha ](images/inter-mouse-image5.png)<br/>           | Selección normal<br/>    | Se usa para la mayoría de los objetos.<br/>                                             |
| ![captura de pantalla de mano con el dedo de índice que señala ](images/inter-mouse-image6.png)<br/>    | Selección de vínculo<br/>      | Se usa para los vínculos de texto y de gráficos debido a su escasa asequibilidad.<br/> |
| ![captura de pantalla de un puntero con forma i ](images/inter-mouse-image7.png)<br/>          | Selección de texto<br/>      | Se usa para que el texto indique una ubicación entre los caracteres.<br/>           |
| ![captura de pantalla de puntero con la forma grande más-signo ](images/inter-mouse-image8.png)<br/> | Selección de precisión<br/> | Se usa para gráficos y otras interacciones bidimensionales.<br/>            |

### <a name="compound-mouse-interactions"></a>Interacciones de mouse compuestas

En la tabla siguiente se describen las interacciones comunes del mouse.

| Acción compuesta | Interacción | Efecto típico | Punteros |
|:---|:---|:---|:---|
| Traslado<br/>                | Si el movimiento es un modo (que se especifica al proporcionar un comando), escriba el modo, coloque el puntero sobre un objeto movible, presione el botón y mueva el mouse, suelte el botón del mouse. en este caso, el puntero cambia de forma para indicar el modo.<br/> en caso contrario, coloque el puntero sobre el enganche de un objeto móvil, presione el botón y mueva el mouse, suelte el botón del mouse. en este caso, no es necesario que el puntero cambie de forma.<br/> | el objeto se mueve en dirección del movimiento del puntero.<br/>            | mover<br/> ![captura de pantalla de puntero con cuatro flechas ](images/inter-mouse-image9.png)<br/> se usa para desplace una ventana en cualquier dirección.<br/> panorámica<br/> ![captura de pantalla de un puntero con forma de mano ](images/inter-mouse-image10.png)<br/> Se usa para trasladar un objeto dentro de una ventana en cualquier dirección.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Cambio de tamaño<br/>              | Coloque el puntero sobre un borde de tamaño variable o un controlador de tamaño, presione un botón del mouse y mueva el mouse y suelte el botón del mouse.<br/>                                                                                                                                                                                                                                                                                 | el objeto cambia de tamaño en dirección del movimiento del puntero.<br/>          | tamaño vertical y horizontal<br/> ![Captura de pantalla que muestra punteros de flechas.](images/inter-mouse-image11.png)![captura de pantalla de los punteros de flechas arriba y derecha ](images/inter-mouse-image12.png)<br/> se usa para cambiar el tamaño de una sola dimensión.<br/> cambiar tamaño diagonalmente<br/> ![bb545459. mouse13 (en-US, msdn. 10). png](images/inter-mouse-image13.png)![captura de pantalla de punteros diagonales con sugerencias de flechas](images/inter-mouse-image14.png)<br/> se usa para cambiar el tamaño de dos dimensiones simultáneamente.<br/> cambiar el tamaño de las filas y las columnas<br/> ![bb545459. mouse15 (en-US, msdn. 10). png](images/inter-mouse-image15.png)![captura de pantalla de punteros de flecha con barras cruzadas ](images/inter-mouse-image16.png)<br/> Se usa para cambiar el tamaño de una fila o columna en una cuadrícula.<br/> |
| División<br/>             | Coloque el puntero sobre un divisor, presione un botón del mouse y mueva el mouse y suelte el botón del mouse.<br/>                                                                                                                                                                                                                                                                                                          | el borde del panel dividido se mueve en dirección del movimiento del puntero.<br/> | separadores de ventanas<br/> ![bb545459. mouse17 (en-US, msdn. 10). png](images/inter-mouse-image17.png)![captura de pantalla de punteros de flecha con doble Cruz ](images/inter-mouse-image18.png)<br/> Se usa para cambiar el tamaño de un panel dividido vertical u horizontalmente.<br/> |
| Arrastrando y colocando<br/> | Coloque el puntero sobre un objeto válido para arrastrarlo, presione un botón del mouse, mueva el mouse a un destino de colocación y suelte el botón del mouse.<br/> | el objeto se mueve o se copia en el destino de colocación.<br/>             | Selección normal<br/> ![captura de pantalla de la fotografía, el puntero estándar y el recuadro informativo ](images/inter-mouse-image19.png)<br/> se usa con destinos de arrastre válidos. también puede tener un recuadro informativo para indicar un efecto específico.<br/> no disponible<br/> ![captura de pantalla del icono pequeño de bloqueado/sin conexión ](images/inter-mouse-image20.png)<br/> Se utiliza para indicar que una superficie no es un destino de colocación válido.<br/> |

### <a name="activity-indicators"></a>Indicadores de actividad

En la tabla siguiente se muestran los punteros que los usuarios ven al realizar una acción que tarda más de un par de segundos en completarse.

| Forma | Nombre | Cuándo se usa |
|:---|:---|:---|
| ![Captura de pantalla que muestra un puntero ' ocupado ' con forma de anillo.](images/inter-mouse-image21.png)<br/>          | Puntero ocupado<br/>                  | Se usa para esperar a que una ventana responda.<br/>                                  |
| ![captura de pantalla de puntero y flecha en forma de anillos](images/inter-mouse-image22.png)<br/> | Trabajar en el puntero en segundo plano<br/> | Se usa para señalar, hacer clic, presionar o seleccionar mientras una tarea se completa en segundo plano.<br/> |

### <a name="hand-pointers"></a>Punteros de mano

Los vínculos de texto y de gráficos usan una mano o un puntero de "selección de vínculo" (una mano con el dedo del índice que señala ![captura de pantalla de mano con el dedo de índice que señala ](images/inter-mouse-image6.png)) debido a su escasa asequibilidad. Mientras que los vínculos pueden tener otras pistas visuales para indicar que son vínculos (como subrayados y una ubicación especial), mostrar el puntero de mano al mantener el puntero es la indicación definitiva de un vínculo.

**Para evitar confusiones, es imperativo no usar el puntero de mano para otros fines.** Por ejemplo, los botones de comando ya tienen una alta disponibilidad, por lo que no necesitan un puntero a mano. El puntero de mano debe significar "este destino es un vínculo" y nada más.

### <a name="custom-pointers"></a>Punteros personalizados

Windows admite la creación de punteros personalizados. Para obtener más información, vea [establecer la imagen del cursor y la entrada del](../learnwin32/setting-the-cursor-image.md) [usuario: ejemplo extendido](../learnwin32/user-input--extended-example.md).

Muchas aplicaciones proporcionan una paleta de controles con punteros personalizados para admitir la funcionalidad de la aplicación.

![captura de pantalla de la paleta con el puntero aerosol-Can ](images/inter-mouse-image23.png)

*Microsoft Paint incluye una paleta de funciones diferentes, cada una con un puntero único*

### <a name="fitts-law"></a>Ley de Fitts

La ley de Fitts es un principio conocido en la ergonomía del diseño de la interfaz gráfica de usuario que básicamente indica:

- Cuanto más lejos se encuentra un destino, más tiempo se tarda en adquirirlo con el mouse.
- Cuanto más pequeño es un destino, más tiempo se tarda en adquirirlo con el mouse.

Por lo tanto, los destinos grandes son buenos. Asegúrese de hacer clic en el área de destino completa.

| Incorrecto | Correcto (todo el destino es en el que se hace clic) |
|:---|:---|
| ![captura de pantalla de un icono con una sola etiqueta en la que se hace clic ](images/inter-mouse-image24.png) | ![captura de pantalla del icono en el que se hace clic y etiqueta en la que se hace clic ](images/inter-mouse-image25.png) |

Puede cambiar dinámicamente el tamaño de un destino cuando señale para facilitar la adquisición.

![captura de pantalla de un mapa de caracteres con un número elevado ](images/inter-mouse-image26.png)

*Un destino es mayor cuando el usuario apunta a facilitar su adquisición*

Y los destinos cercanos también son buenos. Busque elementos en los que se pueda hacer clic cerca de donde sea más probable que se usen. En la imagen siguiente, la paleta de colores está demasiado lejos del selector de herramientas.

![captura de pantalla de la paleta de colores separada de herramientas ](images/inter-mouse-image27.png)

*La paleta de colores está demasiado lejos desde donde es probable que se use*

Tenga en cuenta el hecho de que la ubicación actual del puntero del usuario es tan cercana como el destino puede ser, lo que dificulta la adquisición. Por lo tanto, los menús contextuales sacan el máximo partido de la ley de Fitts, al igual que las Minibarras de herramientas utilizadas por Microsoft Office.

![captura de pantalla de punteros cerca de la lista desplegable ](images/inter-mouse-image28.png)

*La ubicación actual del puntero siempre es la más fácil de adquirir*

Además, tenga en cuenta los dispositivos de entrada alternativos al determinar los tamaños de objeto. Por ejemplo, el tamaño mínimo de destino recomendado para Touch es 23x23 píxeles (13x13 DLU).

### <a name="environments-without-a-mouse"></a>Entornos sin mouse

No todos los entornos de Windows tienen un mouse. Por ejemplo, los quioscos raramente tienen un mouse y normalmente tienen una pantalla táctil. Esto significa que los usuarios pueden realizar interacciones sencillas, como hacer clic con el botón primario y, quizás, arrastrar y colocar. Sin embargo, no pueden mantener el mouse, hacer clic con el botón derecho o hacer doble clic. Esta situación es fácil de diseñar para porque estas limitaciones se suelen conocer de antemano.

El uso de un mouse requiere un buen conocimiento del motor y, como resultado, no todos los usuarios pueden usar un mouse. Para que el software sea accesible para el público más amplio, asegúrese de que todas las interacciones de las que no son esenciales los conocimientos del motor se pueden realizar con el teclado en su lugar.

Para obtener más información e instrucciones, vea [accesibilidad](inter-accessibility.md).

**Si solo hace cuatro cosas...**

1.  Conceda a los comportamientos de interacciones del mouse coherentes con sus efectos estándar, utilizando los punteros estándar siempre que sea apropiado.
2.  Limite las interacciones avanzadas del mouse (aquellas que requieren clics con el botón derecho, varios clics o teclas modificadoras) para tareas avanzadas destinadas a usuarios avanzados.
3.  Asigne interacciones de mouse avanzadas coherentes y predecibles para que se puedan usar de manera eficaz.
4.  Asegúrese de que el programa proporciona la capacidad de revertir o corregir cualquier acción no deseada especialmente para comandos destructivos. Las acciones accidentales son más probables cuando se usa la manipulación directa.

## <a name="guidelines"></a>Directrices

### <a name="click-affordance"></a>Hacer clic en asequibilidad

- **Nunca se requiere que los usuarios haga clic en un objeto para determinar si se pueden hacer clic.** Los usuarios deben poder determinar la posibilidad de hacer clic en la inspección visual por sí solo.
  - La interfaz de usuario principal (por ejemplo, los botones de confirmación) debe tener un compromiso de clic estático. Los usuarios no deben tener que mantener el mouse para detectar la interfaz de usuario principal.
  - La interfaz de usuario secundaria (como los comandos secundarios o los controles de divulgación progresiva) puede mostrar su prestación de clics al mantener el mouse.
  - Los [vínculos de texto](ctrl-links.md) deben sugerir de forma estática el texto del vínculo y, a continuación, mostrar su asequibilidad de clics (subrayado u otro cambio de presentación, con puntero a [mano](#hand-pointers)) al mantener el mouse.
  - Los [vínculos de gráficos](ctrl-links.md) solo muestran un puntero de mano al mantener el mouse.
- **Use el puntero mano (o "seleccionar vínculo") solo para vínculos de texto y gráficos.** De lo contrario, los usuarios tendrían que hacer clic en los objetos para determinar si son vínculos.

### <a name="standard-mouse-button-interactions"></a>Interacciones del botón estándar del mouse

En la tabla siguiente se resumen las interacciones de los botones del mouse que se aplican en la mayoría de los casos:



| Interacción                                    | Efecto                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Al mantener el puntero<br/>                    | Destino muestra la información sobre herramientas, el recuadro informativo o el equivalente.<br/>                                                                                                                                                                                           |
| Un solo clic con el botón primario<br/>        | Activa o selecciona el objeto. En el caso de texto, establece el punto de inserción.<br/>                                                                                                                                                                           |
| Un solo clic con el botón secundario<br/>       | Selecciona el objeto y muestra su menú contextual.<br/>                                                                                                                                                                                              |
| Doble clic con el botón primario<br/>        | Activa o selecciona el objeto y realiza el comando predeterminado. En texto, selecciona Word en el punto de inserción (un tercer clic selecciona la oración o el párrafo).<br/>                                                                            |
| Doble clic con el botón secundario<br/>       | Igual que un solo clic con el botón secundario.<br/>                                                                                                                                                                                                                    |
| Desplazar a la izquierda de un solo clic<br/>  | En el caso de los objetos seleccionables, extiende la selección de forma contigua. De lo contrario, igual que el doble clic con el botón primario con modificaciones posibles. Por ejemplo, en Paint, al dibujar un óvalo con el modificador de tecla Mayús, se dibuja un círculo.<br/>                  |
| Desplazar un solo clic con el botón secundario<br/> | Igual que desplazar un solo clic a la izquierda.<br/>                                                                                                                                                                                                               |
| Desplazar doble clic con el botón primario<br/>  | Igual que desplazar un solo clic a la izquierda, y realiza el comando predeterminado en toda la selección.<br/>                                                                                                                                                     |
| Desplazar doble clic con el botón secundario<br/> | Igual que desplazar un solo clic a la izquierda.<br/>                                                                                                                                                                                                               |
| Ctrl + clic a la izquierda<br/>   | En el caso de los objetos seleccionables, extiende la selección alternando el estado de selección del elemento en el que se hizo clic sin que ello afecte a la selección de otros objetos (lo que permite seleccionar que no sea contiguo). De lo contrario, igual que un solo clic a la izquierda.<br/> |
| Ctrl-clic con el botón secundario<br/>  | Igual que Ctrl a la izquierda, haga clic con el botón primario.<br/>                                                                                                                                                                                                                |
| Ctrl doble clic con el botón primario<br/>   | Igual que Ctrl a la izquierda, hace clic con el botón primario y realiza el comando predeterminado en toda la selección.<br/>                                                                                                                                                      |
| Ctrl + doble clic con el botón secundario<br/>  | Igual que Ctrl a la izquierda, haga clic con el botón primario.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interacción con el mouse

- **Haga clic en los destinos de clics como mínimo de 16x16 píxeles para que pueda hacer clic con facilidad en cualquier dispositivo de entrada.** En el caso de [Touch](inter-touch.md), el tamaño de control mínimo recomendado es 23x23 píxeles (13x13 DLU). Considere la posibilidad de cambiar dinámicamente el tamaño de los destinos pequeños cuando el usuario apunte a facilitar su adquisición.

    En este ejemplo, los botones de control de número son demasiado pequeños para usarse de forma eficaz con la función Touch o Pen.

    ![captura de pantalla del control de número con flechas pequeñas ](images/inter-mouse-image29.png) 

- **Haga que los separadores tengan al menos cinco píxeles de ancho para que se pueda hacer clic con facilidad en cualquier dispositivo de entrada.** Considere la posibilidad de cambiar dinámicamente el tamaño de los destinos pequeños cuando el usuario apunte a facilitar su adquisición.

    En este ejemplo, el divisor del panel de navegación del explorador de Windows es demasiado estrecho para usarse de forma eficaz con un mouse o un lápiz.

    ![captura de pantalla de divisor estrecho y casi invisible ](images/inter-mouse-image30.png)

- **Proporcionar a los usuarios un margen de error espacial.** Permite algún movimiento del mouse (por ejemplo, tres píxeles) cuando los usuarios sueltan un botón del mouse. A veces, los usuarios mueven el mouse ligeramente al soltar el botón del mouse, por lo que la posición del mouse justo antes del lanzamiento del botón refleja mejor la intención del usuario que la posición justo después.
- **Proporcionar a los usuarios un margen de error temporal.** Use la velocidad de doble clic del sistema para distinguir entre los clics únicos y dobles.
- **Haga clic en aplicar al botón del mouse.** Permitir a los usuarios abandonar las acciones del mouse quitando el mouse de destinos válidos antes de soltar el botón del mouse. Para la mayoría de las interacciones con el mouse, al presionar un botón del mouse solo se indica el destino seleccionado y al soltar el botón se activa la acción. Las funciones de repetición automática (como presionar una flecha de desplazamiento para el desplazamiento continuo) son una excepción.
- [Capturar el mouse](/windows/win32/api/winuser/nf-winuser-setcapture) para seleccionar, mover, cambiar de tamaño, dividir y arrastrar.
- Use la tecla ESC para permitir que los usuarios abandonen interacciones de mouse compuestas, como mover, cambiar de tamaño, dividir y arrastrar.
- **Si un objeto no admite doble clic pero es probable que los usuarios lo asuman, interprete un "doble clic" como un solo clic.** Supongamos que el usuario pretendía una sola acción en lugar de dos.

    Dado que es probable que los usuarios asuman que los botones de la barra de tareas admiten doble clic, el "doble clic" se debe tratar como un solo clic.

    ![captura de pantalla del botón de la barra de tareas y puntero estándar ](images/inter-mouse-image31.png)

- **Omitir los clics redundantes del mouse mientras el programa está inactivo.** Por ejemplo, si el usuario hace clic en un botón 10 veces mientras un programa está inactivo, lo interpreta como un solo clic.
- **No utilice las arrastres ni las cuerdas dobles.** Una operación de arrastrar doble es una acción de arrastrar iniciada con un doble clic y una cuerda cuando se presionan varios botones del mouse simultáneamente. Estas interacciones no son estándar, no se pueden detectar, son difíciles de realizar y es más probable que se realicen de forma accidental.
- **No use Alt como modificador para las interacciones con el mouse.** La tecla Alt está reservada para el acceso y las teclas de acceso de la barra de herramientas.
- **No use Mayús + Ctrl como modificador para las interacciones con el mouse.** Hacerlo sería demasiado difícil de usar.
- **Haga que el mantener el mouse sea redundante.** Para que el programa se pueda tocar, saque el máximo partido de Hover, pero solo de maneras que no son necesarias para realizar una acción. Normalmente, esto significa que una acción también se puede realizar haciendo clic, pero no necesariamente exactamente de la misma manera. El desplazamiento no es compatible con la mayoría de las tecnologías táctiles, por lo que los usuarios con estas pantallas no pueden realizar ninguna tarea que requiera el desplazamiento.

### <a name="mouse-wheel"></a>Rueda del mouse

- **Hace que la rueda del mouse afecte al control, panel o ventana en los que está actualmente el puntero.** Al hacerlo, se evitan los resultados imprevistos.
- **Hacer que la rueda del mouse surta efecto sin hacer clic o tener el foco de entrada.** El desplazamiento es suficiente.
- **Haga que la rueda del mouse afecte al objeto con el ámbito más específico.** Por ejemplo, si el puntero se encuentra sobre un control de cuadro de lista desplazable en un panel desplazable dentro de una ventana desplazable, la rueda del mouse afecta al control de cuadro de lista.
- **No cambie el foco de entrada al usar la rueda del mouse.**
- Dé a la rueda del mouse los siguientes efectos:
  - Para ventanas, paneles y controles desplazables:
    - **Al girar la rueda del mouse se desplaza el objeto verticalmente, donde se desplaza hacia arriba.** Para que la rueda tenga una asignación natural, el giro de la rueda del mouse nunca debe desplazarse horizontalmente, ya que esto es desorientando e inesperado.
      - **Si se presiona la tecla Ctrl, al girar la rueda del mouse se amplía el objeto, en el** que la rotación se acerca y gira hacia abajo.
      - **Al inclinar la rueda del mouse se desplaza horizontalmente el objeto.**
  - Para ventanas y paneles que se amplían (sin barras de desplazamiento):
    - **Al girar la rueda del mouse, se amplía el objeto, en el que la** rotación se acerca y gira hacia abajo.
    - La inclinación de la rueda del mouse no tiene ningún efecto.
  - Para las pestañas:
    - Al **girar la rueda del mouse se puede cambiar la pestaña actual,** independientemente de la orientación de las fichas.
    - La inclinación de la rueda del mouse no tiene ningún efecto.
  - Si las teclas Mayús y Alt están presionadas, la rueda del mouse no tiene ningún efecto.
- **Utilice la configuración del sistema de Windows para el tamaño de desplazamiento vertical (para rotar) y el tamaño de desplazamiento horizontal (para la inclinación).** Estas opciones se pueden configurar mediante el elemento del panel de control del mouse.
- **Haga que el desplazamiento de la rueda del mouse resulte más rápido al desplazarse más rápidamente.** Esto permite a los usuarios desplazar documentos grandes de forma más eficaz.
- **En el caso de las ventanas desplazables, considere la posibilidad de hacer clic en el botón de la rueda del mouse para colocar la ventana en "modo de lectura".** El modo lector incorpora un icono especial de origen de desplazamiento y desplaza la ventana en una dirección y velocidad con respecto al origen de desplazamiento.

![captura de pantalla de la página con el icono de desplazamiento de origen ](images/inter-mouse-image32.png)

*Internet Explorer admite el modo lector, que incluye el icono de desplazamiento de origen*

### <a name="hiding-the-pointer"></a>Ocultar el puntero

- **No oculte el puntero.** Excepciones:
  - Las aplicaciones de presentación que se ejecutan en modo de presentación de pantalla completa pueden ocultar el puntero. Sin embargo, el puntero se debe restaurar inmediatamente cuando los usuarios mueven el mouse y se pueden volver a ocultar después de dos segundos de inactividad.
  - Los entornos sin mouse (como quioscos) pueden ocultar el puntero de forma permanente.
- De forma predeterminada, Windows oculta el puntero mientras el usuario está escribiendo en un cuadro de texto. Esta configuración del sistema de Windows se puede configurar mediante el elemento del panel de control del mouse.

### <a name="activity-pointers"></a>Punteros de actividad

Los punteros de actividad en Windows son el puntero ocupado (![captura de pantalla de puntero en forma de anillos ](images/inter-mouse-image33.png)) y el puntero de trabajo en segundo plano (![captura de pantalla de puntero y flecha en forma de anillos ](images/inter-mouse-image34.png)).

- Muestra el puntero ocupado cuando los usuarios tienen que esperar más de un segundo para que se complete una acción. Tenga en cuenta que el puntero ocupado no tiene ninguna zona activa, por lo que los usuarios no pueden hacer clic en nada mientras se muestra.
- Muestra el puntero de trabajo en segundo plano cuando los usuarios tienen que esperar más de un segundo para que se complete una acción, pero el programa responde y no hay ningún otro comentario visual de que la acción no esté completa.
- No combine punteros de actividad con barras de progreso ni animaciones de progreso.

### <a name="caret"></a>Símbolo de intercalación

- **No mostrar el símbolo de intercalación hasta que la ventana Entrada de texto o el control tenga el foco de entrada.** El símbolo de intercalación sugiere el foco de entrada a los usuarios, pero una ventana o un control pueden mostrar el símbolo de intercalación sin el foco de entrada. Por supuesto, no robe el foco de entrada para que un cuadro de diálogo fuera de contexto pueda mostrar el símbolo de intercalación.

    El administrador de credenciales de Windows se muestra fuera de contexto con el símbolo de intercalación, pero sin el foco de entrada. Como resultado, los usuarios acaban de escribir su contraseña en lugares inesperados.

    ![captura de pantalla del administrador de credenciales sin foco ](images/inter-mouse-image35.png)

- **Coloque el símbolo de intercalación en el que es más probable que los usuarios escriban primero.** Normalmente, es el último lugar en el que el usuario estaba escribiendo o al final del texto.

### <a name="accessibility"></a>Accesibilidad

- Para los usuarios que no pueden usar el mouse en absoluto, haga que el mouse esté redundante con el teclado.
  - Los usuarios deben ser capaces de hacer todo con el teclado que puedan usar el mouse, excepto acciones para las que son esenciales los conocimientos del motor, como el dibujo y la reproducción de juegos.
  - Los usuarios deben ser capaces de hacer todo con el mouse que puedan con el teclado, excepto la entrada de texto eficaz.
- Para usuarios con capacidad limitada para usar el mouse:
  - No haga doble clic y arrastre la única forma de realizar una acción.

Para obtener más información e instrucciones, vea [accesibilidad](inter-accessibility.md).

## <a name="documentation"></a>Documentación

Al hacer referencia al mouse:

- Evite usar los ratones en plural; Si necesita hacer referencia a más de un mouse, use los dispositivos de mouse.
- Use el botón del mouse para indicar el botón primario del mouse. No use el botón primario del mouse. Del mismo modo, use el botón secundario del mouse en lugar del botón secundario del mouse. Independientemente de la precisión, los usuarios entienden estos términos y los usuarios que reprograman sus botones realizan el cambio mental.
- Use la rueda para girar la parte de la rueda del mouse y el botón de rueda para hacer referencia al elemento en el que se hace clic.
- Utilice verbos como click, Point y Drag para hacer referencia a las acciones del mouse. Los usuarios giran la rueda verticalmente, lo inclinan horizontalmente y hacen clic en el botón de rueda.
- Use arrastrar, no arrastrar y colocar para la acción de mover un documento o una carpeta. Es aceptable usar arrastrar y colocar como adjetivo, como en "mover la carpeta es una operación de arrastrar y colocar".
- Divida siempre el doble clic y haga clic con el botón derecho como verbos.
- Use hacer clic, no haga clic en. Haga clic en en (como en "hacer clic en la ventana") es aceptable.

Al hacer referencia a los punteros del mouse:

- Haga referencia al puntero del mouse como puntero. Use cursor solo en la documentación técnica de.
- En el caso de los punteros con indicadores de actividad, utilice el puntero busy para el puntero que consta solo de un indicador de actividad y para trabajar en puntero en segundo plano para el puntero de combinación y el indicador de actividad.
- En el caso de los demás tipos de punteros, no use etiquetas descriptivas para hacer referencia al puntero. Si es necesario, use un gráfico para describir cómo puede aparecer el puntero del mouse en la pantalla.

**Ejemplos:**

- Señale al borde de la ventana.
- Con el mouse, haga clic en el botón **minimizar** .
- Mantenga presionada la tecla Mayús y haga clic con el botón secundario del mouse.
- Cuando el puntero se convierte en un ![captura de pantalla de la flecha con dos barras cruzadas](images/inter-mouse-image18.png), arrastre el puntero para moverlo a la línea de división.

## <a name="see-also"></a>Vea también

- [Directrices de interacción de accesibilidad](inter-accessibility.md)
- [Directrices de interacción táctil](inter-touch.md)
- [Instrucciones de interacción del lápiz](inter-pen.md)
- [Vínculos de texto](ctrl-links.md)
- [Vínculos de gráficos](ctrl-links.md)
- [Capturar el mouse](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Establecer la imagen del cursor](../learnwin32/setting-the-cursor-image.md)
- [Entrada de usuario: ejemplo extendido](../learnwin32/user-input--extended-example.md)
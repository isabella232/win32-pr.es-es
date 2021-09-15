---
title: Mouse y punteros
description: El mouse es el dispositivo de entrada principal que se usa para interactuar con objetos de Windows.
ms.assetid: 4d99287d-e908-4c8b-b4f6-6e8c91c6c93e
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6462c69216ee9acb5149a01a805503cea721bb1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570369"
---
# <a name="mouse-and-pointers"></a>Mouse y punteros

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El mouse es el dispositivo de entrada principal que se usa para interactuar con objetos de Windows. La funcionalidad del mouse también puede abarcar otros dispositivos que apuntan, como las esferas de seguimiento, los controles táctiles y los palos que apuntan integrados en equipos de cuadernos, los lápices usados con Tecnología táctil y Tablet PC de Windows y, en equipos con pantalla táctil, incluso el dedo de un usuario.

> [!NOTE]
> Las instrucciones relacionadas con [la accesibilidad,](inter-accessibility.md) [el lápiz](inter-pen.md)y la [entrada](inter-touch.md) táctil se presentan en artículos independientes.

Mover físicamente el mouse mueve el puntero gráfico (también conocido como cursor) en la pantalla. El puntero tiene una variedad de formas para indicar su comportamiento actual.

![captura de pantalla de cinco punteros de mouse típicos ](images/inter-mouse-image1.png)

*Punteros de mouse típicos*

Los dispositivos del mouse suelen tener un botón principal (normalmente el botón izquierdo), un botón secundario (normalmente a la derecha) y una rueda del mouse entre los dos. Al colocar el puntero y hacer clic en los botones principal y secundario del mouse, los usuarios pueden seleccionar objetos y realizar acciones en ellos. Para la mayoría de las interacciones, al presionar un botón del mouse mientras el cursor está sobre un destino se indica el destino seleccionado y al soltar el botón se realiza cualquier acción asociada al destino.

Todos los punteros, excepto el puntero ocupado, tienen una zona activa de un solo píxel que define la ubicación exacta de la pantalla del mouse. La zona de acceso caliente determina qué objeto se ve afectado por las acciones del mouse. Los objetos definen una zona de acceso caliente, que es el área en la que se considera que la zona de acceso es sobre el objeto. Normalmente, la zona de acceso rápido coincide con los bordes de un objeto, pero puede ser mayor para facilitar el rendimiento de la intención del usuario.

El elemento de subrayado es la barra vertical parpadeante que se muestra cuando el usuario escribe en un cuadro de texto u otro editor de texto. El cursor de referencia es independiente del puntero (de forma predeterminada, Windows oculta el puntero mientras el usuario escribe).

![captura de pantalla del cuadro de texto con cursor ](images/inter-mouse-image2.png)

*El centro de atención*

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="the-mouse-is-intuitive"></a>El mouse es intuitivo

El mouse ha sido un dispositivo de entrada correcto porque es fácil de usar para la mano humana típica. La interacción basada en punteros ha sido correcta porque es intuitiva y permite una amplia variedad de experiencias.

**Se dice que los objetos de interfaz de usuario (UI) bien diseñados tienen una asequibilidad, que son propiedades visuales y de comportamiento de un objeto que sugieren cómo se usa.** El puntero actúa como proxy para la mano, lo que permite a los usuarios interactuar con objetos de pantalla de forma muy parecido a como lo harían con los objetos físicos. Los seres humanos tenemos una comprensión innate de cómo funciona la mano humana, por lo que si algo parece que se puede insertar, intentamos insertarla. Si parece que se puede agarrar, intentamos agarrarlo. Por lo tanto, los usuarios pueden averiguar cómo usar objetos con una buena asequibilidad con solo mirarlos y probarlos.

![captura de pantalla de un botón y un control deslizante](images/inter-mouse-image3.png)

*Los botones y los controles deslizantes tienen una asequibilidad segura*

Por el contrario, los objetos con una asequibilidad deficiente son más difíciles de averiguar. Estos objetos a menudo requieren una etiqueta o una instrucción para explicarlos.

![captura de pantalla del texto del vínculo y el icono de Internet Earth](images/inter-mouse-image4.png)

*el texto de vínculo y los iconos tienen una asequibilidad deficiente*

### <a name="some-aspects-of-mouse-use-are-not-intuitive"></a>Algunos aspectos del uso del mouse no son intuitivos

**Hacer clic con el botón derecho,** hacer doble clic y hacer clic con los modificadores de tecla Mayús o Ctrl son tres interacciones del mouse que no son intuitivas, porque no tienen equivalentes reales. A diferencia de los métodos abreviados de teclado y las teclas de acceso, estas interacciones del mouse normalmente no se documentan en ninguna parte de la interfaz de usuario. Esto sugiere que no es necesario hacer clic con el botón derecho, hacer doble clic y modificadores de teclado para realizar tareas básicas, especialmente para los usuarios principiantes. También sugiere que estas interacciones avanzadas deben tener un comportamiento coherente y predecible para poder usarse de forma eficaz.

### <a name="single-click-or-double-click"></a>¿Un solo clic o doble clic?

El doble clic se usa con tanta frecuencia en Windows escritorio que puede que no parezca una interacción avanzada. Por ejemplo, la apertura de carpetas, programas o documentos en el panel de archivos de Windows Explorer se realiza haciendo doble clic. Al abrir un acceso directo en Windows escritorio también se hace doble clic. Por el contrario, la apertura de carpetas o programas en menú Inicio requiere un solo clic.

Los objetos seleccionables usan un solo clic para realizar la selección, por lo que requieren un doble clic para abrirse, mientras que los objetos que no se pueden seleccionar solo requieren un solo clic para abrirse. Muchos usuarios no entienden esta distinción (hacer clic en un icono de programa es hacer clic en un icono de programa, ¿no?) y, como resultado, algunos usuarios simplemente siguen haciendo clic en los iconos hasta que obtienen lo que quieren.

### <a name="direct-manipulation"></a>Manipulación directa

La interacción directa con objetos se conoce como manipulación directa. Apuntar, hacer clic, seleccionar, mover, cambiar el tamaño, dividir, desplazar, desplazar, desplazar y zoom son manipulaciones directas comunes. Por el contrario, la interacción con un objeto a través de su ventana de propiedades u otro cuadro de diálogo se podría describir como manipulación indirecta.

**Sin embargo, cuando hay manipulación directa, puede haber una manipulación accidental y, por lo tanto, la necesidad de una repulsa.** La excepción es la capacidad de invertir o corregir fácilmente una acción no deseada. Las manipulaciones directas se permiten proporcionando deshacer, proporcionando buenos comentarios visuales y permitiendo a los usuarios corregir errores fácilmente. Asociado a la insondez, impide que se realicen acciones no deseadas en primer lugar, lo que se puede hacer mediante controles restringidos y confirmaciones de acciones o comandos de riesgo que tienen consecuencias involuntarias.

### <a name="standard-mouse-button-interactions"></a>Interacciones estándar del botón del mouse

Las interacciones estándar del mouse dependen de diversos factores, como la tecla del mouse en la que se hizo clic, el número de veces que se hace clic, su posición durante los clics y si se presionó algún modificador de teclado. Este es un resumen de cómo estos factores suelen afectar a la interacción:

- Para la mayoría de los objetos, el doble clic izquierdo realiza un solo clic izquierdo y realiza el comando predeterminado. El comando predeterminado se identifica en el menú contextual.
- Para algunos tipos de objetos seleccionables, cada clic expande el efecto del clic. Por ejemplo, al hacer un solo clic en un cuadro de texto se establece la ubicación de entrada, al hacer doble clic se selecciona una palabra y al hacer triple clic se selecciona una oración o párrafo.
- Al hacer clic con el botón derecho se muestra el menú contextual de un objeto.
- Mantener el mouse quieto mientras se señala da como resultado mantener el mouse sobre él.
- Mantener el mouse quieto mientras se presionan los botones del mouse indica hacer clic y seleccionar un solo objeto. Mover el mouse indica mover, cambiar el tamaño, dividir, arrastrar y seleccionar varios objetos.
- La tecla Mayús amplía la selección de forma contigua.
- La tecla Ctrl amplía la selección al alternar el estado de selección del elemento en el que se ha hecho clic sin que ello afecte a la selección de otros objetos.

### <a name="simple-mouse-interactions"></a>Interacciones sencillas del mouse

En la tabla siguiente se describen las interacciones y los efectos comunes del mouse.

| Acción sencilla | Interacción | Efecto típico |
|:---|:---|:---|
| Señalando<br/>          | Coloque el puntero a un objeto específico sin hacer clic en ningún botón del mouse.<br/>                                                                                                                                                                                                                                      | El destino muestra su estado de desplazamiento y las asequibilidades dinámicas.<br/>                                                                                                                                                                                                                                                                                                                                                         |
| Flotando<br/>          | Coloque el puntero en un objeto específico sin hacer clic en los botones del mouse y sin moverse durante al menos un segundo.<br/>                                                                                                                                                                                             | El destino muestra su información sobre herramientas, información o equivalente.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Clic<br/>          | Coloque el puntero en un objeto específico no seleccionable y presione y suelte un botón del mouse sin moverse. Al hacer clic en se hace efecto en la liberación del botón del mouse para permitir a los usuarios la oportunidad de cancelar el clic moviendo el mouse fuera del destino. Por lo tanto, presionar el mouse solo indica el destino seleccionado.<br/> | Para los clics únicos con el botón principal, active el objeto . Para hacer doble clic con el botón principal, active el objeto y realice el comando predeterminado. Para el botón secundario, muestre el menú contextual del objeto.<br/>                                                                                                                                                                                         |
| Seleccionar<br/>         | Coloque el puntero en un objeto específico seleccionable y presione y suelte un botón del mouse.<br/>                                                                                                                                                                                                                        | Para los clics únicos con el botón principal, seleccione el objeto . Si los usuarios arrastran el mouse, seleccione un intervalo contiguo de objetos. Para hacer doble clic con el botón principal, seleccione el objeto y realice el comando predeterminado.<br/> Para el texto, el clic del botón primario derecho establece el punto de inserción, el segundo selecciona la palabra en el punto de inserción y el tercer clic selecciona la oración o párrafo.<br/> |
| Si presiona<br/>          | Coloque el puntero a un objeto específico y presione un botón del mouse sin soltarlo.<br/>                                                                                                                                                                                                                              | En el caso de las funciones de repetición automática (como presionar una flecha de desplazamiento para desplazarse continuamente), active repetidamente. De lo contrario, indica el inicio de un movimiento, cambio de tamaño, división o arrastre, a menos que se le haga una liberación sin mover.<br/>                                                                                                                                                                                               |
| Rueda<br/>          | Mueva la rueda del mouse.<br/>                                                                                                                                                                                                                                                                                                  | La ventana se desplaza verticalmente en dirección al movimiento de la rueda del mouse.<br/>                                                                                                                                                                                                                                                                                                                                                      |

### <a name="pointer-shapes"></a>Formas de puntero

En la tabla siguiente se describen formas y usos comunes de puntero.

| Forma | Nombre | Cuándo se usa |
|:---|:---|:---|
| ![captura de pantalla del puntero con forma de flecha ](images/inter-mouse-image5.png)<br/>           | Selección normal<br/>    | Se usa para la mayoría de los objetos.<br/>                                             |
| ![captura de pantalla de la mano con el dedo índice apuntando ](images/inter-mouse-image6.png)<br/>    | Selección de vínculo<br/>      | Se usa para vínculos de texto y gráficos debido a su débil asequibilidad.<br/> |
| ![captura de pantalla del puntero con forma de haz de i ](images/inter-mouse-image7.png)<br/>          | Selección de texto<br/>      | Se usa para el texto para indicar una ubicación entre caracteres.<br/>           |
| ![captura de pantalla del puntero con forma de signo más grande ](images/inter-mouse-image8.png)<br/> | Selección de precisión<br/> | Se usa para gráficos y otra interacción bidimensional.<br/>            |

### <a name="compound-mouse-interactions"></a>Interacciones compuestas del mouse

En la tabla siguiente se describen las interacciones comunes del mouse.

| Acción compuesta | Interacción | Efecto típico | Punteros |
|:---|:---|:---|:---|
| Traslado<br/>                | Si mover es un modo (especificado mediante un comando), escriba el modo , coloque el puntero sobre un objeto móvil, presione el botón y mueva el mouse, suelte el botón del mouse. En este caso, el puntero cambia de forma para indicar el modo.<br/> De lo contrario, coloque el puntero sobre el control de control de un objeto móvil, presione el botón y mueva el mouse y suelte el botón del mouse. En este caso, el puntero no necesita cambiar la forma.<br/> | El objeto se mueve en dirección del movimiento del puntero.<br/>            | mover<br/> ![captura de pantalla del puntero con cuatro flechas ](images/inter-mouse-image9.png)<br/> se usa para mover una ventana en cualquier dirección.<br/> panorámica<br/> ![captura de pantalla del puntero con forma de mano ](images/inter-mouse-image10.png)<br/> Se usa para mover un objeto dentro de una ventana en cualquier dirección.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Cambio de tamaño<br/>              | Coloque el puntero sobre un borde ajustable o un controlador de cambio de tamaño, presione un botón del mouse y mueva el mouse y, a continuación, suelte el botón del mouse.<br/>                                                                                                                                                                                                                                                                                 | Cambia el tamaño del objeto en dirección del movimiento del puntero.<br/>          | cambio de tamaño vertical y horizontal<br/> ![Captura de pantalla que muestra punteros hacia abajo.](images/inter-mouse-image11.png)![captura de pantalla de punteros hacia arriba y hacia la derecha izquierda ](images/inter-mouse-image12.png)<br/> se usa para cambiar el tamaño de una sola dimensión.<br/> cambio de tamaño diagonal<br/> ![bb545459.mouse13(en-us,msdn.10).png](images/inter-mouse-image13.png)![captura de pantalla de punteros diagonales con puntas de flecha](images/inter-mouse-image14.png)<br/> se usa para cambiar el tamaño de dos dimensiones simultáneamente.<br/> cambio de tamaño de fila y columna<br/> ![bb545459.mouse15(en-us,msdn.10).png](images/inter-mouse-image15.png)![captura de pantalla de punteros de flecha con barra cruzada ](images/inter-mouse-image16.png)<br/> Se usa para cambiar el tamaño de una fila o columna de una cuadrícula.<br/> |
| División<br/>             | Coloque el puntero sobre un divisor, presione un botón del mouse y mueva el mouse y, a continuación, suelte el botón del mouse.<br/>                                                                                                                                                                                                                                                                                                          | el borde del panel dividido se mueve en dirección al movimiento del puntero.<br/> | divisores de ventana<br/> ![bb545459.mouse17(en-us,msdn.10).png](images/inter-mouse-image17.png)![captura de pantalla de punteros de flecha con doble barra cruzada ](images/inter-mouse-image18.png)<br/> Se usa para cambiar el tamaño de un panel dividido vertical u horizontalmente.<br/> |
| Arrastrando y colocando<br/> | Coloque el puntero sobre un objeto válido para arrastrar, presione un botón del mouse y mueva el mouse a un destino de colocación y, a continuación, suelte el botón del mouse.<br/> | El objeto se mueve o copia en el destino de colocación.<br/>             | selección normal<br/> ![captura de pantalla de la foto, el puntero estándar y la información ](images/inter-mouse-image19.png)<br/> se usa en destinos de arrastre válidos. también puede tener una información para indicar un efecto específico.<br/> no disponible<br/> ![captura de pantalla del icono pequeño bloqueado o sin conexión ](images/inter-mouse-image20.png)<br/> Se usa para indicar que una superficie no es un destino de colocación válido.<br/> |

### <a name="activity-indicators"></a>Indicadores de actividad

En la tabla siguiente se muestran los punteros que ven los usuarios al realizar una acción que tarda más de un par de segundos en completarse.

| Forma | Nombre | Cuándo se usa |
|:---|:---|:---|
| ![Captura de pantalla que muestra un puntero "ocupado" en forma de anillo.](images/inter-mouse-image21.png)<br/>          | Puntero ocupado<br/>                  | Se usa para esperar a que una ventana responda.<br/>                                  |
| ![captura de pantalla del puntero y la flecha con forma de anillo](images/inter-mouse-image22.png)<br/> | Trabajar en el puntero en segundo plano<br/> | Se usa para apuntar, hacer clic, presionar o seleccionar mientras se completa una tarea en segundo plano.<br/> |

### <a name="hand-pointers"></a>Punteros de mano

Los vínculos de texto y gráfico usan un puntero de mano o "selección de vínculo" (una mano con el dedo índice apuntando ![captura de pantalla de la mano con el dedo índice apuntando ](images/inter-mouse-image6.png)) debido a su débil asequibilidad. Aunque los vínculos pueden tener otras pistas visuales para indicar que son vínculos (como subrayados y colocación especial), mostrar el puntero de la mano al mantener el puntero es la indicación definitiva de un vínculo.

**Para evitar confusiones, es imperativo no usar el puntero de mano para otros fines.** Por ejemplo, los botones de comando ya tienen una asequibilidad segura, por lo que no necesitan un puntero de mano. El puntero de la mano debe significar "este destino es un vínculo" y nada más.

### <a name="custom-pointers"></a>Punteros personalizados

Windows admite la creación de punteros personalizados. Para obtener más información, vea [Setting the Cursor Image and](../learnwin32/setting-the-cursor-image.md) User [Input: Extended Example](../learnwin32/user-input--extended-example.md).

Muchas aplicaciones proporcionan una paleta de controles con punteros personalizados para admitir la funcionalidad de la aplicación.

![captura de pantalla de la paleta con puntero de aspersión ](images/inter-mouse-image23.png)

*Microsoft Paint incluye una paleta de funciones diferentes, cada una con un puntero único.*

### <a name="fitts-law"></a>Ley de Fitts

La ley de Fitts es un principio conocido en el diseño gráfico de la interfaz de usuario que, básicamente, indica:

- Cuanto más lejos esté un destino, más tiempo se tarda en adquirirlo con el mouse.
- Cuanto menor sea un destino, más tiempo se tarda en adquirirlo con el mouse.

Por lo tanto, los destinos grandes son buenos. Asegúrese de que se puede hacer clic en todo el área de destino.

| Incorrecto | Correcto (se puede hacer clic en todo el destino) |
|:---|:---|
| ![captura de pantalla del icono con solo etiqueta en la que se puede hacer clic ](images/inter-mouse-image24.png) | ![captura de pantalla del icono en el que se puede hacer clic y la etiqueta en la que se puede hacer clic ](images/inter-mouse-image25.png) |

Puede cambiar dinámicamente el tamaño de un destino al apuntar para facilitar la adquisición.

![captura de pantalla del mapa de caracteres con número ampliado ](images/inter-mouse-image26.png)

*Un destino se hace mayor cuando el usuario apunta para facilitar la adquisición.*

Y los objetivos cercanos también son buenos. Busque los elementos en los que se puede hacer clic cerca de donde es más probable que se van a usar. En la imagen siguiente, la paleta de colores está demasiado lejos del selector de herramientas.

![captura de pantalla de la paleta de colores separada de las herramientas ](images/inter-mouse-image27.png)

*La paleta de colores está demasiado lejos de donde es probable que se utilice*

Tenga en cuenta el hecho de que la ubicación actual del puntero del usuario está lo más cerca que puede estar un destino, lo que hace que sea trivial adquirir. Por lo tanto, los menús contextuales aprovechan al máximo la ley de Fitts, al igual que las mini barras de herramientas que Microsoft Office.

![captura de pantalla de punteros cerca de la lista desplegable ](images/inter-mouse-image28.png)

*La ubicación del puntero actual siempre es la más fácil de adquirir*

Además, considere la posibilidad de usar dispositivos de entrada alternativos al determinar los tamaños de los objetos. Por ejemplo, el tamaño de destino mínimo recomendado para la función táctil es de 23 x 23 píxeles (13 x 13 D DLL).

### <a name="environments-without-a-mouse"></a>Entornos sin mouse

No todos Windows entornos tienen un mouse. Por ejemplo, los quioscos rara vez tienen un mouse y normalmente tienen una pantalla táctil en su lugar. Esto significa que los usuarios pueden realizar interacciones sencillas, como hacer clic a la izquierda y quizás arrastrar y colocar. Sin embargo, no pueden mantener el puntero, hacer clic con el botón derecho ni hacer doble clic. Esta situación es fácil de diseñar porque estas limitaciones normalmente se conocen de antemano.

El uso de un mouse requiere habilidades motoras precisas y, como resultado, no todos los usuarios pueden usar un mouse. Para que el software sea accesible para el público más amplio, asegúrese de que todas las interacciones para las que las aptitudes motoras finas no son esenciales se pueden realizar con el teclado en su lugar.

Para obtener más información e instrucciones, vea [Accesibilidad.](inter-accessibility.md)

**Si solo hace cuatro cosas...**

1.  Proporcionar comportamientos de interacciones del mouse coherentes con sus efectos estándar, usando los punteros estándar siempre que sea necesario.
2.  Limite las interacciones avanzadas del mouse (aquellas que requieren clics con el botón derecho, varios clics o teclas modificadoras) a tareas avanzadas destinadas a usuarios avanzados.
3.  Asigne interacciones avanzadas del mouse coherentes y predecibles para que se puedan usar de forma eficaz.
4.  Asegúrese de que el programa proporciona la capacidad de invertir o corregir cualquier acción no buscada, especialmente para los comandos destructivos. Las acciones accidentales son más probables cuando se usa la manipulación directa.

## <a name="guidelines"></a>Directrices

### <a name="click-affordance"></a>Hacer clic en la asequibilidad

- **No es necesario que los usuarios haga clic en un objeto para determinar si se puede hacer clic en él.** Los usuarios deben poder determinar la capacidad de clic solo mediante la inspección visual.
  - La interfaz de usuario principal (como los botones de confirmación) debe tener una asequibilidad de clic estática. Los usuarios no deben tener que mantener el mouse para detectar la interfaz de usuario principal.
  - La interfaz de usuario secundaria (como comandos secundarios o controles de divulgación progresiva) puede mostrar su asequibilidad de clic al mantener el puntero.
  - [Los vínculos de](ctrl-links.md) texto deben sugerir estáticamente texto de vínculo y, a continuación, mostrar su asequibilidad de clic (subrayado u otro cambio de presentación, con puntero [de](#hand-pointers)mano) al mantener el puntero.
  - [Los vínculos gráficos](ctrl-links.md) solo muestran un puntero de mano al mantener el puntero.
- **Use el puntero de la mano (o "selección de vínculo") solo para los vínculos de texto y gráfico.** De lo contrario, los usuarios tendrían que hacer clic en objetos para determinar si son vínculos.

### <a name="standard-mouse-button-interactions"></a>Interacciones estándar del botón del mouse

En la tabla siguiente se resumen las interacciones del botón del mouse que se aplican en la mayoría de los casos:



| Interacción                                    | Efecto                                                                                                                                                                                                                                                          |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Al mantener el puntero<br/>                    | El destino muestra su información sobre herramientas, información o equivalente.<br/>                                                                                                                                                                                           |
| Un solo clic con el botón izquierdo<br/>        | Activa o selecciona el objeto . Para el texto, establece el punto de inserción.<br/>                                                                                                                                                                           |
| Un solo clic con el botón derecho<br/>       | Selecciona el objeto y muestra su menú contextual.<br/>                                                                                                                                                                                              |
| Doble clic izquierdo<br/>        | Activa o selecciona el objeto y realiza el comando predeterminado. En el caso del texto, selecciona la palabra en el punto de inserción (un tercer clic selecciona la frase o párrafo).<br/>                                                                            |
| Doble clic con el botón derecho<br/>       | Igual que un solo clic con el botón derecho.<br/>                                                                                                                                                                                                                    |
| Desplazamiento de un solo clic a la izquierda<br/>  | En el caso de los objetos seleccionables, extiende la selección de forma contigua. De lo contrario, igual que un solo clic izquierdo con posibles modificaciones. Por ejemplo, en Paint, dibujar un óvalo con el modificador de tecla Mayús da como resultado dibujar un círculo.<br/>                  |
| Desplazamiento de un solo clic con el botón derecho<br/> | Igual que Mayús con un solo clic a la izquierda.<br/>                                                                                                                                                                                                               |
| Mayús doble clic a la izquierda<br/>  | Igual que Mayús con un solo clic a la izquierda y realiza el comando predeterminado en toda la selección.<br/>                                                                                                                                                     |
| Mayús haga doble clic con el botón derecho<br/> | Igual que Mayús con un solo clic a la izquierda.<br/>                                                                                                                                                                                                               |
| Ctrl clic con el botón izquierdo<br/>   | En el caso de los objetos seleccionables, extiende la selección al alternar el estado de selección del elemento en el que se ha hecho clic sin afectar a la selección de otros objetos (lo que permite la selección que no es contigua). De lo contrario, igual que un solo clic izquierdo.<br/> |
| Ctrl clic con el botón derecho<br/>  | Igual que Ctrl con un solo clic a la izquierda.<br/>                                                                                                                                                                                                                |
| Ctrl doble clic izquierdo<br/>   | Igual que Ctrl con un solo clic izquierdo y realiza el comando predeterminado en toda la selección.<br/>                                                                                                                                                      |
| Ctrl doble clic con el botón derecho<br/>  | Igual que Ctrl con un solo clic a la izquierda.<br/>                                                                                                                                                                                                                |



 

### <a name="mouse-interaction"></a>Interacción del mouse

- **Haga clic en destinos de al menos 16 x 16 píxeles para que cualquier dispositivo de entrada pueda hacer clic en ellos fácilmente.** En [el caso](inter-touch.md)de la función táctil, el tamaño mínimo de control recomendado es de 23 x 23 píxeles (13 x 13 D DLL). Considere la posibilidad de cambiar dinámicamente el tamaño de los destinos pequeños cuando el usuario apunta para que sean más fáciles de adquirir.

    En este ejemplo, los botones de control de número son demasiado pequeños para usarse eficazmente con la función táctil o un lápiz.

    ![captura de pantalla del control de número con flechas pequeñas ](images/inter-mouse-image29.png) 

- **Cree divisores de al menos cinco píxeles de ancho para que cualquier dispositivo de entrada pueda hacer clic en ellos fácilmente.** Considere la posibilidad de cambiar dinámicamente el tamaño de los destinos pequeños cuando el usuario apunta para que sean más fáciles de adquirir.

    En este ejemplo, el divisor del panel de navegación Windows Explorer es demasiado estrecho para usarse eficazmente con un mouse o un lápiz.

    ![captura de pantalla de divisor estrecho casi invisible ](images/inter-mouse-image30.png)

- **Proporcione a los usuarios un margen de error espacialmente.** Permitir cierto movimiento del mouse (por ejemplo, tres píxeles) cuando los usuarios sueltan un botón del mouse. A veces, los usuarios mueven el mouse ligeramente a medida que sueltan el botón del mouse, por lo que la posición del mouse justo antes de la liberación del botón refleja mejor la intención del usuario que la posición inmediatamente posterior.
- **Proporcione a los usuarios un margen de error temporalmente.** Use la velocidad de doble clic del sistema para distinguir entre clics únicos y dobles.
- **Haga que los clics sumen efecto en el botón del mouse hacia arriba.** Permita a los usuarios abandonar las acciones del mouse quitando el mouse de los destinos válidos antes de liberar el botón del mouse. Para la mayoría de las interacciones del mouse, presionar un botón del mouse solo indica el destino seleccionado y liberar el botón activa la acción. Las funciones de repetición automática (como presionar una flecha de desplazamiento para desplazarse continuamente) son una excepción.
- [Capture el mouse](/windows/win32/api/winuser/nf-winuser-setcapture) para seleccionar, mover, cambiar el tamaño, dividir y arrastrar.
- Use la tecla Esc para permitir que los usuarios abandonen las interacciones compuestas del mouse, como mover, cambiar el tamaño, dividir y arrastrar.
- **Si un objeto no admite doble clic, pero es probable que los usuarios lo supongan, interprete un "doble clic" como un solo clic.** Suponga que el usuario ha pensado una sola acción en lugar de dos.

    Dado que es probable que los usuarios supongan que los botones de la barra de tareas admiten doble clic, un "doble clic" debe controlarse como un solo clic.

    ![captura de pantalla del botón de la barra de tareas y el puntero estándar ](images/inter-mouse-image31.png)

- **Omitir los clics redundantes del mouse mientras el programa está inactivo.** Por ejemplo, si el usuario hace clic 10 veces en un botón mientras un programa está inactivo, interprete esto como un solo clic.
- **No use arrastres dobles ni contrabandos.** Una doble acción de arrastrar es una acción de arrastrar iniciada con un doble clic, y un gesto de presión es cuando se presionan varios botones del mouse simultáneamente. Estas interacciones no son estándar, no son detectables, son difíciles de realizar y lo más probable es que se realicen accidentalmente.
- **No use Alt como modificador para las interacciones del mouse.** La tecla Alt está reservada para las claves de acceso y acceso de la barra de herramientas.
- **No use Mayús+Ctrl como modificador para las interacciones del mouse.** Si lo hace, sería demasiado difícil de usar.
- **Haga que el puntero sea redundante.** Para que el programa sea táctil, aproveche al máximo el puntero, pero solo de maneras que no sean necesarias para realizar una acción. Esto suele significar que una acción también se puede realizar haciendo clic, pero no necesariamente de la misma manera. La mayoría de las tecnologías táctiles no admiten el desplazamiento del mouse, por lo que los usuarios con estas pantallas táctiles no pueden realizar ninguna tarea que requiera mantener el puntero.

### <a name="mouse-wheel"></a>Rueda del mouse

- **Haga que la rueda del mouse afecte al control, panel o ventana sobre el que se encuentra el puntero.** Al hacerlo, se evitan resultados no deseados.
- **Haga que la rueda del mouse suba efecto sin hacer clic ni tener el foco de entrada.** Mantener el puntero es suficiente.
- **Haga que la rueda del mouse afecte al objeto con el ámbito más específico.** Por ejemplo, si el puntero está sobre un control de cuadro de lista desplazable en un panel desplazable dentro de una ventana desplazable, la rueda del mouse afecta al control de cuadro de lista.
- **No cambie el foco de entrada al usar la rueda del mouse.**
- Dé a la rueda del mouse los siguientes efectos:
  - Para ventanas, paneles y controles desplazables:
    - **Al girar la rueda del mouse, el objeto se desplaza verticalmente, donde la rotación hacia arriba se desplaza hacia arriba.** Para que la rueda tenga una asignación natural, girar la rueda del mouse nunca debe desplazarse horizontalmente porque hacerlo es desorienta e inesperado.
      - **Si se presiona la tecla Ctrl,** al girar la rueda del mouse se acerca el objeto, donde al girar hacia arriba se acerca y se acerca hacia abajo.
      - **Al inclinar la rueda del mouse, el objeto se desplaza horizontalmente.**
  - Para ventanas y paneles que se pueden acercar (sin barras de desplazamiento):
    - **Al girar la rueda del mouse,** se acerca el objeto, donde al girar hacia arriba se acerca y se reduce la rotación hacia abajo.
    - Inclinar la rueda del mouse no tiene ningún efecto.
  - Para pestañas:
    - **Girar la rueda del mouse puede cambiar la pestaña actual,** independientemente de la orientación de las pestañas.
    - Inclinar la rueda del mouse no tiene ningún efecto.
  - Si las teclas Mayús y Alt están deprimidas, la rueda del mouse no tiene ningún efecto.
- **Use la configuración Windows sistema para el tamaño de desplazamiento vertical (para rotación) y el tamaño de desplazamiento horizontal (para inclinación).** Esta configuración se puede configurar mediante el elemento del panel de control mouse.
- **Hacer que la rotación de la rueda del mouse sea más rápida hace que el desplazamiento sea más rápido.** Esto permite a los usuarios desplazarse por documentos grandes de forma más eficaz.
- **En el caso de las ventanas desplazables, considere la posibilidad de hacer clic en el botón de rueda del mouse para poner la ventana en "modo lector".** El modo lector planta un icono de origen de desplazamiento especial y desplaza la ventana en una dirección y velocidad con respecto al origen del desplazamiento.

![captura de pantalla de la página con el icono de origen de desplazamiento ](images/inter-mouse-image32.png)

*Internet Explorer admite el modo lector, que incluye el icono scroll-origin*

### <a name="hiding-the-pointer"></a>Ocultar el puntero

- **No oculte el puntero.** Excepciones:
  - Las aplicaciones de presentación que se ejecutan en modo de presentación a pantalla completa pueden ocultar el puntero. Sin embargo, el puntero se debe restaurar inmediatamente cuando los usuarios mueven el mouse y se puede volver a inhidratar después de dos segundos de inactividad.
  - Los entornos sin un mouse (como quioscos) pueden ocultar permanentemente el puntero.
- De forma predeterminada, Windows oculta el puntero mientras el usuario escribe en un cuadro de texto. Esta Windows configuración del sistema se puede configurar mediante el elemento del panel de control Mouse.

### <a name="activity-pointers"></a>Punteros de actividad

Los punteros de actividad Windows son el puntero ocupado (![captura de pantalla del puntero en forma de anillo ](images/inter-mouse-image33.png)) y el objeto que funciona en el puntero en segundo plano (![captura de pantalla del puntero y la flecha con forma de anillo ](images/inter-mouse-image34.png)).

- Muestre el puntero ocupado cuando los usuarios tengan que esperar más de un segundo para que se complete una acción. Tenga en cuenta que el puntero ocupado no tiene ningún punto de acceso, por lo que los usuarios no pueden hacer clic en nada mientras se muestra.
- Muestre el puntero de trabajo en segundo plano cuando los usuarios tengan que esperar más de un segundo para que se complete una acción, pero el programa responde y no hay ningún otro comentario visual de que la acción no se haya completado.
- No combine punteros de actividad con barras de progreso ni animaciones de progreso.

### <a name="caret"></a>Símbolo de intercalación

- **No muestre el caret hasta que la ventana o el control de entrada de texto tenga el foco de entrada.** El caret sugiere el foco de entrada a los usuarios, pero una ventana o control puede mostrar el caret sin foco de entrada. Por supuesto, no robo el foco de entrada para que un cuadro de diálogo fuera de contexto pueda mostrar el aviso.

    La Windows Administrador de credenciales se muestra fuera de contexto con el centro de diálogo pero sin foco de entrada. Como resultado, los usuarios terminan escribiendo su contraseña en lugares inesperados.

    ![captura de pantalla del administrador de credenciales sin foco ](images/inter-mouse-image35.png)

- **Coloque el caret donde es más probable que los usuarios escriban primero.** Normalmente, este es el último lugar en el que el usuario estaba escribiendo o al final del texto.

### <a name="accessibility"></a>Accesibilidad

- Para los usuarios que no pueden usar el mouse en absoluto, haga que el mouse sea redundante con el teclado.
  - Los usuarios deben poder hacer todo con el teclado que puedan con el mouse, excepto las acciones para las que las habilidades motoras finas son esenciales, como dibujar y jugar al juego.
  - Los usuarios deben poder hacer todo con el mouse que puedan con el teclado, excepto la entrada de texto eficaz.
- Para los usuarios con capacidad limitada de usar el mouse:
  - No haga doble clic y arrastre la única manera de realizar una acción.

Para obtener más información e instrucciones, vea [Accesibilidad.](inter-accessibility.md)

## <a name="documentation"></a>Documentación

Al hacer referencia al mouse:

- Evite el uso de los mouse plurales; Si necesita hacer referencia a más de un mouse, use dispositivos de mouse.
- Use el botón del mouse para indicar el botón izquierdo del mouse. No use el botón primario del mouse. De forma similar, use el botón derecho del mouse en lugar del botón secundario del mouse. Independientemente de la precisión, los usuarios comprenden estos términos y los usuarios que reprograman sus botones hacen el cambio mental.
- Use la rueda para la parte de rotación de la rueda del mouse y el botón de rueda para hacer referencia a la parte en la que se puede hacer clic.
- Use verbos como hacer clic, apuntar y arrastrar para hacer referencia a las acciones del mouse. Los usuarios giran la rueda verticalmente, la inclinan horizontalmente y hacen clic en el botón de rueda.
- Use arrastrar, no arrastrar y colocar, para la acción de mover un documento o carpeta. Es aceptable usar arrastrar y colocar como adjetivo, como en "mover la carpeta es una operación de arrastrar y colocar".
- Siempre haga doble clic en guiones y haga clic con el botón derecho como verbos.
- Use clic, no haga clic en . Hacer clic en (como en "hacer clic en la ventana") es aceptable.

Al hacer referencia a punteros del mouse:

- Haga referencia al puntero del mouse como puntero. Use cursor solo en la documentación técnica.
- Para los punteros con indicadores de actividad, use el puntero ocupado para el puntero que consta solo de un indicador de actividad y trabajar en el puntero de fondo para el puntero combinado y el indicador de actividad.
- Para los demás tipos de punteros, no use etiquetas descriptivas para hacer referencia al puntero. Si es necesario, use un gráfico para describir cómo puede aparecer el puntero del mouse en la pantalla.

**Ejemplos:**

- Apunte al borde de la ventana.
- Con el mouse, haga clic en **el botón Minimizar.**
- Mantenga presionada la tecla Mayús y haga clic en el botón derecho del mouse.
- Cuando el puntero se convierte en un ![captura de pantalla de flecha con dos barras cruzadas](images/inter-mouse-image18.png), arrastre el puntero para mover la línea dividida.

## <a name="see-also"></a>Vea también

- [Directrices de interacción de accesibilidad](inter-accessibility.md)
- [Directrices de interacción táctil](inter-touch.md)
- [Directrices de interacción con el lápiz](inter-pen.md)
- [Vínculos de texto](ctrl-links.md)
- [Vínculos de gráficos](ctrl-links.md)
- [Captura del mouse](/windows/win32/api/winuser/nf-winuser-setcapture)
- [Establecimiento de la imagen de cursor](../learnwin32/setting-the-cursor-image.md)
- [Entrada del usuario: ejemplo extendido](../learnwin32/user-input--extended-example.md)
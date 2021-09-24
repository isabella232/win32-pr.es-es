---
title: Guía de programación de cadenas de intercambio de composición
description: La API de intercambio de composición es un sucesor inejetivo de la cadena de intercambio DXGI, que permite a las aplicaciones representar y presentar contenido en la pantalla.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: cd87e1d47e3e44c922310937c0106348ebb4954f
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128524009"
---
# <a name="composition-swapchain-programming-guide"></a>Guía de programación de cadenas de intercambio de composición

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

La API de intercambio de composición es un sucesor inejetivo de la cadena de intercambio DXGI, que permite a las aplicaciones representar y presentar contenido en la pantalla. El uso de esta API a través de la cadena de intercambio DXGI tiene varias ventajas. Se proporciona un control más preciso a la aplicación con respecto al estado de la cadena de intercambio y se proporciona más libertad cuando se trata de cómo se usa la cadena de intercambio. Además, la API proporciona una mejor historia para el momento actual preciso.

## <a name="what-is-presentation"></a>¿Qué es la presentación?

*La* presentación es el concepto de mostrar los resultados de las operaciones de dibujo en pantalla. Un *presente* es una única instancia de presentación de una solicitud para mostrar los resultados de una operación de &mdash; dibujo en un solo búfer, en pantalla. Un presente puede contener atributos adicionales que describen cómo mostrar en pantalla. En esta API, un presente también puede tener una hora de destino *,* que es una marca de tiempo relativa al sistema (un tiempo de interrupción) que describe el momento ideal que debe mostrarse el presente. La aplicación puede usarla para controlar con más precisión la velocidad a la que aparece el contenido en la pantalla y para sincronizar los presentaciones con otros eventos del sistema, como una pista de audio.

La parte central de la presentación es la sincronización. Es decir, las operaciones de dibujo las lleva a cabo normalmente una GPU, en lugar de la CPU y, como tales, se ejecutan en una escala de tiempo asincrónica desde la de la CPU que emitió las operaciones inicialmente. La presentación es una operación enviada a la GPU que garantiza que las operaciones de dibujo que se emitieron anteriormente habrán finalizado antes de que el búfer se muestra en pantalla.

Por lo general, la aplicación emitirá muchos presentaciones a lo largo del tiempo y tendrá varias texturas entre las que seleccionar al emitir los presentes. La aplicación debe usar los mecanismos de sincronización que proporciona esta API para asegurarse de que, una vez dibujado y presentado un búfer, no vuelva a dibujar en ese búfer hasta que se haya mostrado ese presente y, posteriormente, se haya reemplazado por un nuevo búfer de un presente posterior. De lo contrario, el contenido del búfer que la aplicación quería presentar inicialmente se puede sobrescribir, ya que ese presente se muestra en pantalla.

## <a name="presentation-modesmdashcomposition-multiplane-overlay-and-iflip"></a>Composición de modos &mdash; de presentación, superposición de varios plano e iflip

El sistema puede mostrar los búferes presentados por la aplicación de varias maneras diferentes.

La manera más sencilla, que es el valor predeterminado, es que el presente se enviará a DWM y el DWM representará un fotograma basado en el búfer que se presentó. Es decir, hay una copia (o con más precisión, una representación 3D) del búfer de presentación en el búfer de reserva que el DWM envía a la pantalla. Este método para mostrar un presente se denomina Composition.

Un modo más avanzado de mostrar un presente sería examinar el búfer de presentación directamente en el hardware y eliminar la copia que tiene lugar. Este método para mostrar un presente se denomina *examen directo.* Cuando se administran los presentes, DWM puede decidir programar el hardware para que analice directamente fuera de un búfer de presentación, ya sea asignando el búfer a un plano de superposición *multiplano* (o plano MPO, para corto) o directamente voltear el búfer al hardware (conocido como volteo *directo).*

Una manera aún más importante de mostrar un presente sería que el kernel de gráficos mostrara los presentes directamente y omitira completamente el DWM. Este método de presentación se conoce como *volteo independiente* (iflip). Tanto la superposición multiplano como el botón iflip se describen en Para obtener [el mejor rendimiento, use el modelo de volteo DXGI](https://devblogs.microsoft.com/directx/dxgi-flip-model/).

La composición es la que se admite más fácilmente, pero también la menos eficaz. La superficie debe asignarse especialmente para ser apta para el examen directo o iflip, y este tipo de asignación especial tiene requisitos del sistema más estrictos que la cadena de intercambio de composición. Solo está disponible en WDDM 3.0 y hardware superior. Como resultado, la aplicación puede consultar la compatibilidad de api para la presentación de solo composición, así como la presentación que cumple los requisitos para el examen directo o iflip.

## <a name="presentation-factory-checking-capability-and-presentation-manager"></a>Generador de presentación, funcionalidad de comprobación y administrador de presentación

El primer objeto que la aplicación usará fuera de la API de intercambio de composición es el generador *de presentación*. La aplicación crea el generador de presentación y se enlaza a un dispositivo Direct3D que la aplicación pasa a la llamada para crear y, como tal, tiene una afinidad con el adaptador de vídeo asociado a ese dispositivo.

El generador de presentación expone métodos para comprobar si el sistema actual y el dispositivo gráfico son capaces de usar la API de intercambio de composición. Puede usar métodos de funcionalidad como [**IPresentationFactory::IsPresentationSupported para**](/windows/win32/api/presentation/nf-presentation-ipresentationfactory-ispresentationsupported) comprobar la compatibilidad del sistema. Si los métodos de funcionalidad indican la compatibilidad del sistema con la API, puede usar el generador de presentación para crear un administrador *de presentaciones.* Este administrador de presentación es el objeto que se usa para realizar funciones de presentación y está enlazado al mismo dispositivo Direct3D y adaptador de vídeo que ese generador de presentación que se usó para crearlo.

Actualmente, los requisitos del sistema para usar la API de intercambio de composición son los controladores de GPU que admiten WDDM (Windows Device Driver Model) 2.0. Para usar la API de intercambio de composición de la manera más avanzada (análisis directo e inversión independiente, *o iflip),* los sistemas necesitarán controladores de GPU que admitan WDDM 3.0.

Si el sistema no es capaz de usar la API de intercambio de composición, la aplicación deberá tener una ruta de acceso de código independiente para controlar la presentación mediante métodos anteriores, como una cadena de intercambio DXGI.

## <a name="register-presentation-buffers-to-present"></a>Registro de búferes de presentación para presentar

El administrador de presentación realiza un seguimiento de los búferes que puede presentar. Para presentar una textura de Direct3D, la aplicación debe crear primero esa textura con Direct3D y luego registrarla con el administrador de presentación. Cuando se ha registrado una textura con el administrador de presentación, se denomina búfer de presentación y ese administrador de presentación puede presentar a partir de ese punto a la pantalla. La aplicación puede agregar y quitar búferes de presentación como desee, aunque hay un número máximo de búferes de presentación que se pueden agregar a un único administrador de presentación (actualmente 31). Estos búferes de presentación también pueden tener distintos tamaños y formatos que se verán efectivos a medida que se presente un búfer de presentación individual.

Una textura se puede registrar con cualquier número de administradores de presentación; sin embargo, esto no se consideraría un uso normal en la mayoría de los casos y mostrará escenarios de sincronización complicados que la aplicación sería responsable de administrar.

## <a name="defining-the-content-to-be-presented"></a>Definición del contenido que se va a presentar

En general, los búferes que presentamos deben asociarse al contenido de un *árbol visual.* Por lo tanto, es  necesario definir un tipo de enlace para que, cuando se presenten problemas de la aplicación, esté claro dónde están diseñados para ir los búferes que se presentan en el árbol visual. Llamamos a este enlace *Contenido de presentación*.

El contenido presentado podría tener muchas formas. Es posible que la aplicación quiera presentar un solo búfer para mostrar, o puede que desee presentar contenido estéreo con búferes para el ojo izquierdo y derecho, y así sucesivamente. La versión inicial de esta API proporciona compatibilidad para presentar un solo búfer a la pantalla.

Definimos una *superficie de presentación para* que sea una forma de contenido de presentación a la que se presenta un solo búfer a la vez. Una superficie de presentación se puede establecer como contenido en un árbol visual y puede mostrar un único búfer de presentación en pantalla a la vez. Los presentadores del Administrador de presentación actualizarán el búfer mostrado por una o varias superficies de presentación de forma atómica.

El administrador de presentación se puede usar para crear una o varias superficies de presentación para un identificador de superficie *de composición determinado.* Cada identificador de superficie de composición se puede enlazar a uno o varios objetos visuales de un árbol visual (por estrategias descritas en la documentación de la API [**Windows.UI.Composition**](/uwp/api/windows.ui.composition) y [**DirectComposition)**](/windows/win32/directcomp/directcomposition-portal) para definir la relación entre la superficie de presentación asociada y dónde aparece en su árbol visual. La aplicación puede actualizar una o varias superficies de presentación, que se envían al sistema y tienen lugar en la siguiente operación actual.

Tenga en cuenta que el administrador de presentación puede presentar cualquier búfer de presentación a cualquier número de superficies de presentación que desee. No hay ninguna restricción. Sin embargo, la aplicación debe realizar un seguimiento de qué búferes ha emitido y dónde, para asegurarse de que no intente emitir nuevo dibujo en ese búfer mientras se sigue mostrando mediante una superficie de presentación.

## <a name="applying-properties-to-presentation-surface"></a>Aplicación de propiedades a la superficie de presentación

Además de especificar qué búferes se mostrarán en una superficie de presentación, un presente también puede especificar otras propiedades para esa superficie de presentación. Estas incluyen propiedades que definen cómo se muestrea la textura de origen, incluido el modo alfa y el espacio de color, cómo se transformará y se colocará la textura de origen, y las restricciones mostradas o de readback para el contenido protegido. Todos ellos se exponen como métodos de establecimiento de propiedades en una superficie de presentación que la aplicación puede cambiar y, al igual que las actualizaciones de búfer, se harán efectivos cuando tenga lugar el presente de la aplicación.

## <a name="presenting-to-the-presenting-surface"></a>Presentación en la superficie de presentación

Una vez que la aplicación crea superficies de presentación, registra búferes de presentación y especifica las actualizaciones que se deben emitir durante un presente, puede aplicar esas propiedades mediante la presentación. La aplicación emite un presente a través del administrador de presentación. Cuando el sistema procesa ese presente, todas las actualizaciones se aplican de forma atómica. Además, la aplicación también puede especificar otras propiedades del presente, como  el momento ideal que debe tener lugar (la hora de destino actual) y otras propiedades más poco frecuentes, como la velocidad de contenido prevista, que se puede usar para habilitar modos de actualización personalizados en el sistema. Puesto que los presentaciones se pueden programar en un momento dado, la aplicación puede emitir varios presentaciones con antelación. Estos presentes se procesarán uno a uno a medida que se alcance su hora programada. 

## <a name="synchronizing-presentation"></a>Sincronización de la presentación

La aplicación debe asegurarse de que, a medida que se representa en los búferes y se presentan problemas, selecciona un búfer para representar en el que no se hace referencia actualmente a ningún otro presente anterior pendiente, ya que al hacerlo se podría sobrescribir el contenido del búfer que se pretende. Además, si la aplicación tiene problemas para representar en un búfer que se muestra actualmente por una superficie de presentación en el hardware de examen, su representación puede detenerse indefinidamente, porque Direct3D no permite la representación del búfer *frontal.*

La API de intercambio de composición proporciona algunos mecanismos diferentes para permitir que la aplicación practique la sincronización adecuada de los búferes que ha presentado.

Se dice que un búfer está *disponible* si no hay ningún presente pendiente que haga referencia a él y el sistema no lo muestre actualmente. De lo contrario, no está disponible. La API proporciona un evento para cada búfer de presentación que indica si el búfer está disponible o no. Este es el método de sincronización más sencillo que puede usar la aplicación. Antes de dibujar en un búfer y presentarlo, la aplicación puede asegurarse de que su *evento* disponible está señalado. El  evento disponible para un búfer determinado queda sin signo en el momento en que se ha enlazado a una superficie de presentación en la API y permanece sin signo hasta que el presente se retira.

En segundo lugar, el administrador de presentación realiza un seguimiento de una barrera *de* retirada de un solo presente para comunicarse con la aplicación que presenta que se ha completado. El valor de la barrera corresponde al identificador actual  del último presente que inició la  fase de retirada de su ciclo de vida, como se describe en la sección ciclo de vida siguiente. Una vez que un presente entra en esta fase, es seguro suponer que los búferes que se han reemplazado por los siguientes presentes se pueden reutilizar.

Este método de sincronización es más avanzado, pero permite un mayor control sobre la limitación del flujo de trabajo y es más informativo sobre el estado del sistema en lo que respecta a la profundidad de la cola actual. Para obtener información general sobre el ciclo de vida de un presente, consulte la sección siguiente.

## <a name="lifecycle-of-a-present"></a>Ciclo de vida de un presente

Los presentes del administrador de presentación se ponen en cola en el sistema como parte de su *cola actual.* Los procesos del sistema se presentan en orden en cola. Además, cada presente tiene un identificador de presente asociado único (para el administrador de presentación), que es un valor de incremento asignado a un presente, empezando por 1 para el primer presente e incrementándose en 1 para cada presente posterior. Este identificador actual se usa en varias partes de la API, como primitivas de sincronización y estadísticas de presentación, para hacer referencia a ese presente concreto.

Cada uno de ellos presenta que los problemas de la aplicación siguen un ciclo de vida específico, como se describe aquí.

Una vez que la aplicación configura los cambios que se realizarán como parte de un presente, usará el administrador de presentación para emitir realmente el presente. En este momento, se dice que el presente está *pendiente.*

Una vez pendiente, un presente se encontrará en la cola actual del administrador de presentación, donde permanecerá hasta que ocurra una de estas dos cosas.

* El presente se *cancela.* El administrador de presentación permite que la aplicación cancele los presentes emitidos anteriormente. Si esto sucede, se dice que se cancela el presente *y,* a continuación, se retira *inmediatamente.* En esta transición,  se actualizarán los eventos disponibles del búfer asociado para el presente cancelado; sin embargo, la barrera retirada actual no se señalará, ya que el presente mostrado anteriormente (antes de los presentes que se cancelaron) permanecerá mostrado. Por esta razón, la aplicación no puede usar la barrera de retirada actual para determinar qué presentaciones se cancelaron. En su lugar, debe aprender esto de la estadística de estado actual que vuelve para cada presente cancelado. Se recomienda que la aplicación use eventos disponibles *del búfer* para buscar un búfer disponible para presentar después de una cancelación. Una vez que se muestre ese presente, el presente anterior iniciará el proceso de retirada y actualizará la barrera actual que se retira.
* Si no se cancela, el presente finalmente estará *listo para* procesarse. Para estar listo, se deben cumplir dos condiciones principales.
  * Se debe completar todo el trabajo de dibujo emitido en el contexto de Direct3D antes de llamar al presente. Esto garantiza que el búfer no se muestra antes de que se complete el dibujo de la aplicación.
  * Si se especificó una hora de destino actual, la hora relativa al sistema actual que esperamos poder mostrar el presente cumple la hora de destino solicitada que la aplicación aplicó al presente.

Cuando el sistema decida buscar un presente para mostrarlo en pantalla,  elegirá el último presente que esté listo para mostrarse. Si hay  varios presentes listos, se omitirán todos los eventos menos el más reciente (es decir, el presente con el identificador presente más grande) y entrarán inmediatamente en el estado retirado, momento  en el que se señalizarán sus eventos disponibles del búfer, pero no se señalizará la barrera de retirada actual, ya que el presente omitido no se aleja del estado mostrado.  

Cuando se *elige el* presente listo para mostrarse, el sistema comienza a realizar el trabajo para mostrarlo en pantalla. Esto puede significar representar el búfer como parte de un marco DWM y, a continuación, solicitar al hardware mostrar ese marco en pantalla, o bien puede significar enviar el búfer directamente al hardware de examen en el caso de iflip. Una vez que esto tiene lugar, se dice que el presente se pone *en cola.* En un nivel alto, esto significa que está en camino de mostrarse.

Cuando el hardware se pone al día para mostrar el presente, se dice que ese presente *se muestra.* Allí permanecerá, visible en pantalla, hasta que llegue un presente posterior y lo reemplace.

Cuando un presente posterior se pone en cola, sabemos que el hardware finalmente va a dejar de mostrar el presente actual. En este momento, se dice que el presente *está retirando*.

Cuando se muestra ese presente posterior, se dice que el presente actual se *retira.*

El administrador de presentación expone una barrera que se retira, que se señala al identificador actual de cada presente cuando entra en el *estado de* retirada. Esta señal indica a la aplicación que se ha vuelto seguro emitir el trabajo de representación en los búferes asociados a ese presente sin dañar un presente anterior. Si la aplicación tiene problemas para  representar el trabajo durante el estado de retirada del  presente, el trabajo de representación se pondrá en cola hasta que el presente entre en el estado retirado, momento en el que se ejecutará. Si el trabajo de representación se emite después de que el presente se *retire,* se ejecutará inmediatamente.

A continuación se muestra un diagrama de este cambio de estado.

![Ciclo de vida de un presente](images/lifecycle-of-a-present.png)

## <a name="diagram-of-buffers-surfaces-and-presents"></a>Diagrama de búferes, superficies y presentaciones

A continuación se muestra un diagrama relacionado con el administrador de presentación, los búferes de presentación, las superficies de presentación, los presentaciones y las actualizaciones.

![Diagrama de búferes, superficies y presentaciones](images/buffers-surfaces-and-presents.png)

En este diagrama se muestra un administrador de presentación, con dos superficies de presentación y tres búferes de presentación, que ha tenido dos presentaciones emitidas hasta ahora el primer búfer presente 1 en la superficie 1 y el búfer 2 en la superficie &mdash; 2. El segundo elemento actual actualizó la superficie 2 para mostrar el búfer de presentación 3 y no cambió el enlace de la superficie 1. Una vez mostrado el presente 2, la superficie 1 mostrará el búfer 1 y la superficie 2 mostrará el búfer 3, que se puede ver en el estado actual de los objetos en el administrador de presentación. Cada presente en la cola tendrá efecto cuando se procese en el sistema.

> [!NOTE]
> Dado que Present 2 no cambió el búfer de la superficie 1, la superficie 1 se dejó enlazada al búfer 1 desde el presente anterior. En este sentido, hay una referencia "implícita" en el búfer 1 en la actualidad 2, ya que la superficie 1 permanecerá enlazada al búfer 1 después de que se muestre el presente 2.

## <a name="adding-presentation-surfaces-to-visual-tree"></a>Adición de superficies de presentación al árbol visual

Las superficies de presentación son contenido que existe como parte de un árbol visual de composición. Cada superficie de presentación está enlazada a un *identificador de superficie de composición*. En Windows.UI.Composition, se puede crear un pincel de superficie para un identificador de superficie de composición preexistida y enlazarse a un objeto visual sprite. En DirectComposition, se puede crear una superficie de composición a partir de un identificador de superficie de composición preexistida y enlazarse como contenido a un objeto visual. Consulte la documentación correspondiente de cada API para obtener más información.

Las API como Windows Media Foundation, creadas para usar esta API, exponen identificadores de superficie de composición que se enlazarán previamente a una superficie de presentación. Una aplicación también puede crear su propio identificador de superficie de composición para enlazar posteriormente a una superficie de presentación y agregar a un árbol visual llamando a [DCompositionCreateSurfaceHandle](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle).

## <a name="reading-presentation-statistics"></a>Lectura de estadísticas de presentación

La API de cadena de intercambio de composición expone *estadísticas* de presentación, que describen diversas información sobre cómo se procesó un presente determinado. Por lo general, la información podría describir cómo se usó una superficie de presentación en un marco DWM, el momento en que se mostró, si se mostró en absoluto, y así sucesivamente.

Hay diferentes tipos de estadísticas de presentación y están diseñadas para ampliarse en versiones futuras de la API. Una aplicación usa el administrador de presentación para registrarse y recibir los tipos de estadísticas que le interesan. A continuación, esas estadísticas se insertan en la cola de *estadísticas del administrador de presentación.* El administrador de presentación expone un evento de *estadísticas* disponibles para las aplicaciones, que es un identificador de eventos que indica cuándo la cola de estadísticas tiene elementos de estadísticas disponibles para leer. Cuando lo haga, la aplicación puede quitar de la cola el primer elemento de estadísticas, leerlo y procesarlo. El administrador de presentación restablecerá el evento de estadísticas disponibles cuando la aplicación haya leído todas las estadísticas que están actualmente en la cola. Normalmente, una aplicación leerá y procesará las estadísticas en un bucle hasta que se restablezca el evento de estadísticas disponibles. Será habitual que la aplicación procese esta cola de estadísticas en el mismo bucle de trabajo que usa para emitir los presentes. El patrón de uso sugerido es priorizar las estadísticas de procesamiento en lugar de emitir nuevos presentaciones, para asegurarse de que la cola no se desborda.

La cola tiene un número máximo de estadísticas de las que realizará el seguimiento, que estarán en el orden de las estadísticas 512-1024. La profundidad máxima de la cola debe ser suficiente para almacenar estadísticas de aproximadamente 5 segundos en casos normales. Si la cola de estadísticas se llena y se notifican más estadísticas, la directiva es que las estadísticas más antiguas se retirarán para hacer espacio.

## <a name="related-topics"></a>Temas relacionados

* [Cadena de intercambio de composición](comp-swapchain-portal.md)
* [Para obtener el mejor rendimiento, use el modelo de volteo DXGI.](https://devblogs.microsoft.com/directx/dxgi-flip-model/)

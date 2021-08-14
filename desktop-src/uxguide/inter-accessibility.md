---
title: Accesibilidad (conceptos básicos de diseño)
description: Diseñar software para accesibilidad significa garantizar que los programas y la funcionalidad estén disponibles fácilmente para la gama más amplia de usuarios, incluidos aquellos que tienen discapacidades y discapacidades.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c38eb3993880d820a4e65fa25a1e910e9e842de823779aaf3ef24dab8635e60e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212494"
---
# <a name="accessibility-design-basics"></a>Accesibilidad (conceptos básicos de diseño)

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Diseñar software para accesibilidad significa garantizar que los programas y la funcionalidad estén disponibles fácilmente para la gama más amplia de usuarios, incluidos aquellos que tienen discapacidades y discapacidades.

El número de usuarios que las características de accesibilidad pueden ayudar a que le sorprenda. Por ejemplo, en el Estados Unidos, las encuestas han demostrado que más de la mitad de todos los usuarios del equipo experimentan dificultades o discapacidades relacionadas con la accesibilidad y es probable que se beneficien del uso de tecnología accesible. Además, abordar el diseño de software con la flexibilidad y la inclusión que son las marcas de accesibilidad a menudo da como resultado una mayor facilidad de uso y la satisfacción del cliente.

![captura de pantalla del cuadro de diálogo "Centro de acceso fácil" ](images/inter-accessibility-image1.png)

El Centro de accesibilidad, disponible en Panel de control, proporciona una ubicación central donde los usuarios pueden elegir y personalizar las características de accesibilidad que desean.

**Nota:** Las instrucciones relacionadas [con el teclado,](inter-keyboard.md) [el mouse,](inter-mouse.md) [el color](vis-color.md)y [el sonido](vis-sound.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

Muchos factores físicos, perceptuales y cognitivos están en juego cuando los usuarios interactúan con hardware y software del equipo. Antes de considerar formas de hacer que las características del programa sean más accesibles, ayuda a obtener información sobre qué tipos de discapacidades y discapacidades existen, y algunas de las tecnologías de asistencia con las que estos usuarios pueden estar trabajando a medida que interactúan con los equipos.

### <a name="types-of-impairments"></a>Tipos de discapacidades

En la tabla siguiente se describen las discapacidades y discapacidades comunes de los usuarios, y se enumeran algunas de las soluciones más importantes que se usan para hacer que los equipos sea más accesibles.



| menoscabo    | Descripción   | Soluciones  |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visual<br/>             | Abarca desde el 17 por ciento de los usuarios (que afecta al 17 por ciento de los usuarios) hasta los graves (lo que afecta al 9 por ciento de los usuarios).<br/>                                                                                                   | Aumento personalizable, colores y contraste; Utilidades de Adicionales; lectores de pantalla.<br/>                                                                                       |
| Oído<br/>            | Va desde la afición (que afecta al 18 por ciento de los usuarios) hasta la grave (que afecta al 2 por ciento de los usuarios).<br/>                                                                                                   | Redundancia de la información: sonido que solo se usa como complemento a la comunicación visual o de texto.<br/>                                                                                     |
| Destreza<br/>          | Va desde la falta de frecuencia (que afecta al 19 por ciento de los usuarios) hasta la grave (que afecta al 5 por ciento de los usuarios). Esta discapacidad suele implicar dificultades para realizar determinadas aptitudes motoras con el teclado o el mouse.<br/> | Redundancia del método de entrada: características del programa a las que acceden equivalentes de mouse o teclado.<br/>                                                                                       |
| Cognitivo<br/>          | Incluye discapacidades de memoria y diferencias perceptuales. Afecta al 16 por ciento de los usuarios.<br/>                                                                                                         | Interfaz de usuario (UI) altamente personalizable; uso de la [divulgación progresiva para](ctrl-progressive-disclosure-controls.md) ocultar la complejidad; uso de iconos y otras ayuda visuales.<br/> |
| Asimiento<br/>            | Incluye sensibilidad visual al movimiento y al flashing.<br/>                                                                                                                                        | Enfoque conservador para modular interfaces, como el uso de animaciones; evitar el parpadeo de pantalla en el intervalo entre 2 Hertz (Hz) y 55 Hz.<br/>                        |
| Voz o idioma<br/> | Incluye dificultades de comunicación verbal y de displicaciones de comunicación.<br/>                                                                                                                                       | Utilidades de revisión ortográfica y gramatical; reconocimiento de voz y tecnología de texto a voz.<br/>                                                                                 |



 

Para obtener más instrucciones sobre cómo ayudar a los usuarios con estas discapacidades, consulte [Abordar discapacidades concretas](#addressing-particular-impairments) más adelante en este artículo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipos de tecnologías de asistencia y características de accesibilidad

**Lectores de pantalla**

Un lector de pantalla permite a los usuarios con discapacidades visuales o discapacidades navegar por una interfaz de usuario mediante la transformación de objetos visuales en audio. Por lo tanto, el texto de la interfaz de usuario, los controles, los menús, las barras de herramientas, los gráficos y otros elementos de pantalla se pronuncian mediante la voz computarizada del lector de pantalla. Para crear un programa optimizado para la tecnología de asistencia del lector de pantalla, debe planear cómo identificará el lector de pantalla cada elemento de la interfaz de usuario.

Cada elemento de interfaz de usuario con el que el usuario puede interactuar debe ser accesible mediante el teclado, así como exponerse a través de una interfaz de programación de aplicaciones (API) de accesibilidad. Se recomienda usar Automatización de la interfaz de usuario, el nuevo marco de accesibilidad para todas las versiones de Microsoft Windows que admiten Windows Presentation Foundation (WPF). Automatización de la interfaz de usuario proporciona acceso mediante programación a la mayoría de los elementos del escritorio, lo que permite que los productos de tecnología de asistencia, como los lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios y manipulen la interfaz de usuario por medios distintos de la entrada estándar (por ejemplo, hablando en lugar de manipular el mouse o el teclado). Para obtener más información, vea el [Automatización de la interfaz de usuario información general.](/dotnet/framework/ui-automation/ui-automation-overview)

Tenga en cuenta que aunque los lectores de pantalla son una tecnología de asistencia muy importante, también hay otros. Para obtener más información sobre la gama de tecnologías disponibles, vea [Tipos de productos de tecnología de asistencia](https://www.microsoft.com/enable/at/types.aspx).

**Reconocimiento de voz**

El reconocimiento de voz es una característica de accesibilidad de Windows que permite a los usuarios interactuar con sus equipos por voz, lo que reduce la necesidad de interacción motora con el mouse o el teclado. Los usuarios pueden dictar documentos y correo electrónico, usar comandos de voz para iniciar y cambiar entre programas, controlar el sistema operativo e incluso rellenar formularios en la Web.

**Lupa**

La ampliación ayuda a los usuarios con baja visión mediante la ampliación de elementos en pantalla de 2 a 16 veces el original. Los usuarios pueden establecer esta característica para realizar un seguimiento del mouse (para ver una versión ampliada de lo que apunta el mouse), el teclado (para ver el área donde se mueve el puntero al tabular) o la edición de texto (para ver lo que escriben).

**Configuraciones visuales y esquemas de color**

Además de aumentar el tamaño de la pantalla, los usuarios [](glossary.md) con discapacidad visual pueden beneficiarse de la configuración del sistema, como el modo de contraste alto o la capacidad de personalizar esquemas de color de fondo y primer plano.

**Narrador**

Narrador es un lector de pantalla de escala vertical en Windows que permite a los usuarios escuchar el texto en pantalla y los elementos de la interfaz de usuario leídos en voz alta, incluso algunos eventos (incluidos los mensajes de error) que se suceden de forma escerámica. El usuario puede escuchar los menús narrador sin salir de la ventana activa.

![captura de pantalla del cuadro de diálogo "narrador de Microsoft" ](images/inter-accessibility-image2.png)

Los usuarios pueden personalizar la medida en que se usa Microsoft Narrador.

**Teclado en pantalla**

Para los usuarios que tienen dificultades con los teclados físicos y necesitan usar un dispositivo de entrada alternativo, como un conmutador, los teclados en pantalla son una necesidad. Los usuarios pueden seleccionar claves con el mouse u otro dispositivo que señala, un pequeño grupo de teclas o solo una tecla, en función de cómo configure el teclado en pantalla.

**Teclas del mouse**

Con las teclas del mouse habilitadas, los usuarios que prefieran el teclado pueden usar las teclas de dirección del teclado numérico para mover el puntero del mouse.

Para obtener una lista completa de las características de accesibilidad, vea [Accesibilidad en Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) en el sitio web de Microsoft.

### <a name="keyboard-based-navigation"></a>Navegación basada en teclado

La tecla Tab, las teclas de dirección, la barra espaciadoa y la tecla Entrar son importantes para la navegación basada en teclado. Al presionar Tabulación, el foco [de](glossary.md) entrada se desplaza a través de los distintos grupos de controles y al presionar las teclas de dirección se mueve dentro de un control o entre los controles de un grupo. Presionar la barra espaciador es lo mismo que hacer clic en el control con el foco de entrada, mientras que presionar Entrar es lo mismo que hacer clic en el botón de comando predeterminado o en el vínculo de comando, independientemente del foco de entrada.

![captura de pantalla del cuadro de diálogo "papelera de reciclaje vacía" ](images/inter-accessibility-image3.png)

En este ejemplo, los usuarios pueden presionar Tab hasta que la opción deseada tenga el foco de entrada y, a continuación, presionar Entrar para abrir el objeto.

### <a name="access-keys"></a>Claves de acceso

Las claves de acceso permiten a los usuarios elegir opciones e iniciar comandos directamente sin tener que ir primero al control. Las claves de acceso se indican mediante la subrayado de uno de los caracteres de la etiqueta de cada control. A continuación, los usuarios activan la opción o el comando presionando la tecla Alt junto con el carácter subrayado. Las claves de acceso no distinguen mayúsculas de minúsculas.

![captura de pantalla del menú de archivos y las claves de acceso ](images/inter-accessibility-image4.png)

En este ejemplo, al presionar Alt+O se activa el comando Abrir.

La elección de claves de acceso lógico para los controles normalmente no supone ninguna dificultad; Cuanto más controles haya en una ventana, mayor será la posibilidad de que se quedas sin opciones de clave de acceso. En este caso, asigne claves de acceso a grupos de control en lugar de a cada uno individual.

![captura de pantalla de grupos de control y claves de acceso ](images/inter-accessibility-image5.png)

En este ejemplo, las claves de acceso se asignan a grupos de controles, en lugar de a controles individuales.

Las claves de acceso suelen confundirse con las teclas de método abreviado, pero las teclas de método abreviado se asignan de forma diferente a las claves de acceso y tienen objetivos diferentes. Por ejemplo, las teclas de método abreviado usan secuencias de teclas Ctrl y Función y están diseñadas principalmente como un acceso directo para usuarios avanzados en lugar de para accesibilidad.

Para obtener más información, vea [Teclado](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Diseño de accesibilidad: tres procedimientos fundamentales

Los programas accesibles ayudan a todos los usuarios de alguna manera porque los objetivos de accesibilidad y facilidad de uso se superponen. Por ejemplo, las características diseñadas para hacer que los usuarios avanzados sea lo más eficaz posible también benefician a los usuarios que prefieren usar el teclado debido a una discapacidad de la elasticidad.

Tres procedimientos fundamentales le ayudarán con un diseño accesible: permitir un grado de flexibilidad en la interfaz de usuario, permitir que el respetar las necesidades y preferencias del usuario desempeñan un papel importante en las decisiones de diseño y proporcionar acceso mediante programación a la interfaz de usuario.

**Proporcionar una interfaz de usuario flexible**

El diseño accesible se trata, al menos en parte, de proporcionar opciones a los usuarios. No es una matriz de opciones frustrante y creciente, sino un número limitado de opciones que anticipan de forma inteligente las necesidades de los usuarios. "¿No le gusta navegar por el mouse? Aquí, puede hacer lo mismo solo con el teclado. ¿No le gustan los teclados físicos? Este es un virtual que puede usar en pantalla".

Por ejemplo, proporcione flexibilidad mediante:

-   Proporcionar equivalentes seleccionables por el usuario para elementos que no son de texto (por ejemplo, texto alternativo para gráficos y títulos para audio).

    ![captura de pantalla del botón de inicio de sesión](images/inter-accessibility-image6.png)

    ![captura de pantalla del texto alternativo para el botón de inicio de sesión](images/inter-accessibility-image7.png)

    Los usuarios que han elegido no representar gráficos deben ver texto alternativo en su lugar, describiendo lo que hace el control y cómo interactuar con él.

-   Proporcionar alternativas al color (por ejemplo, la diferenciación de iconos o el uso de sonidos).

    ![captura de pantalla de iconos en tonos de gris (escala de grises) ](images/inter-accessibility-image8.png)

    En este ejemplo, los iconos estándar se distinguen fácilmente en función de sus diseños.

-   Garantizar el acceso al teclado (por ejemplo, una tabulación para cada control interactivo) para que los usuarios puedan realizar las mismas cosas en el programa con el mouse o el teclado.
-   Asegurarse de que el programa ofrece buenas opciones de contraste de color para los usuarios. Windows proporciona una opción de contraste alto, pero realmente está diseñada para ser una solución para discapacidades visuales graves. Otras opciones de contraste sirven mejor a los usuarios con discapacidades auditivas, como la visión baja y la cegura del color.
-   Asegurarse de que los usuarios tienen una manera de ajustar el tamaño del texto en la interfaz de usuario del programa (por ejemplo, a través de un control deslizante o un cuadro desplegable para el tamaño de fuente). Si es posible, admite el modo de puntos altos por pulgada (ppp).
-   Asegurarse de que el programa es multimodal, lo que significa que si algunos no pueden acceder al modo principal del programa, estos usuarios tienen una manera de solucionar el problema. Por ejemplo, cuando se muestra la animación, la información debe mostrarse en al menos un modo de presentación no animado a la opción del usuario.

Las interfaces multimodales y la navegación flexible ofrecen esencialmente al usuario la arquitectura de redundancia de la información. La redundancia a veces tiene connotaciones negativas; en el texto de la interfaz de usuario, por ejemplo, se recomienda quitar la redundancia para simplificar la experiencia de lectura. Pero en el contexto de accesibilidad, la redundancia connota experiencias y mecanismos positivos y seguros para errores.

**Respetar a los usuarios**

Respetando como principio general, el principio rector es fundamental para diseñar programas accesibles. Incluso como ejercicio intelectual, imagine lo que debe ser encontrarse con el programa como un usuario deshabilitado. Tómese el tiempo para probar las pantallas de la interfaz de usuario en modo de contraste alto y en varias resoluciones, para asegurarse de que la experiencia es buena para los usuarios con discapacidades visuales. Pruebe la accesibilidad del teclado seleccionando la casilla Subrayado de **métodos abreviados** de teclado y teclas de acceso en el elemento Centro de accesibilidad Panel de control (para que las teclas de acceso estén siempre visibles). Incluso puede ir más allá de pruebas rigurosas mediante la contratación de desarrolladores y diseñadores que tienen una aptitud natural para empatía con otros usuarios.

También debe demostrar el respecto por:

-   Usar la configuración de todo el sistema (por ejemplo, Color del sistema) en lugar de la configuración de los ajustes para el programa en particular. Respete no solo los parámetros que los usuarios han seleccionado específicamente para interactuar con sus programas, sino también las características de accesibilidad integradas en el sistema operativo que el usuario quiera en vigor independientemente del programa que use. Para obtener más información, vea [About Windows Accessibility Features](/previous-versions//ms695605(v=vs.85)).
-   Prefiere los controles comunes a los controles personalizados, ya que los controles comunes ya han implementado Windows API de accesibilidad.
-   Documentar todas las opciones y características de accesibilidad (por ejemplo, todos los métodos abreviados de teclado). Los usuarios con discapacidades están muy motivadas para detectar características de accesibilidad y, a menudo, esperan que se repile información completa en la Ayuda.
-   Creación de documentación accesible en formatos accesibles. Por lo tanto, la propia documentación debe cumplir las mismas reglas de accesibilidad que la interfaz de usuario principal, incluida la capacidad de ampliar el tamaño de fuente, el uso de texto alternativo para gráficos y la arquitectura de información redundante (por ejemplo, usando la codificación de colores solo como complemento al texto).

En los productos de software, el respecto a los usuarios puede manifestarse en la facilidad de uso y la investigación del mercado, en la documentación y los servicios de soporte técnico eficaces y, por supuesto, en las decisiones de diseño. Por ejemplo, piense de nuevo en términos de diseño para usuarios avanzados: ¿está colocando esa característica nueva de vanguardia en porque la desea o porque sabe que los usuarios avanzados la han pedido? El último caso indica que el proceso de toma de decisiones de diseño está bien informado por el valor de respecto.

**Proporcionar acceso mediante programación**

Proporcionar acceso mediante programación a la interfaz de usuario es esencial para que las tecnologías de asistencia (como lectores de pantalla, dispositivos de entrada alternativos y programas de reconocimiento de voz) interpreten la pantalla correctamente para sus usuarios. Al crear un "mapa" de cada pantalla de interfaz de usuario en el programa, se hace que esté disponible para los usuarios de tecnologías de asistencia.

Para hacerlo bien, haga lo siguiente:

-   Habilitar el acceso mediante programación a todos los elementos y texto de la interfaz de usuario (por ejemplo, mediante Active Accessibility interfaz COM, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Colocación de nombres (o títulos) y descripciones en objetos de interfaz de usuario, marcos y páginas (por ejemplo, mediante la [**propiedad IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name).
-   Asegurarse de que todas las actividades de la interfaz de usuario desencadenan eventos mediante programación (por ejemplo, eventos de foco para todas las actividades de la interfaz de usuario que implican el movimiento del foco).

**Si solo hace cuatro cosas...**

1.  Asegúrese de que todos los usuarios puedan aprovechar todo el potencial del programa.
2.  Piense en la accesibilidad como una oportunidad para resolver problemas creativos y como otro medio para aumentar la satisfacción general del usuario.
3.  Respetar la configuración del sistema.
4.  Use controles comunes siempre que sea posible.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No interrumpa ni deshabilite las características activadas del sistema operativo u otros productos que se identifiquen como características de accesibilidad.** Para identificar estas características, consulte la documentación del sistema operativo o el producto en cuestión.
-   **No fuerce a los usuarios a interactuar con el programa como la ventana superior de la pantalla.** Si se requiere una función o una ventana continuamente para que los usuarios realicen una tarea, esa ventana siempre debe permanecer visible, si el usuario así lo decide, independientemente de su posición con respecto a otras ventanas. Por ejemplo, si el usuario tiene un teclado móvil en pantalla que está encima de todas las demás ventanas para que esté visible en todo momento, el programa nunca debe ocultarlo colocando obligatoriamente en la parte superior del pedido [Z](glossary.md).
-   **Use colores del sistema, fuentes y controles comunes siempre que sea posible.** Al hacerlo, se reduce significativamente el número de problemas de accesibilidad que encuentran los usuarios.

### <a name="addressing-particular-impairments"></a>Abordar discapacidades concretas

**Visual**

-   **No confíe nunca en el color por sí solo para transmitir significado.** Use el color solo como medio de reforzar el significado proporcionado por texto, diseño, ubicación o sonido.

    ![captura de pantalla del icono rojo de icono de icono e información sobre herramientas ](images/inter-accessibility-image9.png)

    El método principal de comunicación de este ejemplo es el texto conciso de información sobre herramientas. El uso del color ayuda a comunicar el significado, pero es secundario.

-   **Use información de texto alternativo (alt) para describir gráficos.**
-   **No use texto en gráficos.** Los usuarios con discapacidades visuales pueden tener gráficos desactivados (por ejemplo, en un explorador web) o simplemente no ver o buscar texto colocado en los gráficos.
-   **Asegúrese de que los** cuadros de diálogo y las ventanas tienen nombres significativos para que un usuario que escucha en lugar de ver la pantalla (por ejemplo, mediante un lector de pantalla) obtiene la información contextual adecuada.
-   Respete la configuración del usuario para la presentación **visual** mediante la obtención siempre de tipos de fuente, tamaños y colores, tamaños y colores, tamaños de elementos de visualización Windows y opciones de configuración del sistema de las API Theme y GetSystemMetrics.
-   **Mantenga el texto del globo conciso** para que sea más fácil de leer y minimice la interrupción de los lectores de pantalla.

    ![captura de pantalla de globo que indica los límites de código pin ](images/inter-accessibility-image10.png)

    Aunque los globos pueden usar texto adicional del cuerpo si es necesario, en este ejemplo se muestra que, a veces, el texto del título por sí solo logra el mismo objetivo de una manera más económica y accesible.

**Oído**

-   **No confíe nunca en el sonido por sí solo para transmitir significado.** Use sonido solo como medio de reforzar el significado proporcionado por texto, diseño, ubicación o color.
-   **Permitir a los usuarios controlar el volumen de salida de audio.** Use el Windows volumen Mixer para este propósito. Para obtener más información, vea [Sonido](vis-sound.md).
-   El objetivo es que el sonido del programa se produzca en un intervalo entre **500 Hz y 3000 Hz** o que el usuario pueda ajustarlo fácilmente en ese intervalo. Es más probable que las personas con discapacidad auditiva detecten sonidos de este intervalo.

**Destreza**

-   **Haga que los valores de tiempo de espera de la interfaz de usuario sea relativos a GetDoubleClickTime() en lugar de usar tiempos absolutos.** Al hacerlo, se ajustan los tiempos de espera a la velocidad del usuario.
-   **Asigne teclas de acceso a todos** los elementos de menú para que los usuarios que prefieran trabajar con el teclado tengan la misma capacidad de navegar por el programa que los usuarios que trabajan con el mouse.
-   **No haga doble clic y arrastre la única manera de realizar una acción.** Estos pueden ser movimientos difíciles para algunos usuarios.
-   **No quite las barras de menús del programa.** Las barras de menús son más fáciles que las barras de herramientas a las que tienen acceso los usuarios del teclado. Si no desea que la barra de menús esté visible de forma predeterminada, oculte en su lugar.
-   **Haga que la Ayuda sea accesible desde el teclado proporcionando tabulaciones para los botones y vínculos de Ayuda.**
-   **Para mejorar el conocimiento de las asignaciones de claves de acceso en el programa, puede mostrarlas en todo momento.** En Panel de control, vaya a la Centro de accesibilidad y haga clic en Facilitar el uso **del teclado**; a continuación, active **la casilla Subrayado de los métodos abreviados de** teclado y las teclas de acceso.

**Cognitivo**

-   **Use la divulgación progresiva** para ocultar la complejidad.

    ![captura de pantalla de botones de división con triángulos hacia abajo ](images/inter-accessibility-image11.png)

    En estos ejemplos, las opciones disponibles en el botón de comando están ocultas de forma predeterminada y los usuarios pueden elegir ver las opciones aprovechando los controles de divulgación progresiva.

-   **Use iconos, barras de herramientas y otras** ayuda visuales para reducir la carga cognitiva de lectura de texto.
-   Siempre que sea posible, proporcione funcionalidad de autocompletar en cuadros de texto y listas desplegables **editables** para que los usuarios no tengan que escribir el nombre completo de comandos, nombres de archivo o opciones similares de un conjunto limitado de opciones. Esto reduce la carga cognitiva para todos los usuarios y reduce la cantidad de escritura para los usuarios para los que la ortografía o la escritura son difíciles, lentas o difíciles.
-   **Demostrar conceptos difíciles en la Ayuda mediante la inclusión de tutoriales y animaciones.** Tenga en cuenta que las animaciones pueden ser difíciles para los usuarios con dificultades auditivas y, por tanto, solo se deben usar cuando sea necesario.

**Asimiento**

-   **No use texto parpadeante o parpadeante, objetos u otros elementos que tengan una frecuencia de parpadeo o parpadeo en el intervalo entre 2 y 55 Hz.**
-   **Limitar el uso de animaciones.** Algunos usuarios son especialmente sensibles al movimiento de la pantalla, especialmente en la periferia de su campo visual. Si usa animación para llamar la atención sobre algo, asegúrese de que la atención se merece y merece la pena interrumpir al usuario.

**Voz o idioma**

-   **Organice y escriba texto claro, conciso y fácil de entender.** Las pruebas de facilidad de uso muestran que la revelación de información clave al final de una frase mejora la comprensión. Para obtener más instrucciones, [vea Estilo y tono.](text-style-tone.md)

**Incorrecto:**

¿Tres son los dígitos siguientes?

Haga clic en Aceptar para comenzar.

**Correcto:**

¿Es el siguiente dígito tres?

Para comenzar, haga clic en Aceptar.

### <a name="access-keys"></a>Claves de acceso

-   **Prefiere caracteres con anchos anchos anchos,** como w, m y letras mayúsculas.
-   **Prefiere una consonante distintiva o una voto,** como "x" en "Exit".
-   **Evite usar caracteres que hagan que el subrayado** sea difícil de ver, como (de más problemático a menos problemático):
    -   Caracteres de solo un píxel de ancho, como i y l.
    -   Caracteres con descendientes, como g, j, p, q e y.
    -   Caracteres junto a una letra con un descendiente.

### <a name="menu-access-keys"></a>Teclas de acceso de menú

-   **Asigne claves de acceso a todos los elementos de menú.** Ninguna excepción.
-   **Para los elementos de menú dinámicos (por ejemplo, los archivos usados recientemente), asigne claves de acceso numéricamente.**

    ![captura de pantalla del menú abierto con archivos usados recientemente ](images/inter-accessibility-image12.png)

    En este ejemplo, el programa Paint en Windows asigna claves de acceso numéricas a los archivos usados recientemente.

-   **Asigne claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilitar la tarea de encontrar las claves de acceso:**
    -   Para los elementos de menú usados con más frecuencia, elija caracteres al principio de la primera o segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   Para los elementos de menú usados con menos frecuencia, elija letras que sean una consonante distintiva o una voz en la etiqueta.

### <a name="dialog-box-access-keys"></a>Claves de acceso del cuadro de diálogo

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o sus etiquetas.** [Los cuadros de texto de solo](ctrl-text-boxes.md) lectura son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto), por lo que se benefician de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones Aceptar, Cancelar y Cerrar.** Escriba y Esc se usan para sus claves de acceso. Sin embargo, asigne siempre una clave de acceso a un control que significa Aceptar o Cancelar, pero tiene una etiqueta diferente.

        ![captura de pantalla de los controles con claves de acceso asignadas ](images/inter-accessibility-image13.png)

        En este ejemplo, el botón de confirmación positiva tiene asignada una clave de acceso.

-   **Etiquetas de grupo.** Normalmente, a los controles individuales de un grupo se les asignan claves de acceso, por lo que la etiqueta de grupo no necesita ninguna. Sin embargo, asigne una clave de acceso a la etiqueta de grupo y no a los controles individuales si hay escasez de claves de acceso.
-   **Botones genéricos de Ayuda,** a los que se accede con F1.
-   **Vincular etiquetas.** A menudo hay demasiados vínculos para asignar claves de acceso únicas y los caracteres de subrayado de vínculo ocultan los caracteres de subrayado de la clave de acceso. Haga que los usuarios accedan a los vínculos con la tecla Tab en su lugar.
-   **Nombres de tabulación.** Las pestañas se ciclos mediante Ctrl+Tab y Ctrl+Mayús+Tab.
-   **Botones de exploración etiquetados como "...".** No se pueden asignar claves de acceso de forma única.
-   **Controles sin etiquetar, como** controles de giro, botones de comandos gráficos y controles de divulgación progresiva sin etiquetar.
-   **Texto estático sin etiqueta o etiquetas para controles que no son interactivos,** como barras de progreso.
-   **Asigne primero las claves de acceso del botón de confirmación para asegurarse de que tienen las asignaciones de claves estándar.** Si no hay una asignación de clave estándar, use la primera letra de la primera palabra. Por ejemplo, la clave de acceso para los botones de confirmación Sí y No siempre debe ser "Y" y "N", independientemente de los demás controles del cuadro de diálogo.
-   **En el caso de los botones de confirmación negativos (distintos de Cancelar) con la frase "No", asigne la clave de acceso a "n" en "No lo haga".** Si no se frasea como "No", use la asignación de clave de acceso estándar o asigne la primera letra de la primera palabra. Al hacerlo, todos los elementos No y No tienen una clave de acceso coherente.
-   Para facilitar la búsqueda de claves de acceso, asigne las claves de acceso a un carácter que aparezca al principio de la **etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.

Para obtener más instrucciones y ejemplos, vea [Teclado](inter-keyboard.md).

## <a name="text"></a>Texto

-   **Use dos puntos al final de las etiquetas de control externo.** Algunas tecnologías de asistencia buscan dos puntos para identificar las etiquetas de control.
-   **Coloque las etiquetas de forma coherente con respecto a los elementos que están etiquetando.** Esto ayuda a la tecnología de asistencia a asociar correctamente las etiquetas a sus controles correspondientes y ayuda a los usuarios de los ampliadores de pantalla a saber dónde buscar una etiqueta o un control.

    ![captura de pantalla de etiquetas colocadas de forma coherente ](images/inter-accessibility-image14.png)

    En este ejemplo, las etiquetas de cada una de las listas desplegables se colocan de forma coherente y usan dos puntos.

-   **Limite el texto alternativo a 150 caracteres como máximo.** Describa la acción para activar el control (por ejemplo, hacer clic, hacer clic con el botón derecho, y así sucesivamente) y, a continuación, describir la función del control.

    **Aceptable:**

    Botón.

    Azul azul.

    **Mejor:**

    Haga clic para iniciar sesión en su cuenta.

    Foto de distancias lejanas en las que se muestra cómo se atenuan los colores a lo largo de la distancia.

-   **No use texto para dibujar líneas, cuadros u otros símbolos gráficos.** Los caracteres usados de esta manera pueden confundir a los usuarios de los lectores de pantalla. Por ejemplo, el software de lector de pantalla lee un cuadro dibujado con la letra "X" alrededor de un área de texto como "X X X X X X" en la primera línea, seguido de "X" y el contenido y "X".

## <a name="documentation"></a>Documentación

-   Documente todas las opciones y características de accesibilidad (por ejemplo, todos los métodos abreviados de teclado).
-   Cree documentación accesible en formatos accesibles. Por lo tanto, la propia documentación debe cumplir las mismas reglas de accesibilidad que la interfaz de usuario principal.
-   Consulte teclas de acceso, no teclas de método abreviado (que tienen un significado y uso diferentes), teclas mnemotécnicas o aceleradores.
-   En general, consulte a una persona con algún tipo de discapacidad, no a una persona con discapacidad. Considere primero a la persona, no a la etiqueta.



| Use estos términos           | En lugar de                                                        |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| Tiene una elasticidad limitada, tiene discapacidades de movimiento.<br/>     | Paralizado, desasistido<br/>                                                        |
| Sin discapacidades<br/>                               | Normal, con forma, correcto<br/>                                          |
| Personas con una mano que escriben con una mano<br/>          | Con una sola mano <br/>                                                        |
| Personas con discapacidades<br/>                           | Las personas deshabilitadas, las personas con discapacidad, las personas con discapacidades, las personas con discapacidad<br/> |
| Discapacidades cognitivas, discapacidades de desarrollo<br/> |                                                                                  |



 


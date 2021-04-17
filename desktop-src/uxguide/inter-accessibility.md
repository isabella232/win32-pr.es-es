---
title: Accesibilidad (conceptos básicos del diseño)
description: El diseño de software para accesibilidad significa garantizar que los programas y la funcionalidad están disponibles fácilmente para la gama más amplia de usuarios, incluidos aquellos con discapacidades e impedimentos.
ms.assetid: df6947ec-6a1d-4645-ae3e-863839c32588
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 559d4c18e59c63a428aca1086e57f2ba4e62ae6f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552245"
---
# <a name="accessibility-design-basics"></a>Accesibilidad (conceptos básicos del diseño)

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El diseño de software para accesibilidad significa garantizar que los programas y la funcionalidad están disponibles fácilmente para la gama más amplia de usuarios, incluidos aquellos con discapacidades e impedimentos.

El número de usuarios que las características de accesibilidad pueden ayudar puede sorprenderle; por ejemplo, en el Estados Unidos, las encuestas han demostrado que más de la mitad de todos los usuarios del equipo experimentan dificultades o discapacidades relacionadas con la accesibilidad, y es probable que se beneficien del uso de la tecnología accesible. Además, el diseño de software con la flexibilidad y inclusiveness que son los sellos de accesibilidad a menudo da como resultado una mejora general del uso y la satisfacción del cliente.

![captura de pantalla del cuadro de diálogo ' centro de accesibilidad ' ](images/inter-accessibility-image1.png)

El centro de accesibilidad, disponible en el panel de control, proporciona una ubicación central en la que los usuarios pueden elegir y personalizar las características de accesibilidad que desean.

**Nota:** Las instrucciones relacionadas con el [teclado](inter-keyboard.md), el [mouse](inter-mouse.md), el [color](vis-color.md)y el [sonido](vis-sound.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

Muchos factores físicos, perceptuales e cognitivos entran en juego cuando los usuarios interactúan con el hardware y el software del equipo. Antes de tener en cuenta las maneras de mejorar la accesibilidad de las características del programa, ayuda a obtener información sobre los tipos de discapacidad y las discapacidades, y algunas de las tecnologías de asistencia con las que estos usuarios pueden estar trabajando mientras interactúan con los equipos.

### <a name="types-of-impairments"></a>Tipos de discapacidades

En la tabla siguiente se describen las discapacidades y los problemas comunes de los usuarios, y se enumeran algunas de las soluciones más importantes que se usan para que los equipos sean más accesibles.



|                               |                                                                                                                                                                                                         |                                                                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Discapacidad**<br/>     | **Descripción**<br/>                                                                                                                                                                              | **Soluciones**<br/>                                                                                                                                                              |
| Elemento visual<br/>             | Intervalos desde leves (que afectan al 17 por ciento de los usuarios) a graves (que afectan al 9 por ciento de los usuarios).<br/>                                                                                                   | Ampliación, colores y contraste personalizables; Utilidades de Braille; lectores de pantalla.<br/>                                                                                       |
| Oído<br/>            | Intervalos desde leves (que afectan al 18 por ciento de los usuarios) a graves (que afectan al 2 por ciento de los usuarios).<br/>                                                                                                   | Redundancia de la información: sonido que se usa solo como complemento para el texto o la comunicación visual.<br/>                                                                                     |
| Destreza manual<br/>          | Intervalos desde leves (que afectan al 19 por ciento de los usuarios) a graves (que afectan al 5 por ciento de los usuarios). Este incumplimiento suele tener dificultades para realizar determinados conocimientos del motor con el teclado o el mouse.<br/> | Redundancia del método de entrada: características de programa a las que tienen acceso los equivalentes del mouse o del teclado.<br/>                                                                                       |
| Cognitivo<br/>          | Incluye impedimentos de memoria y diferencias perceptuales. Afecta al 16 por ciento de los usuarios.<br/>                                                                                                         | Interfaz de usuario (UI) altamente personalizable; uso de la [divulgación progresiva](ctrl-progressive-disclosure-controls.md) para ocultar la complejidad; uso de iconos y otras ayudas visuales.<br/> |
| Toma<br/>            | Incluye sensibilidad visual al movimiento y el parpadeo.<br/>                                                                                                                                        | Enfoque conservador para las interfaces de modulating, como el uso de animaciones; evitar el parpadeo de la pantalla en el intervalo comprendido entre 2 hercios (Hz) y 55 Hz.<br/>                        |
| Voz o lenguaje<br/> | Incluye las dificultades de la dislexia y la comunicación oral.<br/>                                                                                                                                       | Utilidades de revisión ortográfica y de comprobación gramatical; tecnología de reconocimiento de voz y de texto a voz.<br/>                                                                                 |



 

Para obtener más instrucciones sobre cómo ayudar a los usuarios con estas discapacidades, consulte [abordar determinados problemas](#addressing-particular-impairments) más adelante en este artículo.

### <a name="types-of-assistive-technologies-and-accessibility-features"></a>Tipos de tecnologías de asistencia y características de accesibilidad

**Lectores de pantalla**

Un lector de pantalla permite que los usuarios con discapacidades visuales o discapacitaciones naveguen por una interfaz de usuario mediante la transformación de objetos visuales en el audio. Por lo tanto, el texto de la interfaz de usuario, los controles, los menús, las barras de herramientas, los gráficos y otros elementos de pantalla se pronuncian por la voz en equipo del lector de pantalla. Para crear un programa optimizado para la tecnología de asistencia del lector de pantalla, debe planear el modo en que el lector de pantalla identificará cada elemento de la interfaz de usuario.

Cada elemento de la interfaz de usuario con el que el usuario puede interactuar debe ser accesible desde el teclado y exponerse a través de una interfaz de programación de aplicaciones (API) de accesibilidad. Se recomienda usar la automatización de la interfaz de usuario, el nuevo marco de accesibilidad para todas las versiones de Microsoft Windows que admiten Windows Presentation Foundation (WPF). La automatización de la interfaz de usuario proporciona acceso mediante programación a la mayoría de los elementos del escritorio, lo que permite que los productos de tecnología de asistencia, como lectores de pantalla, proporcionen información sobre la interfaz de usuario a los usuarios y manipulen la interfaz de usuario de forma distinta a la entrada estándar (por ejemplo, hablando en lugar de o además de manipular el mouse o teclado). Para obtener más información, vea [información general sobre la automatización](/dotnet/framework/ui-automation/ui-automation-overview)de la interfaz de usuario.

Tenga en cuenta que, aunque los lectores de pantalla son una tecnología de asistencia muy importante, también hay otros. Para obtener más información sobre el abanico de tecnologías disponibles, consulte [tipos de productos de tecnología de asistencia](https://www.microsoft.com/enable/at/types.aspx).

**Reconocimiento de voz**

El reconocimiento de voz es una característica de accesibilidad de Windows que permite a los usuarios interactuar con sus equipos por voz, lo que reduce la necesidad de interacción del motor con el mouse o el teclado. Los usuarios pueden dictar documentos y correo electrónico, usar comandos de voz para iniciar y cambiar entre programas, controlar el sistema operativo e incluso rellenar formularios en la Web.

**Lupa**

La ampliación ayuda a los usuarios con deficiencias visuales al ampliar los elementos de la pantalla en cualquier parte de 2 a 16 veces la original. Los usuarios pueden establecer esta característica para realizar el seguimiento del mouse (para ver una versión ampliada de lo que señala el mouse), el teclado (para ver el área donde se mueve el puntero al tabular) o la edición de texto (para ver lo que están escribiendo).

**Configuración visual y combinaciones de colores**

Además de aumentar el tamaño de las cosas en la pantalla, los usuarios con discapacidades visuales pueden beneficiarse de la configuración del sistema, como el [modo de contraste alto](glossary.md) , o la capacidad de personalizar los esquemas de color de fondo y de primer plano.

**Narrador**

El narrador es un lector de pantalla reducido en Windows que permite a los usuarios oír texto en pantalla y elementos de la interfaz de usuario leídos en voz alta, incluso algunos eventos (incluidos los mensajes de error) que se producen espontáneamente. El usuario puede oír los menús del narrador sin cerrar la ventana activa.

![captura de pantalla del cuadro de diálogo "narrador de Microsoft" ](images/inter-accessibility-image2.png)

Los usuarios pueden personalizar la medida en la que se usa Microsoft narrador.

**Teclado en pantalla**

Para los usuarios que tienen dificultades con los teclados físicos y necesitan usar un dispositivo de entrada alternativo, como un conmutador, los teclados en pantalla son necesarios. Los usuarios pueden seleccionar teclas con el mouse u otro dispositivo señalador, un pequeño grupo de claves o simplemente una clave, en función de cómo se configure el teclado en pantalla.

**Teclas del mouse**

Con las teclas de mouse habilitadas, los usuarios que prefieren el teclado pueden utilizar las teclas de dirección del teclado numérico para desplace el puntero del mouse.

Para obtener una lista completa de las características de accesibilidad, vea [accesibilidad en Windows Vista](https://www.microsoft.com/enable/products/windowsvista/default.aspx) en el sitio web de Microsoft.

### <a name="keyboard-based-navigation"></a>Navegación basada en teclado

La tecla Tab, las teclas de dirección, la barra espaciadora y la tecla entrar son importantes para la navegación basada en teclado. Al presionar la tecla Tab, el [foco de entrada se centra](glossary.md) en los diferentes grupos de control y al presionar las teclas de dirección se mueve dentro de un control o entre los controles de un grupo. Presionar la barra espaciadora es lo mismo que hacer clic en el control con el foco de entrada, mientras que presionar entrar es igual que hacer clic en el botón de comando o vínculo de comando predeterminados, independientemente del foco de entrada.

![captura de pantalla del cuadro de diálogo ' Papelera de reciclaje vacía ' ](images/inter-accessibility-image3.png)

En este ejemplo, los usuarios pueden presionar TAB hasta que la opción deseada tenga el foco de entrada y, a continuación, presionar entrar para abrir el objeto.

### <a name="access-keys"></a>Claves de acceso

Las claves de acceso permiten a los usuarios elegir opciones e iniciar comandos directamente sin tener que desplazarse al control en primer lugar. Las teclas de acceso se indican mediante la subrayación de uno de los caracteres de la etiqueta de cada control. A continuación, los usuarios activan la opción o el comando presionando la tecla Alt junto con el carácter subrayado. Las claves de acceso no distinguen mayúsculas de minúsculas.

![captura de pantalla del menú Archivo y las teclas de acceso ](images/inter-accessibility-image4.png)

En este ejemplo, al presionar ALT + O se activa el comando abrir.

La elección de claves de acceso lógico para los controles normalmente no supone ninguna dificultad; sin embargo, cuanto más controles hay en una ventana, mayor será la posibilidad de quedarse sin opciones de clave de acceso. En este caso, asigne las claves de acceso a los grupos de control en lugar de a cada uno de ellos.

![captura de pantalla de grupos de control y claves de acceso ](images/inter-accessibility-image5.png)

En este ejemplo, las claves de acceso se asignan a los grupos de control, en lugar de a los controles individuales.

Las teclas de acceso suelen confundirse con las teclas de método abreviado, pero las teclas de método abreviado se asignan de forma diferente a las claves de acceso y tienen objetivos diferentes. Por ejemplo, las teclas de método abreviado usan secuencias de teclas Ctrl y de función y están pensadas principalmente como un acceso directo para usuarios avanzados en lugar de para accesibilidad.

Para obtener más información, consulte [teclado](inter-keyboard.md).

### <a name="designing-for-accessibility-three-fundamental-practices"></a>Diseño para accesibilidad: tres prácticas fundamentales

Los programas accesibles ayudan a todos los usuarios de alguna manera, ya que los objetivos de accesibilidad y facilidad de uso se superponen. Por ejemplo, las características diseñadas para que los usuarios avanzados sean lo más eficientes posible también pueden beneficiar a los usuarios que prefieren usar el teclado debido a la deficiencia de Dexterity.

Tres prácticas fundamentales le ayudarán con el diseño accesible: permitir un grado de flexibilidad en la interfaz de usuario, en el sentido de que las necesidades y las preferencias de los usuarios desempeñan un papel importante en las decisiones de diseño y proporcionan acceso mediante programación a la interfaz de usuario.

**Proporcionar una interfaz de usuario flexible**

El diseño accesible es, al menos en parte, de ofrecer opciones a los usuarios. No es una matriz de opciones de dizzying frustrante, sino un número limitado de opciones que prevén de forma inteligente las necesidades de los usuarios. "¿No le gusta navegar por el mouse? Aquí, puede hacer lo mismo con solo el teclado. ¿No le gustan los teclados físicos? A continuación se muestra una virtual que puede usar en pantalla ".

Por ejemplo, proporcione flexibilidad de la siguiente manera:

-   Proporcionar equivalentes seleccionables por el usuario para los elementos que no son de texto (por ejemplo, texto alternativo para gráficos y leyendas de audio).

    ![captura de pantalla del botón de inicio de sesión](images/inter-accessibility-image6.png)

    ![captura de pantalla del texto alternativo para el botón de inicio de sesión](images/inter-accessibility-image7.png)

    Los usuarios que han elegido no representar gráficos deberían ver texto alternativo en su lugar, lo que describe lo que hace el control y cómo interactuar con él.

-   Proporcionar alternativas al color (por ejemplo, diferenciación de iconos o uso de sonidos).

    ![captura de pantalla de iconos en tonalidades de gris (escala de grises) ](images/inter-accessibility-image8.png)

    En este ejemplo, los iconos estándar se pueden distinguir fácilmente en función de sus diseños.

-   Garantizar el acceso mediante teclado (por ejemplo, una tabulación para cada control interactivo) para que los usuarios puedan realizar las mismas acciones en el programa con el mouse o el teclado.
-   Asegurarse de que el programa ofrece opciones de contraste de color adecuadas para los usuarios. Windows proporciona una opción de contraste alto, pero realmente se ha diseñado para ser una solución para una deficiencia visual grave. Otras opciones de contraste mejoran a los usuarios con deficiencias leves, como la deficiencia de visión y la ceguera de color.
-   Asegurarse de que los usuarios tienen una manera de ajustar el tamaño del texto en la interfaz de usuario del programa (por ejemplo, a través de un control deslizante o un cuadro desplegable para el tamaño de fuente). Si es posible, admita el modo de alto puntos por pulgada (PPP).
-   Asegurarse de que el programa es multimodal, lo que significa que si el modo principal del programa es inaccesible para algunos, estos usuarios tienen una forma de solucionar el problema. Por ejemplo, cuando se muestra la animación, la información debe ser visible en al menos un modo de presentación no animada en la opción del usuario.

Esencialmente, las interfaces multimodal y la navegación flexible ofrecen al usuario la arquitectura de la redundancia de la información. A veces la redundancia tiene connotaciones negativas; en el texto de la interfaz de usuario, por ejemplo, se recomienda quitar la redundancia para optimizar la experiencia de lectura. Sin embargo, en el contexto de accesibilidad, la redundancia denota mecanismos positivos y de error.

**Respetar los usuarios**

En general, el principio de los GUID es fundamental para diseñar programas accesibles. Incluso como ejercicio intelectual, Imagine lo que debe hacer para que el programa se encuentre como un usuario que está deshabilitado. Tómese el tiempo de probar las pantallas de la interfaz de usuario en el modo de contraste alto y en distintas resoluciones para asegurarse de que la experiencia es una buena para los usuarios con discapacidades visuales. Para probar la accesibilidad del teclado, active la casilla **subrayar métodos abreviados de teclado y teclas de acceso** en el elemento del panel de control de facilidad de acceso (para que las claves de acceso siempre estén visibles). Incluso puede ir más allá de las rigurosas pruebas contratando a los desarrolladores y diseñadores que tienen una aptitud natural para empatía con otras personas con las que empezar.

También debe demostrar lo siguiente:

-   Usar la configuración de todo el sistema (por ejemplo, el color del sistema) en lugar de la configuración del programa en particular. Respete no solo los parámetros que los usuarios seleccionaron específicamente para interactuar con sus programas, sino también las características de accesibilidad integradas en el sistema operativo que el usuario desea en vigor independientemente del programa que estén usando. Para obtener más información, consulte [acerca de las características de accesibilidad de Windows](/previous-versions//ms695605(v=vs.85)).
-   La preferencia de controles comunes a los controles personalizados, ya que los controles comunes ya han implementado las API de accesibilidad de Windows.
-   Documentar todas las opciones y características de accesibilidad (por ejemplo, todos los métodos abreviados de teclado). Los usuarios con discapacidades tienen una gran motivación para detectar características de accesibilidad y, a menudo, esperan que se recopile información completa en la ayuda de.
-   Crear documentación accesible en formatos accesibles. Por lo tanto, la documentación en sí debe cumplir las mismas reglas de accesibilidad que la interfaz de usuario principal, incluida la capacidad de ampliar el tamaño de fuente, el uso de texto alternativo para los gráficos y la arquitectura de información redundante (por ejemplo, el uso de la codificación de colores solo como complemento del texto).

En los productos de software, el respeto de los usuarios puede manifestarse en la facilidad de uso y la investigación de mercado, en los servicios de soporte técnico de efficacious y en la documentación y en las decisiones de diseño. Por ejemplo, al pensar de nuevo en términos de diseño para usuarios avanzados: ¿va a colocar la nueva característica de vanguardia en porque lo desea o porque sabe que los usuarios avanzados la han solicitado? Este último caso indica que el proceso de toma de decisiones de diseño está bien informado por el valor de respeto.

**Proporcionar acceso mediante programación**

Proporcionar acceso mediante programación a la interfaz de usuario es esencial para que las tecnologías de asistencia (como lectores de pantalla, dispositivos de entrada alternativos y programas de reconocimiento de voz) interpreten la pantalla correctamente para sus usuarios. Al crear una "asignación" de cada pantalla de la interfaz de usuario en el programa, la pone a disposición de los usuarios de tecnologías de asistencia.

Hágalo bien:

-   Habilitar el acceso mediante programación a todos los elementos y texto de la interfaz de usuario (por ejemplo, mediante la interfaz COM Active Accessibility, [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)).
-   Colocar nombres (o títulos) y descripciones en objetos de interfaz de usuario, marcos y páginas (por ejemplo, mediante la propiedad [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Name).
-   Garantizar que todas las actividades de la interfaz de usuario desencadenan eventos mediante programación (por ejemplo, eventos de foco para todas las actividades de la interfaz de usuario que impliquen el movimiento del foco).

**Si solo hace cuatro cosas...**

1.  Asegúrese de que todos los usuarios pueden aprovechar todo el potencial de su programa.
2.  Piense en la accesibilidad como una oportunidad para la solución de problemas creativos y otro medio para aumentar la satisfacción general del usuario.
3.  Respete la configuración del sistema.
4.  Use controles comunes siempre que sea posible.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **No interrumpa ni deshabilite las características activadas del sistema operativo u otros productos que se identifican como características de accesibilidad.** Puede identificar estas características si hace referencia a la documentación del sistema operativo o del producto en cuestión.
-   **No obligue a los usuarios a interactuar con el programa en la ventana superior de la pantalla.** Si una función o una ventana se requiere continuamente para que los usuarios realicen una tarea, esa ventana siempre debe permanecer visible, si el usuario elige, independientemente de su posición en relación con otras ventanas. Por ejemplo, si el usuario tiene un teclado en pantalla movible que está en la parte superior de todas las demás ventanas, de modo que sea visible en todo momento, el programa nunca debe ocultarlo por ubicación obligatoria en la parte superior del [orden Z](glossary.md).
-   **Use colores del sistema, fuentes y controles comunes siempre que sea posible.** Al hacerlo, se reduce considerablemente el número de problemas de accesibilidad que se encuentran los usuarios.

### <a name="addressing-particular-impairments"></a>Solucionar discapacidades concretas

**Visual**

-   **Nunca se basa únicamente en el color para transmitir el significado.** Utilice el color únicamente como medio para reforzar el significado proporcionado por el texto, el diseño, la ubicación o el sonido.

    ![captura de pantalla del icono e información sobre herramientas de Communicator en rojo ](images/inter-accessibility-image9.png)

    El método principal de comunicación en este ejemplo es el texto conciso de la información sobre herramientas. El uso de color ayuda a comunicar el significado, pero es secundario.

-   **Use recuadros informativos de texto alternativo (Alt) para describir los gráficos.**
-   **No use texto en los gráficos.** Los usuarios con discapacidades visuales pueden tener los gráficos desactivados (por ejemplo, en un explorador Web) o simplemente no pueden ver o buscar el texto colocado en los gráficos.
-   **Asegúrese de que los cuadros de diálogo y las ventanas tengan nombres significativos,** de modo que un usuario que esté escuchando en lugar de ver la pantalla (por ejemplo, con un lector de pantalla) obtenga la información contextual adecuada.
-   **Respete la configuración del usuario para la presentación visual** obteniendo siempre los tipos de letra, los tamaños y los colores de fuente, los tamaños de los elementos de presentación de Windows y los valores de configuración del sistema del tema y las API de GetSystemMetrics.
-   **Mantenga un globo de texto conciso** para que sea más fácil leer y minimizar la interrupción de los lectores de pantalla.

    ![captura de pantalla de un globo que indica límites de código PIN ](images/inter-accessibility-image10.png)

    Aunque los globos pueden usar texto de cuerpo adicional si es necesario, este ejemplo muestra que a veces el texto del título solo consigue el mismo objetivo de una manera más económica y accesible.

**Oído**

-   **Nunca se basa en sonido solo para transmitir el significado.** Use el sonido solo como medio para reforzar el significado proporcionado por el texto, el diseño, la ubicación o el color.
-   **Permite a los usuarios controlar el volumen de salida de audio.** Use el mezclador de volumen de Windows para este fin. Para obtener más información, consulte [sonido](vis-sound.md).
-   **Destine el sonido del programa para que se produzca en un intervalo entre 500 Hz y 3000 Hz** , o que el usuario pueda ajustarlo fácilmente a ese intervalo. Es más probable que los sonidos de este intervalo sean detectables por personas con discapacidades auditivas.

**Destreza manual**

-   **Convierta los valores de tiempo de espera de la interfaz de usuario en relación con GetDoubleClickTime () en lugar de usar horas absolutas.** Al hacerlo, se ajustan los tiempos de espera a la velocidad del usuario.
-   **Asigne teclas de acceso a todos los elementos de menú** para que los usuarios que prefieren trabajar con el teclado tengan la misma capacidad de navegar por el programa que los usuarios que trabajan con el mouse.
-   **No haga doble clic y arrastre la única forma de realizar una acción.** Estos pueden ser movimientos difíciles de algunos usuarios.
-   **No quite las barras de menús del programa.** Las barras de menús son más fáciles que las barras de herramientas de los usuarios del teclado. Si no desea que la barra de menús esté visible de forma predeterminada, ocúltela en su lugar.
-   **Haga que la ayuda sea accesible desde el teclado proporcionando tabulaciones para botones y vínculos de ayuda.**
-   **Para mejorar el conocimiento de las asignaciones de teclas de acceso en el programa, puede mostrarlas en todo momento.** En el panel de control, vaya al centro de accesibilidad y haga clic en facilitar **el uso del teclado**; a continuación, active la casilla **subrayar métodos abreviados de teclado y teclas de acceso** .

**Cognitivo**

-   **Use la divulgación progresiva** para ocultar la complejidad.

    ![captura de pantalla de los botones de expansión con triángulos hacia abajo ](images/inter-accessibility-image11.png)

    En estos ejemplos, las opciones disponibles en el botón comando están ocultas de forma predeterminada y los usuarios pueden elegir ver las opciones aprovechando los controles de divulgación progresiva.

-   **Use iconos, barras de herramientas y otras ayudas visuales** para reducir la carga cognitiva de texto de lectura.
-   Siempre que sea posible, **proporcione funcionalidad de autocompletar en cuadros de texto y listas** desplegables editables, de modo que los usuarios no tengan que escribir el nombre completo de los comandos, los nombres de archivo o las opciones similares de un conjunto limitado de opciones. Esto reduce la carga cognitiva para todos los usuarios y reduce la cantidad de tipos de usuarios para los que la ortografía o la escritura son difíciles, lentas o complicadas.
-   **Demuestre conceptos difíciles de ayuda mediante la inclusión de tutoriales y animaciones.** Tenga en cuenta que las animaciones pueden ser difíciles de usar para los usuarios con discapacidades de secuestro y, por lo tanto, solo deben utilizarse cuando sea necesario.

**Toma**

-   **No use texto intermitente o intermitente, objetos u otros elementos que tengan una frecuencia de parpadeo o Flash en el intervalo entre 2-55 Hz.**
-   **Limite el uso de animaciones.** Algunos usuarios son especialmente sensibles al movimiento de la pantalla, especialmente en el periferia de su campo visual. Si usa la animación para atraer la atención a algo, asegúrese de que la atención se mantiene y es digno de interrumpir al usuario.

**Voz o lenguaje**

-   **Organice y escriba texto claro, conciso y fácil de comprender.** Las pruebas de facilidad de uso muestran que la desdoblación de la información de clave al final de una frase mejora la comprensión. Para obtener más instrucciones, consulte [estilo y tono](text-style-tone.md).

**Incorrecto:**

¿Es tres el siguiente dígito?

Haga clic en Aceptar para comenzar.

**Correcto:**

¿Es el siguiente dígito tres?

Para empezar, haga clic en Aceptar.

### <a name="access-keys"></a>Claves de acceso

-   **Prefiere caracteres con ancho ancho,** como w, m y mayúsculas.
-   **Prefiere una consonante distintiva o una vocal,** como "x" en "Exit".
-   **Evite el uso de caracteres que hagan que el subrayado sea difícil de ver,** como (desde la mayoría de los problemas a los menos problemáticos):
    -   Caracteres que solo tienen un píxel de ancho, como i y l.
    -   Caracteres con descendiente, como g, j, p, q e y.
    -   Caracteres situados junto a una letra con un descendiente.

### <a name="menu-access-keys"></a>Teclas de acceso de menú

-   **Asignar teclas de acceso a todos los elementos de menú.** Sin excepciones.
-   **Para los elementos de menú dinámicos (por ejemplo, los archivos usados recientemente), asigne claves de acceso numéricamente.**

    ![captura de pantalla del menú abrir con archivos usados recientemente ](images/inter-accessibility-image12.png)

    En este ejemplo, el programa Paint de Windows asigna claves de acceso numéricas a archivos usados recientemente.

-   **Asignar claves de acceso únicas dentro de un nivel de menú.** Puede reutilizar las claves de acceso en distintos niveles de menú.
-   **Facilite la búsqueda de las claves de acceso:**
    -   En el caso de los elementos de menú que se usan con más frecuencia, elija caracteres al principio de la primera o la segunda palabra de la etiqueta, preferiblemente el primer carácter.
    -   En el caso de los elementos de menú que se utilizan con menos frecuencia, seleccione las letras que son una consonante distintiva o una vocal en la etiqueta.

### <a name="dialog-box-access-keys"></a>Claves de acceso de cuadro de diálogo

-   **Siempre que sea posible, asigne claves de acceso únicas a todos los controles interactivos o a sus etiquetas.** Los [cuadros de texto de solo lectura](ctrl-text-boxes.md) son controles interactivos (porque los usuarios pueden desplazarlos y copiar texto) para que se beneficien de las claves de acceso. **No asigne claves de acceso a:**
    -   **Botones aceptar, cancelar y cerrar.** ENTER y ESC se usan para sus claves de acceso. Sin embargo, asigne siempre una tecla de acceso a un control que signifique aceptar o cancelar, pero que tenga una etiqueta diferente.

        ![captura de pantalla de controles con claves de acceso asignadas ](images/inter-accessibility-image13.png)

        En este ejemplo, el botón confirmación positivo tiene asignada una clave de acceso.

-   **Etiquetas de grupo.** Normalmente, los controles individuales dentro de un grupo tienen asignadas claves de acceso, por lo que la etiqueta de grupo no necesita una. Sin embargo, asigne una clave de acceso a la etiqueta del grupo y no a los controles individuales si hay una escasez de claves de acceso.
-   **Botones de ayuda genéricos,** a los que se tiene acceso con F1.
-   **Etiquetas de vínculo.** A menudo hay demasiados vínculos para asignar claves de acceso únicas, y los subrayados de vínculo ocultan los guiones bajos de la tecla de acceso. Haga que los usuarios tengan acceso a los vínculos con la tecla TAB en su lugar.
-   **Nombres de pestaña.** Las pestañas se recorren con Ctrl + Tab y Ctrl + Mayús + Tab.
-   **Botones examinar etiquetados como "...".** No se les pueden asignar claves de acceso de forma única.
-   **Controles sin etiqueta,** como controles de número, botones de comando gráficos y controles de divulgación progresiva sin etiquetar.
-   **Etiquetas o texto estático sin etiqueta para los controles que no son interactivos,** como las barras de progreso.
-   **Asigne las claves de acceso del botón confirmar primero para asegurarse de que tienen las asignaciones de clave estándar.** Si no hay ninguna asignación de clave estándar, utilice la primera letra de la primera palabra. Por ejemplo, la tecla de acceso para los botones sí y no confirmar siempre debe ser "Y" y "N", independientemente de los otros controles del cuadro de diálogo.
-   **En el caso de los botones de confirmación negativos (que no sean cancelar) frase como "no", asigne la clave de acceso a la "n" en "no".** Si no tiene frase como "no", use la asignación de la clave de acceso estándar o asigne la primera letra de la primera palabra. Al hacerlo, todo no se realiza y no tiene una clave de acceso coherente.
-   Para facilitar la búsqueda de las **claves de acceso, asigne las teclas de acceso a un carácter que aparece al principio de la etiqueta,** idealmente el primer carácter, incluso si hay una palabra clave que aparece más adelante en la etiqueta.

Para obtener más instrucciones y ejemplos, consulte [teclado](inter-keyboard.md).

## <a name="text"></a>Texto

-   **Use dos puntos al final de las etiquetas de control externas.** Algunas tecnologías de ayuda buscan dos puntos para identificar las etiquetas de control.
-   **Coloca las etiquetas de forma coherente con respecto a los elementos que se etiquetan.** Esto ayuda a la tecnología de asistencia a asociar correctamente las etiquetas con sus controles correspondientes y ayuda a los usuarios de los ampliadores de pantalla a saber dónde buscar una etiqueta o un control.

    ![captura de pantalla de etiquetas colocadas de forma coherente ](images/inter-accessibility-image14.png)

    En este ejemplo, las etiquetas de cada una de las listas desplegables se colocan de forma coherente y usan dos puntos.

-   **Limite el texto alternativo a 150 caracteres como máximo.** Describa la acción para activar el control (por ejemplo, haga clic en, haga clic con el botón derecho, etc.) y, a continuación, describa la función del control.

    **Aceptable:**

    Botón.

    Colinas azules.

    **Manera**

    Haga clic para iniciar sesión en su cuenta.

    Foto de colinas alejadas que muestran cómo los colores se atenúan a distancia.

-   **No utilice texto para dibujar líneas, cuadros u otros símbolos gráficos.** Los caracteres que se usan de esta manera pueden confundir a los usuarios de los lectores de pantalla. Por ejemplo, un cuadro dibujado con la letra "X" alrededor de un área de texto se lee mediante el software lector de pantalla como "X x x x x x" en la primera línea, seguido de "X" y el contenido y "X".

## <a name="documentation"></a>Documentación

-   Documente todas las opciones y características de accesibilidad (por ejemplo, todos los métodos abreviados de teclado).
-   Cree documentación accesible en formatos accesibles. Por lo tanto, la documentación en sí debe cumplir las mismas reglas de accesibilidad que la interfaz de usuario principal.
-   Consulte teclas de acceso, no teclas de método abreviado (que tienen un significado y uso diferentes), teclas de acceso o aceleradores.
-   En general, consulte a una persona con un tipo de discapacidad, no una persona deshabilitada. Considere la persona en primer lugar, no la etiqueta.



|                                                               |                                                                                  |
|---------------------------------------------------------------|----------------------------------------------------------------------------------|
| **Usar estos términos**<br/>                                | **En lugar de**<br/>                                                        |
| Tiene destreza limitada, tiene discapacidades de movimiento<br/>     | Desperjudicado, lisiado<br/>                                                        |
| Sin discapacidades<br/>                               | Normal, con cuerpo y en buen estado<br/>                                          |
| Monodireccionales, personas que escriben con una mano<br/>          | Una sola entrega <br/>                                                        |
| Personas con discapacidades<br/>                           | Los usuarios deshabilitados, deshabilitados, personas con discapacidades, el minusválido<br/> |
| Discapacidades cognitivas, discapacidades de desarrollo<br/> |                                                                                  |



 


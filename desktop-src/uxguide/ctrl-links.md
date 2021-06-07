---
title: Vínculos
description: Con un vínculo, los usuarios pueden navegar a otra página, ventana o tema de Ayuda. mostrar una definición; iniciar un comando; o elija una opción.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 161313008612d04b5009942f82f662888d1ffd35
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524260"
---
# <a name="links"></a>Vínculos

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Con un *vínculo*, los usuarios pueden navegar a otra página, ventana o tema de Ayuda; mostrar una definición; iniciar un comando; o elija una opción. Un vínculo es texto o un gráfico que indica que se puede hacer clic en él, normalmente mediante el uso de los colores del sistema de vínculos visitados o no [visualizados.](vis-color.md) Tradicionalmente, los vínculos también se subrayan, pero ese enfoque a menudo no es necesario y se desaconspeda para reducir el desorden visual.

Cuando los usuarios mantienen el puntero sobre un vínculo, el texto del vínculo aparece como subrayado (si no lo estaba ya) y la forma del puntero cambia a una [mano.](inter-mouse.md)

Un vínculo de texto es el control en el que se puede hacer clic más ligeramente y, a menudo, se usa para reducir la complejidad visual de un diseño.

> [!Note]  
> Las instrucciones relacionadas con [los vínculos de](ctrl-command-links.md) comandos [y el](vis-layout.md) diseño se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **Es el vínculo que se usa para navegar a otra página, ventana o tema de Ayuda; mostrar una definición; iniciar un comando; o elegir una opción?** Si no es así, usa otro control.
-   **¿Un botón de comando sería una opción mejor?** Use un [botón de comando](ctrl-command-buttons.md) si:
    -   El control inicia una acción inmediata, incluida la visualización de una ventana, y ese comando se relaciona con el propósito principal de la ventana.
    -   Se muestra una ventana para recopilar la entrada o tomar decisiones, incluso si se trata de un comando secundario.
    -   La etiqueta es corta, consta de cuatro o menos palabras, lo que evita la apariencia difícil de los botones largos.
    -   El comando no está en línea.
    -   El control aparece dentro de un grupo de otros botones de comando relacionados.
    -   La acción es destructiva o irreversible. Dado que los usuarios asocian vínculos con la navegación (y la capacidad de volver atrás), los vínculos no son adecuados para los comandos con consecuencias significativas.
    -   De forma similar, en un [asistente o](win-wizards.md) [flujo de tareas](glossary.md), el comando representa el compromiso. En estas ventanas, los botones de comando sugieren compromiso, mientras que los vínculos sugieren navegar al paso siguiente.

## <a name="design-concepts"></a>Conceptos de diseño

**Hacer que los vínculos se reconocen**

Los [vínculos carecen de](glossary.md)asequibilidad, lo que significa que sus **propiedades visuales** no sugieren cómo se usan y solo se entienden a través de la experiencia. Los vínculos sin un subrayado y los colores del sistema de vínculos aparecen como texto normal; La única manera de determinar su comportamiento es desde su presentación, su contexto o colocando el puntero sobre ellos.

Sorprendentemente, esta falta de asequibilidad suele ser una motivación para usar vínculos porque parecen tan ligeros, lo que reduce la complejidad visual de un diseño. Los vínculos eliminan el marco visualmente pesado que usan los [botones de comando](ctrl-command-buttons.md) y el borde que usan otros controles. Por ejemplo, aunque puede usar botones de comando para hacer que los comandos principales sea obvio, puede elegir vínculos para los comandos secundarios para desencentrrlos.

El desafío consiste entonces en mantener suficientes pistas visuales para que los usuarios puedan reconocer los vínculos. La guía fundamental es que los usuarios deben ser capaces de reconocer los vínculos mediante inspección visual por sí solos, no deben tener que mantener el puntero sobre un objeto o hacer clic en él para determinar si se trata de **un vínculo**.

Los usuarios pueden reconocer un vínculo solo [](vis-color.md) mediante inspección visual si el vínculo usa los colores del sistema de vínculos y al menos una de las siguientes pistas visuales:

-   Texto subrayado.
-   Gráfico o viñeta, como con el texto con el [patrón de vínculo de](#usage-patterns) icono.
-   Colocación dentro de una ubicación de navegación, [](glossary.md) opción o comando estándar, como el área de contenido de una ventana o en una barra de navegación, barra de menús, barra de herramientas o pie de página.

Los usuarios también pueden reconocer un vínculo mediante inspección visual con las siguientes pistas visuales, pero estas pistas no son suficientes por sí mismos:

-   Texto que sugiere hacer clic, como un comando que comienza con un verbo imperativo como Mostrar, Imprimir, Copiar o Eliminar.
-   Colocación dentro de un bloque de texto normal.

Por supuesto, los usuarios siempre pueden determinar un vínculo a través de la interacción, ya sea mantener el puntero o hacer clic. Si la detección de un vínculo no es necesaria para realizar tareas importantes, puede desacentr estos vínculos.

![captura de pantalla de etiquetas grises en el fondo negro ](images/ctrl-links-image1.png)

En este ejemplo, póngase en contacto con nosotros, los términos de uso, las marcas comerciales y la declaración de privacidad son vínculos. Se desmarcan intencionadamente porque no son necesarias para ninguna tarea importante. Las únicas pistas de que son vínculos son que tienen un puntero del mouse al mantener el puntero y se sitúan en un área de navegación estándar en la parte inferior de la ventana.

**Hacer que los vínculos sean específicos, pertinentes y predecibles**

El texto del vínculo debe indicar el resultado de hacer clic en el vínculo.

Los vínculos específicos son más atractivos para los usuarios que los vínculos generales, por lo que use etiquetas de vínculo que den información descriptiva específica sobre el resultado de hacer clic **en el vínculo**. Sin embargo, asegúrese de que el texto del vínculo no sea tan específico que sea confuso y desaconseja el uso adecuado.

Es más probable que se lean vínculos concisos que vínculos detallados. **Elimine el texto y los detalles innecesarios.** Las etiquetas de vínculo no tienen que ser completas.

Para evaluar el texto del vínculo:

-   Asegúrese de que el texto del vínculo refleja los escenarios que admite el vínculo.
-   Asegúrese de que los resultados del vínculo son predecibles. Los resultados no deben sorprender a los usuarios.

**Si solo hace dos cosas...**

1. Hacer que los vínculos se detecte solo mediante inspección visual. Los usuarios no deben tener que interactuar con el programa para buscar vínculos.

2. Use vínculos que den información descriptiva específica sobre el resultado de hacer clic en el vínculo, usando tanto texto como sea necesario. Los usuarios deben poder predecir con precisión el resultado de un vínculo a partir de su texto de vínculo y la información [opcional](ctrl-tooltips-and-infotips.md).

## <a name="usage-patterns"></a>Patrones de uso

Los vínculos tienen varios patrones funcionales:



|    Uso                  |    Ejemplo   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vínculos de navegación**<br/> Vínculo que se usa para navegar a otra página o ventana. <br/>                                                      | Al hacer clic en el vínculo, se navega de forma local a otra página, como en una ventana o asistente del explorador. o muestra una nueva ventana. A diferencia de los vínculos de tareas, la navegación no inicia una tarea, sino que simplemente navega a otro lugar o continúa con una tarea que ya está en curso. La navegación implica seguridad porque el usuario siempre puede volver atrás.<br/> Titulares de noticias<br/> En este ejemplo, al hacer clic en el vínculo, se navega a la página Titulares de noticias.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Vínculos de tareas**<br/> Vínculo que se usa para iniciar un nuevo comando. <br/>                                                                        | Al hacer clic en el vínculo, se ejecuta un comando inmediatamente o se muestra un cuadro de diálogo o una página para recopilar más entradas. A diferencia de los vínculos de navegación, los vínculos de tareas inician una nueva tarea en lugar de continuar con una tarea existente. Las tareas no implican que los usuarios de seguridad no puedan revertir al estado anterior con un comando Atrás. Los vínculos de tareas se llaman así para evitar confusiones con los [vínculos de comando](ctrl-command-links.md). <br/> Iniciar sesión<br/> En este ejemplo, al hacer clic en el vínculo se inicia un comando de inicio de sesión.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Vínculos a la Ayuda**<br/> Vínculo de texto que se usa para mostrar un tema de Ayuda. <br/>                                                                     | Al hacer clic en el vínculo se muestra un artículo de Ayuda en una ventana independiente.<br/> ¿Qué es una contraseña segura?<br/> En este ejemplo, al hacer clic en el vínculo se muestra una ventana de Ayuda con el tema dado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Vínculos de definición**<br/> un vínculo de texto que se usa para mostrar una definición en una información cuando el usuario hace clic en el vínculo o mantiene el puntero sobre él. <br/> | Este patrón es útil para definir términos que es posible que los usuarios no conozcan sin agregar desorden en la pantalla.<br/> ![captura de pantalla de información que se muestra al mantener el mouse ](images/ctrl-links-image2.png)<br/> En este ejemplo, se muestra la definición de información sobre información. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Vínculos de menú**<br/> un conjunto de vínculos de tareas que se usan para crear un menú. <br/>                                                                    | Dado que el contexto del menú indica un conjunto de vínculos, el texto no suele estar subrayado (excepto al mantener el puntero) y es posible que no use los colores del sistema de vínculos.<br/> ![captura de pantalla de un conjunto de vínculos ](images/ctrl-links-image3.png)<br/> En este ejemplo, un conjunto de vínculos crea un menú.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Vínculos de opción**<br/> una opción seleccionada o su marcador de posición, donde al hacer clic en el vínculo se invoca un comando para cambiar esa opción.<br/>       | A diferencia de los vínculos de texto normales, el vínculo cambia su texto para reflejar la opción seleccionada actualmente y siempre se dibuja con el color de vínculo novisido. <br/> ![captura de pantalla de una regla en el Asistente para reglas de Outlook ](images/ctrl-links-image4.png)<br/> En el ejemplo de la izquierda se muestra una regla del Asistente para reglas de Microsoft Outlook con opciones de marcador de posición. Después de que los usuarios hacen clic en los vínculos y seleccionan algunas opciones, el ejemplo derecho actualiza el texto del vínculo para mostrar los resultados.<br/> usar vínculos de opción es especialmente adecuado si las opciones tienen un formato de variable. <br/> ![captura de pantalla de una regla modificada en el Asistente para reglas ](images/ctrl-links-image5.png)<br/> En el ejemplo de la derecha se muestra que las reglas de Outlook tienen un formato de variable. <br/> ![captura de pantalla de cómo cambia el texto a la lista desplegable ](images/ctrl-links-image6.png)<br/> En el ejemplo de la izquierda se muestra un vínculo de opción. Se convierte en una lista desplegable cuando se selecciona, como se muestra a la derecha.<br/> |



 

Los vínculos también tienen varios patrones de presentación:



|    Uso                                 |    Ejemplo                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vínculos de texto sin formato**<br/> solo constan de texto. <br/>                                      | esta presentación es la más flexible porque se puede usar en cualquier lugar, incluido [en línea](glossary.md).<br/> ![captura de pantalla del texto del vínculo azul ](images/ctrl-links-image7.png)<br/> En este ejemplo, el color del texto identifica claramente un vínculo en línea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Texto con vínculos de icono**<br/> texto con un icono anterior que indica su función.<br/> | Dado que el gráfico proporciona una indicación visual adicional de un vínculo, es más fácil reconocerlo como vínculo que un vínculo de texto sin formato que no esté subrayado. este patrón suele usar un icono de 16 x 16 píxeles.<br/> ![captura de pantalla de la lista de cuatro vínculos con iconos ](images/ctrl-links-image8.png)<br/> En este ejemplo, los iconos proporcionan una indicación visual adicional de un vínculo.<br/> ![captura de pantalla del comando play con triángulo pequeño ](images/ctrl-links-image9.png)<br/> En este ejemplo, el símbolo de reproducción triangular estándar indica que este texto es un comando.<br/>                                                                                                                                     |
| **Vínculos de solo gráficos**<br/> consta solo de un gráfico.<br/>                               | Dada la falta de un vínculo de texto, no hay color de vínculo ni subrayado para indicar el vínculo. Estos vínculos dependen del diseño gráfico para sugerir clics o del texto dentro del gráfico que sugiere una acción cuando los usuarios hacen clic. Los vínculos solo gráficos a veces tienen un efecto de mouse sobre para indicar el vínculo. este enfoque ayuda, pero no se puede detectar mediante la inspección visual por sí solo.<br/> ![captura de pantalla del icono con el puntero del mouse de selección de vínculo ](images/ctrl-links-image10.png)<br/> En este ejemplo, la inspección visual no puede detectar el vínculo por sí solo.<br/> **Debido a sus posibles problemas de reconocimiento y localización, no se recomiendan vínculos de solo gráficos como la única manera de realizar una tarea.** <br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **Muestra un puntero ocupado si el resultado de hacer clic en un vínculo no es instantáneo.** Sin comentarios, los usuarios podrían suponer que el clic no se ha hecho y hacer clic de nuevo.

### <a name="color"></a>Color

-   **Use los colores del sistema de temas o vínculos para los vínculos visitados y novistiados.** El significado de estos colores es coherente en todos los programas. Si, por cualquier motivo, a los usuarios no les gustan estos colores (quizás por motivos de accesibilidad), pueden cambiarlos ellos mismos.
-   **Para los vínculos de navegación, use colores diferentes para los vínculos visitados y novistidos.** Mantenga el historial de vínculos visitados solo mientras dure la instancia del programa. El color visitado es importante para indicar dónde han estado los usuarios, lo que impide que vuelvan a visitar involuntarlamente las mismas páginas varias veces.
-   **Para otros tipos de vínculos, no use el color del vínculo visitado.** Por ejemplo, no hay suficiente valor para identificar comandos "visitados".
-   **No colore el texto que no sea un vínculo porque los usuarios pueden suponer que es un vínculo.** Use negrita o un tono gris donde, de lo contrario, usaría texto coloreado.
-   **Excepción:** puede usar texto coloreado si todos los vínculos están subrayados o colocados dentro de ubicaciones de comandos o navegación estándar.

    **Incorrecto:**

    ![captura de pantalla del mensaje de plan de energía con texto azul ](images/ctrl-links-image11.png)

    En este ejemplo, el texto azul se usa incorrectamente para el texto que no es un vínculo.

-   **Use colores de fondo que contrastan con los colores de vínculo.** El [color del sistema de](vis-color.md) ventana siempre es una buena opción.

    **Incorrecto:**

    ![captura de pantalla de texto de vínculo azul sobre fondo azul ](images/ctrl-links-image12.png)

    En este ejemplo, el color de fondo proporciona un contraste deficiente con el color de vínculo.

### <a name="underlining"></a>Subrayando

-   **En el caso de los vínculos necesarios para realizar una tarea principal, proporcione pistas visuales para que los usuarios puedan reconocer los vínculos por inspección visual por sí solos.** Estas pistas incluyen la sublineación, gráficos o viñetas y ubicaciones de vínculo estándar. Los usuarios no deben tener que mantener el puntero sobre un objeto ni intentar hacer clic en él para determinar si es un vínculo. Use texto subrayado si el vínculo no es obvio desde su contexto.
-   **No subrayado texto que no sea un vínculo porque los usuarios pueden suponer que es un vínculo.** Use cursiva donde, de lo contrario, usaría texto subrayado. Reserve la sublineación solo para los vínculos.
-   **Al imprimir, no imprima subrayados ni colores de vínculo.** Los vínculos impresos no tienen ningún valor y pueden resultar confusos.

### <a name="text-with-icon-links"></a>Texto con vínculos de icono

-   **Use el icono de flecha solo para los vínculos de comandos.** Los vínculos normales no deben usar el icono de flecha a menos que se usen como sustituto de los vínculos [de comandos](ctrl-command-links.md) en Windows XP.
-   **Coloque el icono a la izquierda del texto.** El icono debe dirigirse visualmente al texto.

**Correcto:**

![captura de pantalla del icono de texto anterior ](images/ctrl-links-image13.png)

**Incorrecto:**

![captura de pantalla del icono siguiente texto ](images/ctrl-links-image14.png)

En el ejemplo incorrecto, el icono no lleva al texto.

-   **Haga que el resultado de hacer clic en el icono sea el mismo que al hacer clic en el texto.** De lo contrario, sería inesperado y confuso.

### <a name="graphics-only-links"></a>Vínculos de solo gráficos

-   **No use vínculos de solo gráficos.** Los usuarios tienen dificultades para reconocerlos como vínculos y cualquier texto dentro del gráfico (que se usa para indicar su acción cuando se hace clic) crea un problema de localización.

### <a name="navigation-links"></a>Vínculos de navegación

-   **Asegúrese de que los vínculos de navegación no requieren compromiso.** Los usuarios siempre deben poder volver al estado inicial, ya sea usando Atrás para la navegación en el lugar o Cancelar para cerrar una nueva ventana.
-   **Vínculo a contenido específico en lugar de contenido general.** Por ejemplo, es mejor vincular a la sección pertinente de un documento que vincular al principio.
-   **Use un vínculo solo si el material vinculado es pertinente, útil y no redundante.** El uso de restricciones en los vínculos de navegación no los usa solo porque puede.
-   **Si un vínculo navega a un sitio externo, coloque** la dirección URL en la información para que los usuarios puedan determinar el destino del vínculo.
-   **Vincule solo la primera aparición del texto del vínculo.** Los vínculos redundantes no son necesarios y pueden dificultar la lectura del texto.

    **Correcto:**

    La carpeta Imágenes facilita el uso compartido de las imágenes. Puede usar las tareas de Imágenes para enviar las imágenes por correo electrónico o publicarlas en una ubicación privada segura en la Web. También puede imprimir las imágenes directamente desde la carpeta Imágenes.

    **Incorrecto:**

    La carpeta Imágenes facilita el uso compartido de las imágenes. Puede usar las tareas de Imágenes para enviar las imágenes por correo electrónico o publicarlas en una ubicación privada segura en la Web. También puede imprimir las imágenes directamente desde la carpeta Imágenes.

    En el ejemplo correcto, solo se vincula la primera aparición del texto pertinente.

    **Excepciones:**

    -   **Si una instrucción tiene un vínculo, coloque el vínculo en la instrucción .**

        El uso de contraseñas seguras es muy importante. Para obtener más información, consulte Contraseñas seguras.

        En este ejemplo, el vínculo está en la instrucción en lugar de la primera aparición.

    -   **Vincule a las repeticiones posteriores si están lejos de la primera.** Por ejemplo, puede vincular de forma redundante en distintas secciones dentro de un tema de Ayuda.

### <a name="task-links"></a>Vínculos de tareas

-   **Use vínculos de tarea para comandos que no sean destructivos o sean fácilmente reversibles.** Dado que los usuarios asocian vínculos con la navegación (y la capacidad de resalte), los vínculos no son adecuados para los comandos con consecuencias significativas. Los comandos que muestran un cuadro de diálogo o una confirmación son una buena opción.

    **Correcto:**

    Start

    Stop

    **Incorrecto:**

    Eliminar archivo

    En el ejemplo incorrecto, el comando es destructivo.

### <a name="menu-links"></a>Vínculos de menú

-   **Agrupación de vínculos de tareas y navegación relacionados en menús.** Un menú de vínculos relacionados colocados dentro de una ubicación de comandos o navegación estándar facilita la búsqueda y la información de los vínculos que cuando se colocan por separado.
-   **Para los menús dependientes de la selección, quite los vínculos de menú que no se aplican.** No los deshabilite. Si lo hace, se elimina el desorden y los usuarios no perderán los vínculos que requieren selección.
-   **Para los menús independientes de la selección, deshabilite los vínculos de menú que no se aplican.** No los quite. Al hacerlo, los menús son más estables y estos vínculos son más fáciles de encontrar.

    ![captura de pantalla del cuadro de diálogo con el comando de menú atenuado ](images/ctrl-links-image15.png)

    En este ejemplo de Windows Update, se está realizando una actualización, por lo que el comando Buscar actualizaciones está deshabilitado en lugar de quitarse.

### <a name="link-infotips"></a>Información sobre vínculos

-   Si un vínculo requiere una explicación adicional, proporcione la explicación en un control de **texto** independiente o en una [información,](ctrl-tooltips-and-infotips.md)pero no en ambos. Use oraciones completas y signos de puntuación finales. Proporcionar ambos no es necesario si el texto es el mismo y confuso si el texto es diferente.

    ![captura de pantalla del vínculo con texto complementario ](images/ctrl-links-image16.png)

    En este ejemplo, una explicación complementaria proporciona más información sobre el vínculo.

    ![captura de pantalla del vínculo con información ](images/ctrl-links-image17.png)

    En este ejemplo, una información sobre información proporciona más información.

-   **No proporcione información que sea simplemente una nueva declaración del texto del vínculo.**

    **Incorrecto:**

    ![captura de pantalla del vínculo con información redundante ](images/ctrl-links-image18.png)

    En este ejemplo, la información sobre la información corre el riesgo de que los usuarios se quejen por su repetibilidad.

## <a name="text"></a>Texto

-   No asigne una clave [de acceso.](glossary.md) Se accede a los vínculos mediante la tecla Tab.
-   **Use vínculos que den información descriptiva específica sobre el resultado** de hacer clic en el vínculo , usando tanto texto como sea necesario. El texto del vínculo debe indicar el resultado de hacer clic en el vínculo. **Los usuarios deben poder predecir con precisión el resultado de un vínculo a partir de su texto de vínculo y la información opcional.**

    **Incorrecto:**

    ![captura de pantalla de un vínculo de advertencia de aviso de seguridad ](images/ctrl-links-image19.png)

    En este ejemplo, aunque el vínculo parezca importante, su etiqueta es demasiado general. Es más probable que los usuarios haga clic en un vínculo más específico.

-   Para vínculos en línea:
    -   Conserve el uso de mayúsculas y signos de puntuación del texto.
    -   No incluya la puntuación final en el vínculo a menos que el texto sea una pregunta.
    -   Vincule en la parte más relevante del texto y elija texto de vínculo lo suficientemente grande como para que sea fácil de hacer clic.

        **Correcto:**

        Vaya a un grupo de noticias.

        **Incorrecto:**

        Vaya a un grupo de noticias.

        En estos ejemplos, "Go" no es la parte más relevante del texto y no es lo suficientemente grande como para hacer un buen destino de clic, mientras que "newsgroup" es.

    -   **Evite colocar dos vínculos en línea diferentes entre sí.** Es probable que los usuarios crean que son un único vínculo.

        **Incorrecto:**

        Para más información, consulte Directrices de la experiencia de usuario.

        En este ejemplo, "UX" y "guidelines" son dos vínculos diferentes.

-   Para vínculos independientes (no en línea):
    -   Use [mayúsculas de estilo oración.](glossary.md)
    -   No use la puntuación final a menos que el vínculo sea una pregunta.
    -   Use todo el texto como vínculo.
-   Use vínculos claramente diferenciados de los demás vínculos de la pantalla. Los usuarios deben poder predecir y diferenciar con precisión entre los destinos de vínculo.

    **Incorrecto:**

    Buscar software antivirus

    Obtener software antivirus

    **Correcto:**

    Cómo saber si el software antivirus está instalado

    Instalación de software antivirus

    En el ejemplo incorrecto, la distinción entre los dos vínculos no es clara.

-   No agregue Haga clic o haga clic aquí al texto del vínculo. No es necesario porque un vínculo implica hacer clic. Además, haga clic aquí y aquí solo para transmitir información sobre el vínculo cuando lo lea un lector de pantalla.

    **Incorrecto:**

    Haga clic aquí para obtener una descripción.

    **Correcto:**

    Descripción

    En los ejemplos incorrectos, "haga clic aquí" no dice nada y no transmite información sobre el vínculo.

**Vínculos de navegación**

-   **Inicie el vínculo con un sustantivo y describa claramente dónde irá al hacer clic en el vínculo.** No uses puntuación final. En ocasiones, es posible que deba iniciar vínculos de navegación con un verbo, pero no use verbos que repitiendo la navegación que ya está implícita por el hecho de vincular, como Ver, Abrir o Ir a.
-   **Presente un vínculo de navegación como una dirección URL si navega a una página web y espera que los usuarios de destino recuerden la dirección URL y la escriban en un explorador.** Si es posible, diseñe estas direcciones URL para que sean cortas y fáciles de recordar.
-   **Si el vínculo incluye una dirección URL a un sitio web a partir de "www", omita el nombre https:// protocolo y use texto en minúsculas.**

    **Incorrecto:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Correcto:**

    microsoft.com

    En los ejemplos incorrectos, "https://" y "www" van sin decir nada.

**Vínculos de tareas**

-   **Inicie el vínculo con un verbo imperativo y describa claramente la tarea que realiza el vínculo.** No uses puntuación final.
-   **Finalice el vínculo con puntos suspensivos si el comando necesita información adicional (incluida una confirmación) para la finalización correcta.** No use puntos suspensivos cuando la finalización correcta de la tarea sea mostrar otra ventana solo cuando se necesite información adicional para realizar la tarea.

    Imprimir...

    En este ejemplo, imprimir... El vínculo de comando muestra un cuadro de diálogo Imprimir para recopilar más información.

    Impresión

    Por el contrario, en este ejemplo, un vínculo de comando Imprimir imprime una sola copia de un documento en la impresora predeterminada sin ninguna interacción adicional del usuario.

    **El uso adecuado de puntos suspensivos** es importante para indicar que los usuarios pueden tomar más decisiones antes de realizar la tarea, o bien puede cancelar la tarea por completo. La indicación visual que ofrece un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

-   **Si es necesario, finalice un vínculo de tarea con "now" para distinguirlo de un vínculo de navegación.**

    Descarga de archivos

    Descarga de archivos ahora

    En este ejemplo, "Descargar archivos" navega a una página para descargar archivos, mientras que "Descargar archivos ahora" realmente realiza el comando .

**Vínculos a la Ayuda**

Para obtener instrucciones y ejemplos, vea [Ayuda .](winenv-help.md)

**Información sobre vínculos**

-   Use oraciones completa y signos de puntuación finales.

Para obtener más instrucciones y ejemplos, vea [Información sobre herramientas e información sobre herramientas.](ctrl-tooltips-and-infotips.md)

## <a name="documentation"></a>Documentación

Al hacer referencia a vínculos:

-   Use el texto de vínculo exacto, incluida su mayúscula, pero no incluya los puntos suspensivos.
-   Para describir la interacción del usuario, use click.
-   Cuando sea posible, formatee el texto del vínculo con texto en negrita. De lo contrario, coloque el texto del vínculo entre comillas solo si es necesario para evitar confusiones.

Ejemplo: para iniciar el examen, haga clic **en Examinar un equipo.**

 


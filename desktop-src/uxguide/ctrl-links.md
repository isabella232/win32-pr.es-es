---
title: Vínculos
description: Con un vínculo, los usuarios pueden desplazarse a otra página, ventana o tema de ayuda; Mostrar una definición; iniciar un comando; o elija una opción.
ms.assetid: a23748e4-b2dd-4b9f-9a7c-ff6533922c8c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 521f96146de535210d79814b375499ea34399179
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104552733"
---
# <a name="links"></a>Vínculos

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Con un *vínculo*, los usuarios pueden desplazarse a otra página, ventana o tema de ayuda; Mostrar una definición; iniciar un comando; o elija una opción. Un vínculo es texto o un gráfico que indica que se puede hacer clic en él; normalmente, se muestra con los [colores del sistema de vínculo](vis-color.md)visitado o no visitado. Tradicionalmente, los vínculos también están subrayados, pero este enfoque no suele ser necesario y no favorecer la confusión visual.

Cuando los usuarios mantienen el mouse sobre un vínculo, el texto del vínculo aparece como subrayado (si aún no lo estaba) y la forma de puntero cambia a una [mano](inter-mouse.md).

Un vínculo de texto es el control en el que se hace clic con menor peso y se usa a menudo para reducir la complejidad visual de un diseño.

> [!Note]  
> Las instrucciones relacionadas con los [vínculos de comandos](ctrl-command-links.md) y el [diseño](vis-layout.md) se presentan en artículos independientes.

 

## <a name="is-this-the-right-control"></a>¿Es este el control adecuado?

Para decidirte, intenta responder a estas preguntas:

-   **Es el vínculo que se usa para navegar a otra página, ventana o tema de ayuda; Mostrar una definición; iniciar un comando; ¿o elige una opción?** Si no es así, usa otro control.
-   **¿Sería un botón de comando una opción mejor?** Use un [botón de comando](ctrl-command-buttons.md) si:
    -   El control inicia una acción inmediata, incluida la visualización de una ventana, y ese comando se relaciona con el propósito principal de la ventana.
    -   Se muestra una ventana para recopilar entradas o tomar decisiones, incluso si se trata de un comando secundario.
    -   La etiqueta es corta y consta de cuatro o menos palabras, lo que evita la apariencia poco complicada de botones largos.
    -   El comando no está alineado.
    -   El control aparece dentro de un grupo de otros botones de comando relacionados.
    -   La acción es destructiva o irreversible. Dado que los usuarios asocian vínculos con la navegación (y la capacidad de revertir), los vínculos no son adecuados para los comandos con consecuencias significativas.
    -   Del mismo modo, en un [flujo de tareas](glossary.md)o un [Asistente](win-wizards.md) , el comando representa el compromiso. En tales ventanas, los botones de comando sugieren compromiso, mientras que los vínculos sugieren ir al paso siguiente.

## <a name="design-concepts"></a>Conceptos de diseño

**Crear vínculos reconocible**

Los vínculos carecen de [asequibilidad](glossary.md), lo que significa que **sus propiedades visuales no sugieren cómo se usan** y se entienden solo a través de la experiencia. Los vínculos sin subrayado y vincular colores del sistema aparecen como texto normal; la única manera de determinar su comportamiento es desde su presentación, su contexto o colocando el puntero sobre ellos.

Sorprendentemente, esta falta de asequibilidad es a menudo una motivación para el uso de vínculos porque parecen tan ligeros, lo que reduce la complejidad visual de un diseño. Los vínculos eliminan el marco visualmente pesado utilizado por los [botones de comando](ctrl-command-buttons.md) y el borde utilizados por otros controles. Por ejemplo, aunque puede usar los botones de comando para que los comandos principales sean obvios, puede elegir vínculos para comandos secundarios para desenfatizarlos.

A continuación, el desafío es mantener suficientes pistas visuales para que los usuarios puedan reconocer los vínculos. La directriz fundamental es que **los usuarios deben ser capaces de reconocer los vínculos mediante la inspección visual únicamente no deben tener que mantener el mouse sobre un objeto o hacer clic en él para determinar si es un vínculo**.

Los usuarios pueden reconocer un vínculo mediante la inspección visual por sí solo si el vínculo usa los [colores del sistema de vínculo](vis-color.md) y al menos una de las siguientes indicaciones visuales:

-   Texto subrayado.
-   Un gráfico o una viñeta, como con el patrón de [vínculo texto con icono](#usage-patterns) .
-   Selección de ubicación en una ubicación de navegación, opción o comando estándar, como el [área de contenido](glossary.md) de una ventana o en una barra de navegación, una barra de menús, una barra de herramientas o un pie de página.

Los usuarios también pueden reconocer un vínculo mediante inspección visual con las siguientes indicaciones visuales, pero estas pistas no son suficientes por sí mismas:

-   Texto que sugiere hacer clic, como un comando que comienza con un verbo imperativo como mostrar, imprimir, copiar o eliminar.
-   Ubicación dentro de un bloque de texto normal.

Por supuesto, los usuarios siempre pueden determinar un vínculo a través de la interacción al mantener el mouse o hacer clic. Si no se requiere la detección de un vínculo para tareas significativas, puede deshacer este tipo de vínculos.

![captura de pantalla de las etiquetas grises en el fondo negro ](images/ctrl-links-image1.png)

En este ejemplo, póngase en contacto con nosotros, términos de uso, marcas comerciales y declaración de privacidad. Se desenfatizan intencionalmente porque no son necesarios para las tareas importantes. Las únicas pistas que son vínculos son que tienen un puntero del mouse sobre el desplazamiento y se colocan en un área de navegación estándar en la parte inferior de la ventana.

**Crear vínculos específicos, relevantes y predecibles**

El texto del vínculo debe indicar el resultado de hacer clic en el vínculo.

Los vínculos específicos son más atractivos para los usuarios que los vínculos generales, por lo que debe **usar etiquetas de vínculo que proporcionen información descriptiva específica sobre el resultado de hacer clic en el vínculo**. Sin embargo, asegúrese de que el texto del vínculo no sea tan específico que sea engañoso y desaconseja el uso adecuado.

Es más probable que se lean vínculos concisos que los vínculos detallados. **Elimine el texto y los detalles innecesarios.** No es necesario que las etiquetas de vínculo sean completas.

Para evaluar el texto del vínculo:

-   Asegúrese de que el texto del vínculo refleja los escenarios que admite el vínculo.
-   Asegúrese de que los resultados del vínculo son predecibles. Los resultados no deberían sorprender a los usuarios.

**Si solo hace dos cosas...**

1. Hacer que los vínculos sean reconocibles por la inspección visual solo. Los usuarios no deben tener que interactuar con el programa para buscar vínculos.

2. Use los vínculos que proporcionan información descriptiva específica sobre el resultado de hacer clic en el vínculo, utilizando tantos textos como sea necesario. Los usuarios deben ser capaces de predecir con precisión el resultado de un vínculo desde el texto del vínculo y el recuadro informativo [opcional.](ctrl-tooltips-and-infotips.md)

## <a name="usage-patterns"></a>Patrones de uso

Los vínculos tienen varios patrones funcionales:



|                                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vínculos de navegación**<br/> Un vínculo que se usa para navegar a otra página o ventana. <br/>                                                      | Al hacer clic en el vínculo, se navega por la ubicación en otra página, como en una ventana o un asistente del explorador. o muestra una nueva ventana. A diferencia de los vínculos de tarea, la navegación no inicia una tarea, sino que simplemente navega a otro lugar o continúa con una tarea que ya está en curso. La navegación implica la seguridad porque el usuario siempre puede volver.<br/> Titulares de noticias<br/> En este ejemplo, al hacer clic en el vínculo, se navega a la página titulares de noticias.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Vínculos de tarea**<br/> Un vínculo que se usa para iniciar un nuevo comando. <br/>                                                                        | Al hacer clic en el vínculo, se realiza un comando inmediatamente o se muestra un cuadro de diálogo o una página para recopilar más entradas. A diferencia de los vínculos de navegación, los vínculos de tarea inician una nueva tarea en lugar de continuar con una tarea existente. Las tareas no implican que safetyusers no pueda revertir al estado anterior con un comando atrás. Se llama a los vínculos de tarea para evitar la confusión con los [vínculos de comandos](ctrl-command-links.md). <br/> Inicio de sesión<br/> En este ejemplo, al hacer clic en el vínculo, se inicia un comando de inicio de sesión.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Vínculos a la Ayuda**<br/> Vínculo de texto que se usa para mostrar un tema de ayuda. <br/>                                                                     | Al hacer clic en el vínculo, se muestra un artículo de ayuda en una ventana independiente.<br/> ¿Qué es una contraseña segura?<br/> En este ejemplo, al hacer clic en el vínculo, se muestra una ventana de ayuda con el tema especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Vínculos de definición**<br/> un vínculo de texto que se usa para mostrar una definición en un recuadro informativo cuando el usuario hace clic en el vínculo o mantiene el mouse sobre él. <br/> | Este patrón es útil para definir términos que es posible que no conozcan los usuarios sin agregar desorden en la pantalla.<br/> ![captura de pantalla del recuadro informativo que se muestra al mantener el mouse ](images/ctrl-links-image2.png)<br/> En este ejemplo, se muestra la definición del recuadro informativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Vínculos de menú**<br/> conjunto de vínculos de tarea que se usan para crear un menú. <br/>                                                                    | Dado que el contexto del menú indica un conjunto de vínculos, el texto no suele estar subrayado (excepto al mantener el mouse) y podría no usar los colores del sistema de vínculo.<br/> ![captura de pantalla de un conjunto de vínculos ](images/ctrl-links-image3.png)<br/> En este ejemplo, un conjunto de vínculos crea un menú.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Vínculos de opción**<br/> una opción seleccionada o su marcador de posición, donde al hacer clic en el vínculo se invoca un comando para cambiar esa opción.<br/>       | a diferencia de los vínculos de texto normales, el vínculo cambia el texto para reflejar la opción seleccionada actualmente y siempre se dibuja con el color de vínculo no visitado. <br/> ![captura de pantalla de una regla en el Asistente para reglas de Outlook ](images/ctrl-links-image4.png)<br/> en el ejemplo de la izquierda se muestra una regla del Asistente para reglas de Microsoft Outlook con opciones de marcador de posición. una vez que los usuarios hacen clic en los vínculos y seleccionan algunas opciones, el ejemplo de la derecha actualiza el texto del vínculo para mostrar los resultados.<br/> el uso de vínculos de opción es especialmente adecuado si las opciones tienen un formato variable. <br/> ![captura de pantalla de una regla modificada en el Asistente para reglas ](images/ctrl-links-image5.png)<br/> en el ejemplo de la derecha se muestra que las reglas de Outlook tienen un formato de variable. <br/> ![captura de pantalla de cómo cambia el texto a la lista desplegable ](images/ctrl-links-image6.png)<br/> En el ejemplo de la izquierda se muestra un vínculo de opción. Se convierte en una lista desplegable cuando se selecciona, como se muestra a la derecha.<br/> |



 

Los vínculos también tienen varios patrones de presentación:



|                                                                                                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vínculos de texto sin formato**<br/> constan solo de texto. <br/>                                      | Esta presentación es la más flexible, ya que se puede usar en cualquier parte, incluso en [línea](glossary.md).<br/> ![captura de pantalla de texto de vínculo azul ](images/ctrl-links-image7.png)<br/> En este ejemplo, el color del texto identifica claramente un vínculo insertado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Texto con vínculos de icono**<br/> texto con un icono anterior que indica su función.<br/> | Dado que el gráfico proporciona una indicación visual adicional de un vínculo, es más fácil reconocer como un vínculo que un vínculo de texto sin formato que no está subrayado. Este patrón suele usar un icono de 16x16 píxeles.<br/> ![captura de pantalla de la lista de cuatro vínculos con iconos ](images/ctrl-links-image8.png)<br/> en este ejemplo, los iconos proporcionan una indicación visual adicional de un vínculo.<br/> ![captura de pantalla del comando Play con triángulo pequeño ](images/ctrl-links-image9.png)<br/> En este ejemplo, el símbolo de reproducción triangular estándar indica que este texto es un comando.<br/>                                                                                                                                     |
| **Vínculos solo de gráficos**<br/> solo consta de un gráfico.<br/>                               | Dada la falta de un vínculo de texto, no hay ningún color de vínculo o subrayado para indicar el vínculo. estos vínculos dependen del diseño gráfico para hacer clic, o texto dentro del gráfico que sugiere una acción cuando los usuarios hacen clic. los vínculos de solo gráficos tienen a veces un efecto de pasar el puntero del mouse para indicar el vínculo. Este enfoque ayuda, pero no es reconocible solo por inspección visual.<br/> ![captura de pantalla del icono con el puntero del mouse para seleccionar un vínculo ](images/ctrl-links-image10.png)<br/> En este ejemplo, el vínculo no es reconocible solo por inspección visual.<br/> **Debido a sus posibles problemas de reconocimiento y localización, no se recomienda usar vínculos de solo gráficos como la única forma de realizar una tarea.** <br/> |



 

## <a name="guidelines"></a>Directrices

### <a name="interaction"></a>Interacción

-   **Muestra un puntero ocupado si el resultado de hacer clic en un vínculo no es instantáneo.** Sin comentarios, los usuarios pueden suponer que el clic no se ha producido y hacer clic de nuevo.

### <a name="color"></a>Color

-   **Use el tema o vincule los colores del sistema para los vínculos visitados y no visitados.** El significado de estos colores es coherente en todos los programas. Si, por alguna razón, los usuarios no les gustan estos colores (quizás por motivos de accesibilidad), pueden cambiarlos.
-   **En el caso de los vínculos de navegación, use colores diferentes para los vínculos visitados y no visitados.** Mantenga el historial de los vínculos visitados solo mientras dure la instancia del programa. El color visitado es importante para indicar el lugar en el que los usuarios ya han estado, evitando que revisiten las mismas páginas repetidamente.
-   **Para otros tipos de vínculos, no use el color de vínculo visitado.** No hay suficiente valor para identificar los comandos "visitados", por ejemplo.
-   **No colorear texto que no sea un vínculo porque los usuarios pueden suponer que es un vínculo.** Utilice negrita o un sombreado de color gris en el que, de lo contrario, usaría texto coloreado.
-   **Excepción**: puede usar texto en color si todos los vínculos están subrayados o colocados dentro de la navegación estándar o en ubicaciones de comandos.

    **Incorrecto:**

    ![captura de pantalla del mensaje del plan de energía con texto azul ](images/ctrl-links-image11.png)

    En este ejemplo, el texto azul se usa incorrectamente para el texto que no es un vínculo.

-   **Use los colores de fondo que contrastann los colores de los vínculos.** El [color del sistema de ventana](vis-color.md) siempre es una buena opción.

    **Incorrecto:**

    ![captura de pantalla de texto de vínculo azul en fondo azul ](images/ctrl-links-image12.png)

    En este ejemplo, el color de fondo proporciona un contraste deficiente con el color del vínculo.

### <a name="underlining"></a>Subrayado

-   **En el caso de los vínculos necesarios para realizar una tarea principal, proporcione pistas visuales para que los usuarios puedan reconocer los vínculos mediante la inspección visual por sí solo.** Estas pistas incluyen el subrayado, los gráficos o las viñetas, y las ubicaciones de los vínculos estándar. Los usuarios no deben tener que mantener el mouse sobre un objeto o intentar hacer clic en él para determinar si es un vínculo. Use el texto subrayado si el vínculo no es obvio desde su contexto.
-   **No subraye el texto que no sea un vínculo porque los usuarios pueden suponer que es un vínculo.** Use cursiva en la que, de lo contrario, usará texto subrayado. Reserve el subrayado solo para los vínculos.
-   **Al imprimir, no imprima los subrayados ni los colores de los vínculos.** Los vínculos impresos no tienen ningún valor y son potencialmente confusos.

### <a name="text-with-icon-links"></a>Texto con vínculos de icono

-   **Use el icono de flecha solo para los vínculos de comandos.** Los vínculos normales no deben usar el icono de flecha a menos que se usen como sustituto de los [vínculos de comandos](ctrl-command-links.md) de Windows XP.
-   **Coloque el icono a la izquierda del texto.** El icono debe conducir al texto visualmente.

**Correcto:**

![captura de pantalla del texto anterior del icono ](images/ctrl-links-image13.png)

**Incorrecto:**

![captura de pantalla del icono siguiente texto ](images/ctrl-links-image14.png)

En el ejemplo incorrecto, el icono no conduce al texto.

-   **Haga que el resultado de hacer clic en el icono sea el mismo que si hace clic en el texto.** De lo contrario, sería inesperado y confuso.

### <a name="graphics-only-links"></a>Vínculos solo de gráficos

-   **No use vínculos solo de gráficos.** Los usuarios los reconocen de forma difícil como vínculos y cualquier texto dentro del gráfico (que se usa para indicar su acción al hacer clic en él) crea un problema de localización.

### <a name="navigation-links"></a>Vínculos de navegación

-   **Asegúrese de que los vínculos de navegación no requieren compromiso.** Los usuarios siempre deben poder volver al estado inicial, ya sea mediante el retroceso para la navegación en el lugar o cancelar para cerrar una nueva ventana.
-   **Vincular a contenido específico en lugar de a contenido general.** Por ejemplo, es mejor vincular a la sección relevante de un documento que vincular al principio.
-   **Use un vínculo solo si el material vinculado es relevante, útil y no redundante.** El uso de la retención en los vínculos de navegación no los usa solo porque puede.
-   **Si un vínculo navega a un sitio externo, coloque la dirección URL en el** recuadro informativo para que los usuarios puedan determinar el destino del vínculo.
-   **Vincule solo la primera aparición del texto del vínculo.** Los vínculos redundantes no son necesarios y pueden dificultar la lectura del texto.

    **Correcto:**

    La carpeta imágenes facilita el uso compartido de las imágenes. Puede usar las tareas de las imágenes para enviar imágenes por correo electrónico o publicarlas en una ubicación segura y privada en la Web. También puede imprimir las imágenes directamente desde la carpeta imágenes.

    **Incorrecto:**

    La carpeta imágenes facilita el uso compartido de las imágenes. Puede usar las tareas de las imágenes para enviar imágenes por correo electrónico o publicarlas en una ubicación segura y privada en la Web. También puede imprimir las imágenes directamente desde la carpeta imágenes.

    En el ejemplo correcto, solo se vincula la primera aparición del texto pertinente.

    **Excepciones:**

    -   **Si una instrucción tiene un vínculo, coloque el vínculo en la instrucción.**

        Es muy importante usar contraseñas seguras. Para obtener más información, consulte Contraseñas seguras.

        En este ejemplo, el vínculo está en la instrucción en lugar de en la primera aparición.

    -   **Vínculo a repeticiones posteriores si están lejos del primer.** Por ejemplo, puede vincular redundante en secciones diferentes dentro de un tema de ayuda.

### <a name="task-links"></a>Vínculos de tarea

-   **Use los vínculos de tarea para los comandos que no son destructivos o que son fácilmente reversibles.** Dado que los usuarios asocian vínculos con la navegación (y la capacidad de revertir), los vínculos no son adecuados para los comandos con consecuencias significativas. Los comandos que muestran un cuadro de diálogo o una confirmación son una buena opción.

    **Correcto:**

    Start

    Stop

    **Incorrecto:**

    Eliminar archivo

    En el ejemplo incorrecto, el comando es destructivo.

### <a name="menu-links"></a>Vínculos de menú

-   **Agrupe los vínculos de navegación y tareas relacionados en los menús.** Un menú de vínculos relacionados colocada dentro de una navegación estándar o una ubicación de comandos facilita la búsqueda y comprensión de los vínculos que cuando se colocan por separado.
-   **En el caso de los menús dependientes de la selección, quite los vínculos de menú que no se aplican.** No las deshabilite. Al hacerlo, se elimina el desorden y los usuarios no podrán echar vínculos que requieran selección.
-   **En el caso de los menús independientes de la selección, deshabilite los vínculos de menú que no se aplican.** No las quite. Esto hace que los menús sean más estables y que los vínculos sean más fáciles de encontrar.

    ![captura de pantalla del cuadro de diálogo con comando de menú atenuado ](images/ctrl-links-image15.png)

    En este ejemplo de Windows Update, se realiza una actualización, por lo que el comando Buscar actualizaciones está deshabilitado en lugar de quitarse.

### <a name="link-infotips"></a>Vincular recuadros informativos

-   Si un vínculo requiere una explicación más detallada, **proporcione la explicación en una explicación complementaria en un control de texto independiente o una** [sugerencia](ctrl-tooltips-and-infotips.md), pero no en ambas. Usar frases completas y puntuación final. Proporcionar ambos no es necesario si el texto es el mismo y confuso si el texto es diferente.

    ![captura de pantalla del vínculo con texto complementario ](images/ctrl-links-image16.png)

    En este ejemplo, una explicación complementaria proporciona más información sobre el vínculo.

    ![captura de pantalla del vínculo con recuadro informativo ](images/ctrl-links-image17.png)

    En este ejemplo, un recuadro informativo proporciona más información.

-   **No proporcione un recuadro informativo que es simplemente una reexpresión del texto del vínculo.**

    **Incorrecto:**

    ![captura de pantalla del vínculo con recuadro informativo redundante ](images/ctrl-links-image18.png)

    En este ejemplo, el recuadro informativo arriesga los usuarios molestos por su repetición.

## <a name="text"></a>Texto

-   No asigne una [clave de acceso](glossary.md). Se tiene acceso a los vínculos mediante la tecla TAB.
-   **Use los vínculos que proporcionan información descriptiva específica sobre el resultado de hacer clic en el vínculo**, utilizando tantos textos como sea necesario. El texto del vínculo debe indicar el resultado de hacer clic en el vínculo. **Los usuarios deben ser capaces de predecir con precisión el resultado de un vínculo desde el texto del vínculo y el recuadro informativo opcional.**

    **Incorrecto:**

    ![captura de pantalla de un vínculo de advertencia de aviso de seguridad ](images/ctrl-links-image19.png)

    En este ejemplo, aunque el vínculo parezca importante, su etiqueta es demasiado general. Es más probable que los usuarios haga clic en un vínculo más específico.

-   Para vínculos en línea:
    -   Conserva las mayúsculas y los signos de puntuación del texto.
    -   No incluya signos de puntuación finales en el vínculo a menos que el texto sea una pregunta.
    -   Vínculo en la parte más relevante del texto y elija el texto del vínculo que sea lo suficientemente grande como para que sea fácil de hacer clic.

        **Correcto:**

        Vaya a un grupo de noticias.

        **Incorrecto:**

        Vaya a un grupo de noticias.

        En estos ejemplos, "ir" no es la parte más relevante del texto y no es lo suficientemente grande como para crear un buen objetivo de clic, mientras que "grupo de noticias" es.

    -   **Evite colocar dos vínculos en línea diferentes entre sí.** Es probable que los usuarios creen que son un solo vínculo.

        **Incorrecto:**

        Para obtener más información, consulte las directrices de la experiencia del usuario.

        En este ejemplo, "UX" y "directrices" son dos vínculos diferentes.

-   Para vínculos independientes (no alineados):
    -   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
    -   No use la puntuación final a menos que el vínculo sea una pregunta.
    -   Use todo el texto como vínculo.
-   Use los vínculos que se diferencian claramente de los demás vínculos de la pantalla. Los usuarios deben poder predecir y diferenciar con precisión los destinos de los vínculos.

    **Incorrecto:**

    Buscar software antivirus

    Obtener software antivirus

    **Correcto:**

    Cómo saber si el software antivirus está instalado

    Instalación del software antivirus

    En el ejemplo incorrecto, la diferencia entre los dos vínculos no es clara.

-   No agregue clic o haga clic aquí para el texto del vínculo. No es necesario porque un vínculo implica hacer clic en. Además, haga clic aquí y aquí solo no se transmite información sobre el vínculo cuando lo lee un lector de pantalla.

    **Incorrecto:**

    Haga clic aquí para obtener una descripción.

    **Correcto:**

    Descripción

    En los ejemplos incorrectos, "haga clic aquí" va sin indicar y no transmite información sobre el vínculo.

**Vínculos de navegación**

-   **Inicie el vínculo con un sustantivo y describa claramente dónde irá haciendo clic en el vínculo.** No uses puntuación final. En ocasiones es posible que tenga que iniciar vínculos de navegación con un verbo, pero no usar verbos que reiteren la navegación que ya está implícita por el hecho de que la vinculación, como ver, abrir o ir a.
-   **Presente un vínculo de navegación como una dirección URL Si navega a una página web y espera que los usuarios de destino recuperen la dirección URL y la escriban en un explorador.** Si es posible, diseñe estas direcciones URL para que sean breves y fáciles de recordar.
-   **Si el vínculo incluye una dirección URL a un sitio web que empieza por "www", omita el nombre del protocolo https://y use texto en minúsculas.**

    **Incorrecto:**

    https://www.microsoft.com

    `www.microsoft.com`

    **Correcto:**

    microsoft.com

    En los ejemplos incorrectos, "https://" y "www" van sin decir.

**Vínculos de tarea**

-   **Inicie el vínculo con un verbo imperativo y describa claramente la tarea que realiza el vínculo.** No uses puntuación final.
-   **Finalice el vínculo con puntos suspensivos si el comando necesita información adicional (incluida una confirmación) para que se complete correctamente.** No use puntos suspensivos cuando la finalización correcta de la tarea sea Mostrar otra ventana solo cuando se necesite información adicional para realizar la tarea.

    Imprimir...

    En este ejemplo, se imprime... vínculo de comando muestra un cuadro de diálogo de impresión para recopilar más información.

    Impresión

    Por el contrario, en este ejemplo, un vínculo de comando de impresión imprime una única copia de un documento en la impresora predeterminada sin ninguna interacción adicional del usuario.

    **El uso correcto de las elipses es importante para indicar que los usuarios pueden tomar más opciones antes de realizar la tarea, o bien cancelar la tarea por completo**. La indicación visual ofrecida por un botón de puntos suspensivos permite a los usuarios explorar el software sin miedo.

-   **Si es necesario, finalice un vínculo de tarea con "Now" para distinguirlo de un vínculo de navegación.**

    Descarga de archivos

    Descargar archivos ahora

    En este ejemplo, "download files" navega a una página para descargar archivos, mientras que "download files Now" ejecuta el comando.

**Vínculos a la Ayuda**

Para obtener instrucciones y ejemplos, vea la [ayuda](winenv-help.md)de.

**Vincular recuadros informativos**

-   Usar oraciones completas y puntuación final.

Para obtener más instrucciones y ejemplos, vea [información sobre herramientas y recuadros informativos](ctrl-tooltips-and-infotips.md).

## <a name="documentation"></a>Documentación

Al hacer referencia a los vínculos:

-   Use el texto del vínculo exacto, incluido el uso de mayúsculas, pero no incluya los puntos suspensivos.
-   Para describir la interacción del usuario, use haga clic en.
-   Siempre que sea posible, dé formato al texto del vínculo usando texto en negrita. De lo contrario, coloque el texto del vínculo entre comillas solo si es necesario para evitar confusiones.

Ejemplo: para iniciar el examen, haga clic en **digitalizar un equipo**.

 


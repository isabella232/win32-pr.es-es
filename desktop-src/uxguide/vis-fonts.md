---
title: Fuentes
description: Los usuarios interactúan con texto más que con cualquier otro elemento de Microsoft Windows. Segoe UI (se pronuncia \ 0034; VEA-go \ 0034;) es la fuente del sistema de Windows. El tamaño de fuente estándar se ha aumentado a 9 puntos.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6c5fad1459d4ce45f2d677d4bd5864d89b125e4e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103819986"
---
# <a name="fonts"></a>Fuentes

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Los usuarios interactúan con texto más que con cualquier otro elemento de Microsoft Windows. Segoe UI (pronunciado "ver-ir") es la fuente del sistema de Windows. El tamaño de fuente estándar se ha aumentado a 9 puntos.

![Ilustración del alfabeto en la fuente Segoe UI ](images/vis-fonts-image1.png)

Fuente de Segoe UI.

Segoe UI y Segoe no son la misma fuente. Segoe UI es la fuente de Windows diseñada para las cadenas de texto de la interfaz de usuario. Segoe es una fuente de personalización de marca utilizada por Microsoft y sus asociados para generar material para impresión y publicidad.

Segoe UI es un tipo de letra accesible, abierto y descriptivo, y como resultado tiene una mejor legibilidad que Tahoma, Microsoft sans serif y Arial. Tiene las características de un Humanist sans serif: los distintos anchos de sus mayúsculas (E y S estrechos, por ejemplo, en comparación con Helvetica, donde los anchos son más similares, bastante ancho); el estrés y el letterforms de su minúsculas; y su verdadero en cursiva (en lugar de "oblicuo" o romano inclinado, al igual que muchos Sans Serif de aspecto industrial). El tipo de letra está pensado para dar el mismo efecto visual en la pantalla y en la impresión. Se diseñó para ser un Humanist sans serif sin ningún carácter seguro o distraera la peculiaridad.

Segoe UI está optimizado para ClearType, que está activado de forma predeterminada en Windows. Con ClearType habilitado, Segoe UI es una fuente elegante y legible. Sin ClearType habilitado, Segoe UI solo es aceptable en el margen. Este factor determina cuándo se debe utilizar Segoe UI.

Segoe UI incluye caracteres latinos, griego, cirílico y árabe. Hay nuevas fuentes, también optimizadas para ClearType, creadas para otros juegos de caracteres y usos. Entre estos se incluyen Meiryo para japonés, Malgun Gothic para Coreano, Microsoft JhengHei para chino (tradicional), Microsoft YaHei para chino (simplificado), Gisha para hebreo y Leelawadee para tailandés, y las fuentes de la colección ClearType diseñadas para su uso en documentos.

Meiryo incluye caracteres latinos basados en Verdana. Malgun Gothic, Microsoft JhengHei y Microsoft YaHei usan un Segoe UI personalizado. No se recomienda el uso de versiones en cursiva de estas fuentes. Malgun Gothic, Microsoft JhengHei y Microsoft YaHei se proporcionan únicamente en los estilos normal y negrita, lo que significa que los caracteres en cursiva se sintetizan inclinando los estilos verticales. Aunque Meiryo incluye true cursiva y negrita cursiva, estos estilos solo se aplican a los caracteres latinos que los caracteres japoneses permanecen verticales cuando se aplica el estilo de cursiva.

Se prefiere una variación de Meiryo, denominada Meiryo UI, en la interfaz de usuario de comandos de la [cinta](cmd-ribbons.md) de opciones.

Para admitir configuraciones regionales con estos juegos de caracteres, Segoe UI se reemplaza con las fuentes correctas en función de cada configuración regional durante el proceso de [localización](glossary.md) .

Para obtener una licencia Segoe UI y otras fuentes de Microsoft para la distribución con un programa basado en Windows, póngase en contacto con [Monotype](https://www.monotype.com/).

**Nota:** Las instrucciones relacionadas con el [estilo y el tono](text-style-tone.md) y el texto de la [interfaz de usuario](text-ui.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Fuentes, tipos de letra, tamaños de punto y atributos

En la tipografía tradicional, una fuente describe una combinación de un tipo de letra, un tamaño de punto y atributos. Un tipo de letra es la apariencia de la fuente. Segoe UI, Tahoma, Verdana y Arial son todos los tipos de letra. El tamaño de punto hace referencia al tamaño de la fuente, medido desde la parte superior de los ascendentes hasta la parte inferior de los descendentes, menos el espaciado interno (llamado interlineado). Un punto es aproximadamente 1/72 de pulgada. Por último, una fuente puede tener atributos de negrita o cursiva.

De manera informativa, las personas suelen usar la fuente en lugar de tipo de letra como se hace en este artículo, pero técnicamente, Segoe UI es un tipo de letra, no una fuente. Cada combinación de atributos es una fuente única (por ejemplo, 9 puntos Segoe UI normal, 10 puntos Segoe UI negrita, etc.).

### <a name="serif-and-sans-serif"></a>Serif y sans serif

Los tipos de letra son Serif o sans serif. Serif hace referencia a pequeñas vueltas que suelen acabar con los trazos de las letras de una fuente. Un tipo de letra sans serif no tiene serifs.

Por lo general, los lectores prefieren usar fuentes serif como texto de cuerpo dentro de un documento. Los serifs proporcionan una sensación de formalidad y elegancia a un documento. En el caso del texto de la interfaz de usuario, la necesidad de una apariencia limpia y la resolución más baja de los monitores del equipo hace que los tipos de letra sans serif sean la mejor opción.

### <a name="contrast"></a>Compare

El texto es más fácil de leer cuando hay una gran diferencia entre la luminancia del texto y el fondo. El texto negro sobre un fondo blanco permite que el texto oscuro de contraste superior de un fondo muy claro también ofrezca un contraste alto. Esta combinación es mejor para las superficies de la interfaz de usuario principal.

El texto claro de un fondo oscuro ofrece un buen contraste, pero no tan bueno como el texto oscuro sobre un fondo claro. Esta combinación funciona bien para las superficies de la interfaz de usuario secundaria, como los paneles de tareas del explorador, que desea desenfatizar en relación con las superficies de la interfaz de usuario principal.

**Si desea asegurarse de que los usuarios lean el texto, use texto oscuro sobre un fondo claro.**

### <a name="affordances"></a>Prestaciones

El texto puede utilizar las siguientes [prestaciones](glossary.md) para indicar cómo se utiliza:

-   **Puntero.** El puntero de barra I ("selección de texto") indica que el texto es seleccionable, mientras que el puntero de la flecha que señala a la izquierda ("Selección normal") indica que el texto no es.
-   **Intercalación.** Cuando el texto tiene el foco de entrada, el símbolo de intercalación es la barra vertical parpadeante que indica el punto de inserción/selección en texto seleccionable o editable.
-   **Cuadro.** Cuadro alrededor del texto que indica que es editable. Para reducir el peso de la presentación, el cuadro se puede mostrar dinámicamente solo cuando se selecciona el texto editable.
-   **Color de primer plano.** El color gris claro indica que el texto está deshabilitado. Los colores no grises, especialmente el azul y el púrpura, indican que el texto es un vínculo.
-   **Color de fondo.** Un fondo gris claro sugiere de forma débil que el texto es de solo lectura, pero en la práctica el texto de solo lectura puede tener cualquier fondo de color.

Estas prestaciones se combinan para los significados siguientes:

-   **Edita.** Texto que se muestra en un cuadro, con un puntero de selección de texto, un símbolo de intercalación (en el foco de entrada) y, normalmente, en un fondo blanco.
-   **Solo lectura, seleccionable.** Texto con un puntero de selección y un símbolo de intercalación (en el foco de entrada).
-   **Solo lectura, no seleccionable.** Texto con un puntero de flecha.
-   **Deshabilitado.** Texto gris claro con un puntero de flecha, a veces en un fondo gris.

El texto de solo lectura tradicionalmente tiene un fondo gris, pero no es necesario un fondo gris. De hecho, un fondo gris puede ser no deseable, especialmente para grandes bloques de texto, porque sugiere que el texto está deshabilitado y desaconseja la lectura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Accesibilidad y la fuente del sistema, tamaños y colores

Las instrucciones para hacer que el texto sea accesible para los usuarios con discapacidades o discapacidades se puede reducir a una regla simple: respete la configuración del usuario usando siempre la fuente, los tamaños y los colores del sistema.

**Si solo hace algo...**

Respete la configuración del usuario usando siempre la fuente, los tamaños y los colores del sistema.

**Desarrolladores:** Desde el código, puede determinar las propiedades de la fuente del sistema (incluido su tamaño) mediante la función de la API GetThemeFont. Puede determinar los colores del sistema mediante la función de la API GetThemeSysColor.

Dado que no puede hacer ninguna suposición sobre la configuración de temas del sistema de los usuarios, debe:

-   Siempre debe basar los colores de fuente y el fondo de los colores del tema del sistema. Nunca cree sus propios colores en función de los valores de RGB fijos (rojo, verde y azul).
-   Coincide siempre con los colores de texto del sistema con sus colores de fondo correspondientes. Por ejemplo, si elige \_ STATICTEXT de color para el color del texto, también debe elegir \_ el color estático para el color de fondo.
-   Cree siempre nuevas fuentes basadas en variaciones de tamaño proporcional de la fuente del sistema. Dadas las métricas de fuentes del sistema, puede crear las variaciones en negrita, cursiva, más grande y más pequeñas.

**Una manera sencilla de asegurarse de que el programa respeta la configuración de los usuarios es probar con un tamaño de fuente diferente y una combinación de colores de contraste alto.** Todo el texto debe cambiar de tamaño y mostrarse correctamente en la combinación de colores elegida.

## <a name="usage-patterns"></a>Patrones de uso

El texto tiene varios patrones de uso:



|                                                                                                                                                                                                                                                           |                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto de la barra de título**<br/> Texto en la barra de título que identifica la ventana.<br/>                                                                                                                                                                | ![ejemplo de fuente de texto de barra de título ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Instrucciones principales**<br/> Texto que explica lo que se debe hacer en una página, ventana o cuadro de diálogo. <br/>                                                                                                                                              | ![ejemplo de fuente de texto de instrucciones principales ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Instrucciones secundarias**<br/> Texto complementario que explica lo que se debe hacer en una página, ventana o cuadro de diálogo. <br/>                                                                                                                            | ![ejemplo de fuente de texto de instrucciones secundarias ](images/vis-fonts-image4.png)<br/>                                                               |
| **Texto normal**<br/> Texto normal (de solo lectura) que se muestra en una interfaz de usuario. <br/>                                                                                                                                                           | ![ejemplo de fuente de texto normal ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Texto resaltado**<br/> El texto en negrita se usa para facilitar el análisis del texto y atraer la atención a los usuarios de texto que deben leer. el texto en cursiva se usa para hacer referencia literalmente al texto (en lugar de a las comillas) y para resaltar palabras específicas. <br/> | ![ejemplo de fuente de texto resaltado ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Texto editable**<br/> El texto que los usuarios pueden editar se muestra en un cuadro. para reducir el peso de la presentación, el cuadro solo se puede mostrar cuando se selecciona el texto editable. <br/>                                                          | ![ejemplo de fuente de texto modificable ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Texto deshabilitado**<br/> Texto que no se aplica al contexto actual, como etiquetas para los controles deshabilitados. el texto deshabilitado indica que los usuarios (normalmente) no deberían molestarse en leer el texto. <br/>                                           | ![ejemplo de fuente de texto deshabilitado ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Vínculos**<br/> Texto que se usa para navegar a otra página, ventana o tema de ayuda, o iniciar un comando. <br/>                                                                                                                                     | ![ejemplo de fuente de texto de vínculo ](images/vis-fonts-image9.png)<br/> ![ejemplo de la fuente de texto de vínculos (mantener el mouse) ](images/vis-fonts-image10.png)<br/> |
| **Encabezado de grupo**<br/> Texto que se utiliza para agrupar elementos en una vista de lista. <br/>                                                                                                                                                                          | ![ejemplo de fuente de texto de encabezado de grupo ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nombre de archivo**<br/> Texto del nombre de archivo (solo en la vista de contenido). <br/>                                                                                                                                                                               | ![ejemplo de nombre de archivo (en la vista de contenido) fuente de texto ](images/vis-fonts-image12.png)<br/>                                                         |
| **Texto del documento**<br/> Texto que se usa en los documentos (en lugar del texto de la interfaz de usuario). <br/>                                                                                                                                                                  | ![ejemplo de fuente de texto de documento ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Encabezados de documento**<br/> Texto que se usa como encabezado dentro de un documento. <br/>                                                                                                                                                                    | ![ejemplo de fuente de texto de encabezados de documento ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Directrices

### <a name="fonts-and-colors"></a>Fuentes y colores

-   **Las siguientes fuentes y colores son valores predeterminados para Windows Vista y Windows 7.**



|                                                                                               |                             |                                                            |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| **Patrón**<br/>                                                                        | **Símbolo de tema**<br/> | **Fuente, color**<br/>                                 |
| ![ejemplo de fuente de texto de barra de título ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto de instrucciones principales ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt. Segoe UI azul ( \# 003399)<br/>                 |
| ![ejemplo de fuente de texto de instrucciones secundarias ](images/vis-fonts-image4.png)<br/>       | Instrucción<br/>      | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto normal ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto resaltado ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt. Black ( \# 000000) Segoe UI, negrita o cursiva<br/> |
| ![ejemplo de fuente de texto modificable ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt. negro ( \# 000000) Segoe UI, en un cuadro<br/>       |
| ![ejemplo de fuente de texto deshabilitado ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 pt. Segoe UI gris oscuro ( \# 323232)<br/>             |
| ![ejemplo de fuente de texto de vínculo ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt. Segoe UI azul ( \# 0066CC)<br/>                  |
| ![ejemplo de la fuente de texto de vínculos (mantener el mouse) ](images/vis-fonts-image10.png)<br/>               | Acceso frecuente<br/>              | 9 pt. Segoe UI azul claro ( \# 3399FF)<br/>            |
| ![ejemplo de fuente de texto de encabezado de grupo ](images/vis-fonts-image11.png)<br/>                |                             | 11 pt. Segoe UI azul ( \# 003399)<br/>                 |
| ![ejemplo de nombre de archivo (en la vista de contenido) fuente de texto ](images/vis-fonts-image12.png)<br/> |                             | 11 pt. negro ( \# 000000) Segoe UI<br/>                |
| ![ejemplo de fuente de texto de documento ](images/vis-fonts-image13.png)<br/>                    | (ninguno)<br/>           | 9 pt. negro ( \# 000000) Calibri<br/>                  |
| ![ejemplo de fuente de texto de encabezados de documento ](images/vis-fonts-image14.png)<br/>           | (ninguno)<br/>           | 17 PT. negro ( \# 000000) Calibri<br/>                 |



 

-   **Elija fuentes y optimice los diseños de ventana en función de la tecnología de interfaz de usuario y la versión de destino de Windows:**



|                                            |                                                       |                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tecnología de interfaz de usuario**<br/>               | **Versión de Windows de destino**<br/>                 | **Fuentes para usar y optimizar para**<br/>                                                                                                                                                                                                                                                                                                                     |
| Windows Presentation Foundation<br/> | All<br/>                                        | Usar partes del tema de WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 o WinForms<br/>               | Windows Vista o posterior<br/>                     | Use la fuente de Segoe UI adecuada.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Componentes extensibles o anteriores a Windows Vista<br/> | Para tener como destino Windows XP y Windows 2000, use la pseudo fuente MS Shell Dlg 2 de 8 puntos, que se asigna a Tahoma.<br/> Para tener como destino versiones anteriores de Windows, use la pseudo fuente MS Shell Dlg de 8 puntos, que se asigna a Tahoma en Windows 2000 y Windows XP, y a MS Sans Serif en Windows 95, Windows 98, Windows Millennium Edition y Windows NT 4,0.<br/> |



 

-   **Developer**
    -   En el caso de los elementos que usan el diseño fijo (como las plantillas de cuadro de diálogo de Windows y WinForms), codifique la fuente adecuada de la tabla anterior.
    -   En el caso de los elementos que utilizan el diseño dinámico (como Windows Presentation Foundation), use las fuentes del tema. Use las API de tema como DrawThemeText para dibujar texto basado en el símbolo de tema. Asegúrese de tener una alternativa basada en las métricas del sistema en caso de que el servicio de tema no se esté ejecutando.
-   **En Segoe UI, use un tamaño de fuente de 9 puntos o mayor.** La fuente Segoe UI está optimizada para estos tamaños, así que evite el uso de tamaños menores.
-   **Coincide siempre con los colores de texto del sistema con sus colores de fondo correspondientes.** Por ejemplo, si elige \_ STATICTEXT de color para el color del texto, también debe elegir \_ el color estático para el color de fondo.
-   **Cree siempre nuevas fuentes basadas en variaciones de tamaño proporcional de la fuente del sistema.** Dadas las métricas de fuentes del sistema, puede crear las variaciones en negrita, cursiva, más grande y más pequeñas.
-   Muestra grandes bloques de texto de solo lectura (como los términos de licencia) en un fondo claro en lugar de un fondo gris. Los fondos grises sugieren que el texto está deshabilitado y desaconseja la lectura.
-   **Considere una longitud de línea máxima de 65 caracteres** para facilitar la lectura del texto. (Entre los caracteres se incluyen letras, signos de puntuación y espacios).

### <a name="attributes"></a>Atributos

-   La mayoría del texto de la interfaz de usuario no debe ser normal sin ningún atributo. Los atributos se pueden usar de la siguiente manera:
    -   **Poner.** Use en etiquetas de control para facilitar el análisis del texto. Use con moderación para atraer la atención a los usuarios de texto que deben leer. El uso excesivo de negrita reduce su impacto.
    -   **Aplicar.** Use para hacer referencia a texto literalmente en lugar de Comillas. Use con moderación para resaltar palabras específicas. [Se](glossary.md) usa para los mensajes en [cuadros de texto](ctrl-text-boxes.md) y [listas desplegables modificables](/windows/desktop/uxguide/ctrl-drop).
    -   **Negrita cursiva.** No use.
    -   **Raya.** No utilice excepto para los vínculos. Use cursiva en lugar de énfasis.
-   No todas las fuentes admiten negrita y cursiva, por lo que nunca deben ser cruciales para comprender el texto.


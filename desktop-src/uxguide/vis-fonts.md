---
title: Fuentes
description: Los usuarios interactúan con texto más que con cualquier otro elemento de Microsoft Windows. Segoe UI (se pronuncia \ 0034; SEE-go \ 0034;) es la Windows fuente del sistema. El tamaño de fuente estándar se ha aumentado a 9 puntos.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ac9f725349433f1cd5f2070b0c80d86acb9d8b3f4d9537cc14375d977283620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816580"
---
# <a name="fonts"></a>Fuentes

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Los usuarios interactúan con texto más que con cualquier otro elemento de Microsoft Windows. Segoe UI (que se pronuncia "SEE-go") es la fuente Windows del sistema. El tamaño de fuente estándar se ha aumentado a 9 puntos.

![ilustración del alfabeto en la fuente segoe ui ](images/vis-fonts-image1.png)

La Segoe UI fuente.

Segoe UI y Segoe no son la misma fuente. Segoe UI es la fuente Windows para las cadenas de texto de la interfaz de usuario. Segoe es una fuente de personal de marca utilizada por Microsoft y asociados para producir material para impresión y publicidad.

Segoe UI es un tipo de letra fácil de abordar, abierto y descriptivo y, como resultado, tiene una mejor legibilidad que Sioma, Microsoft Sans Serif y Arial. Tiene las características de un humanista sans serif: los distintos anchos de sus mayúsculas (E y S estrechos, por ejemplo, en comparación con Helvetica, donde los anchos son más iguales, bastante anchos); el esfuerzo y las formas de letra de su minúscula; y su verdadera cursiva (en lugar de un "oblique" o un román inclinado, como muchos sans serifs de aspecto industrial). El tipo de letra está diseñado para dar el mismo efecto visual en la pantalla y en la impresión. Se diseñó para ser un sans serif humanista sin ningún carácter fuerte ni una rareza distraída.

Segoe UI está optimizado para ClearType, que está on de forma predeterminada en Windows. Con ClearType habilitado, Segoe UI es una fuente elegante y legible. Sin ClearType habilitado, Segoe UI solo es marginalmente aceptable. Este factor determina cuándo se debe usar Segoe UI.

Segoe UI incluye caracteres latinos, griegos, cirílicos y árabes. Hay nuevas fuentes, también optimizadas para ClearType, creadas para otros juegos de caracteres y usos. Entre ellas se incluyen Meiryo para japonés, Malgun Deserción para coreano, Microsoft JhengMelo para chino (tradicional), Microsoft YaMelo para chino (simplificado), Gjj para hebreo y Leelawadee para tailandés y las fuentes clearType Collection diseñadas para el uso de documentos.

Meiryo incluye caracteres latinos basados en Verdana. Malgun, Microsoft JhengForma y Microsoft YaHi usan un Segoe UI. No se recomienda el uso de versiones en cursiva de estas fuentes. Malgun Italic, Microsoft Jheng Byte y Microsoft YaRang solo se proporcionan en estilos normales y en negrita, lo que significa que los caracteres cursiva se sintetizan inclinando los estilos de estilo vertical. Aunque Meiryo incluye cursiva verdadera y cursiva en negrita, estos estilos solo se aplican a los caracteres latinos que los caracteres japoneses permanecen verticales cuando se aplica el estilo cursiva.

Se prefiere una variación de Meiryo, denominada meiryo UI, en la interfaz de usuario del comando [ribbons.](cmd-ribbons.md)

Para admitir configuraciones regionales mediante estos conjuntos de caracteres, Segoe UI se reemplaza por las fuentes correctas en función de cada configuración regional durante el [proceso de](glossary.md) localización.

Para obtener Segoe UI y otras fuentes de Microsoft para su distribución con un programa basado en Windows, póngase en contacto con [Monotype](https://www.monotype.com/).

**Nota:** Las instrucciones relacionadas con [el estilo y el tono](text-style-tone.md) y el texto de la interfaz de [usuario](text-ui.md) se presentan en artículos independientes.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Fuentes, tipos de letra, tamaños de punto y atributos

En la tipografía tradicional, una fuente describe una combinación de un tipo de letra, un tamaño de punto y atributos. Un tipo de letra es el aspecto de la fuente. Segoe UI,Metoma, Verdana y Arial son tipos de letra. El tamaño de punto hace referencia al tamaño de la fuente, medido desde la parte superior de los descendientes hasta la parte inferior de los descendientes, menos el espaciado interno (denominado inicial). Un punto es aproximadamente de 1/72 pulgadas. Por último, una fuente puede tener atributos de negrita o cursiva.

Informalmente, las personas suelen usar la fuente en lugar del tipo de letra, como se hace en este artículo, pero técnicamente, Segoe UI es un tipo de letra, no una fuente. Cada combinación de atributos es una fuente única (por ejemplo, 9 puntos Segoe UI normal, 10 puntos Segoe UI negrita, y así sucesivamente).

### <a name="serif-and-sans-serif"></a>Serif y sans serif

Los tipos de letra son serif o sans serif. Serif hace referencia a pequeños turnos que a menudo finalizan los trazos de letras de una fuente. Un tipo de letra sans serif no tiene serifs.

Por lo general, los lectores prefieren fuentes serif usadas como texto del cuerpo dentro de un documento. Los serifs proporcionan una sensación de formalidad y comodidad a un documento. Para el texto de la interfaz de usuario, la necesidad de una apariencia limpia y la menor resolución de los monitores de equipo hace que los tipos de letra sans serif sea la mejor opción.

### <a name="contrast"></a>Compare

El texto es más fácil de leer cuando hay una gran diferencia entre la luminosidad del texto y el fondo. El texto negro sobre un fondo blanco proporciona el texto oscuro de contraste más alto en un fondo muy claro también puede proporcionar contraste alto. Esta combinación es mejor para las superficies de interfaz de usuario principales.

El texto claro en un fondo oscuro ofrece un buen contraste, pero no tan bueno como el texto oscuro en un fondo claro. Esta combinación funciona bien para las superficies secundarias de la interfaz de usuario, como los paneles de tareas del Explorador, que desea desacentr en relación con las superficies principales de la interfaz de usuario.

**Si desea asegurarse de que los usuarios leen el texto, use texto oscuro sobre un fondo claro.**

### <a name="affordances"></a>Asequiciones

El texto puede usar las [siguientes asequiciones](glossary.md) para indicar cómo se usa:

-   **Puntero.** El puntero de la barra I ("selección de texto") indica que el texto se puede seleccionar, mientras que el puntero de flecha hacia la izquierda ("selección normal") indica que el texto no lo es.
-   **Intercalación.** Cuando el texto tiene el foco de entrada, el elemento de inserción es la barra vertical parpadeante que indica el punto de inserción o selección en texto seleccionable o modificable.
-   **Caja.** Cuadro alrededor del texto que indica que es editable. Para reducir el peso de la presentación, el cuadro solo se puede mostrar dinámicamente cuando se selecciona el texto modificable.
-   **Color de primer plano.** El color gris claro indica que el texto está deshabilitado. Los colores no grises, especialmente azul y púrpura, indican que el texto es un vínculo.
-   **Color de fondo.** Un fondo gris claro sugiere débilmente que el texto es de solo lectura, pero en la práctica el texto de solo lectura puede tener cualquier fondo de color.

Estas asequiciones se combinan para los significados siguientes:

-   **Editable.** Texto que se muestra en un cuadro, con un puntero de selección de texto, un cursor de subrayado (en el foco de entrada) y normalmente sobre un fondo blanco.
-   **De solo lectura, seleccionable.** Texto con un puntero de selección y un cursor de cursor (en el foco de entrada).
-   **De solo lectura, no seleccionable.** Texto con un puntero de flecha.
-   **Deshabilitado.** Texto gris claro con un puntero de flecha, a veces sobre un fondo gris.

El texto de solo lectura tradicionalmente tiene un fondo gris, pero no es necesario un fondo gris. De hecho, no se puede desear un fondo gris, especialmente para grandes bloques de texto, porque sugiere que el texto está deshabilitado y desaconseja la lectura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Accesibilidad y la fuente, tamaños y colores del sistema

Las directrices para hacer que el texto sea accesible para los usuarios con discapacidades o discapacidades se pueden convertir en una regla sencilla: Respetar la configuración del usuario usando siempre la fuente, los tamaños y los colores del sistema.

**Si solo hace una cosa...**

Respeta la configuración del usuario usando siempre la fuente, los tamaños y los colores del sistema.

**Desarrolladores:** A partir del código, puede determinar las propiedades de fuente del sistema (incluido su tamaño) mediante la función de API GetThemeFont. Puede determinar los colores del sistema mediante la función de API GetThemeSysColor.

Dado que no se puede hacer ninguna suposición sobre la configuración del tema del sistema de los usuarios, debe:

-   Base siempre los colores de fuente y los fondos de los colores del tema del sistema. Nunca haga sus propios colores basados en valores RGB fijos (rojo, verde, azul).
-   Coincide siempre con los colores de texto del sistema con sus colores de fondo correspondientes. Por ejemplo, si elige COLOR STATICTEXT para el color de texto, también debe elegir \_ COLOR STATIC para el color de \_ fondo.
-   Cree siempre nuevas fuentes basadas en variaciones de tamaño proporcional de la fuente del sistema. Dadas las métricas de fuente del sistema, puede crear variaciones en negrita, cursiva, más grandes y más pequeñas.

**Una manera sencilla de asegurarse de que el programa respeta la configuración de los usuarios es probar con un tamaño de fuente diferente y una combinación de colores de contraste alto.** Todo el texto debe cambiar de tamaño y mostrarse correctamente en la combinación de colores elegida.

## <a name="usage-patterns"></a>Patrones de uso

El texto tiene varios patrones de uso:



|    Uso                                         |    Descripción                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto de la barra de título**<br/> Texto en la barra de título que identifica la ventana.<br/>                                                                                                                                                                | ![ejemplo de fuente de texto de barra de título ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Instrucciones principales**<br/> Texto que explica qué hacer en una página, ventana o cuadro de diálogo. <br/>                                                                                                                                              | ![ejemplo de fuente de texto de instrucciones principales ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Instrucciones secundarias**<br/> Texto complementario que explica qué hacer en una página, ventana o cuadro de diálogo. <br/>                                                                                                                            | ![ejemplo de fuente de texto de instrucciones secundarias ](images/vis-fonts-image4.png)<br/>                                                               |
| **Texto normal**<br/> Texto normal (de solo lectura) que se muestra en una interfaz de usuario. <br/>                                                                                                                                                           | ![ejemplo de fuente de texto normal ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Texto resaltado**<br/> El texto en negrita se usa para facilitar el análisis del texto y llamar la atención sobre el texto que los usuarios deben leer. El texto cursiva se usa para hacer referencia al texto literalmente (en lugar de comillas) y para resaltar palabras específicas. <br/> | ![ejemplo de fuente de texto resaltada ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Texto editable**<br/> El texto que los usuarios pueden editar se muestra en un cuadro. Para reducir el peso de la presentación, el cuadro solo se puede mostrar cuando se selecciona el texto modificable. <br/>                                                          | ![ejemplo de fuente de texto editable ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Texto deshabilitado**<br/> Texto que no se aplica al contexto actual, como las etiquetas de los controles deshabilitados. el texto deshabilitado indica que los usuarios (normalmente) no deben preocuparse de leer el texto. <br/>                                           | ![ejemplo de fuente de texto deshabilitada ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Vínculos**<br/> Texto que se usa para navegar a otra página, ventana o tema de ayuda, o iniciar un comando. <br/>                                                                                                                                     | ![ejemplo de fuente de texto de vínculo ](images/vis-fonts-image9.png)<br/> ![ejemplo de fuente de texto de vínculos (mantener el puntero) ](images/vis-fonts-image10.png)<br/> |
| **Encabezado de grupo**<br/> Texto utilizado para agrupar elementos en una vista de lista. <br/>                                                                                                                                                                          | ![ejemplo de fuente de texto de encabezado de grupo ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nombre de archivo**<br/> Texto del nombre de archivo (solo en la vista de contenido). <br/>                                                                                                                                                                               | ![ejemplo de fuente de texto de nombre de archivo (en la vista de contenido) ](images/vis-fonts-image12.png)<br/>                                                         |
| **Texto del documento**<br/> Texto usado en documentos (en lugar de texto de interfaz de usuario). <br/>                                                                                                                                                                  | ![ejemplo de fuente de texto del documento ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Encabezados de documento**<br/> Texto usado como encabezado dentro de un documento. <br/>                                                                                                                                                                    | ![ejemplo de fuente de texto de encabezados de documento ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Directrices

### <a name="fonts-and-colors"></a>Fuentes y colores

-   **Las siguientes fuentes y colores son los valores predeterminados para Windows Vista y Windows 7.**



| Patrón | Símbolo de tema | Fuente, Color |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![ejemplo de fuente de texto de barra de título ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto de instrucciones principales ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt. blue \# (003399) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto de instrucciones secundarias ](images/vis-fonts-image4.png)<br/>       | Instrucción<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto normal ](images/vis-fonts-image5.png)<br/>                       | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto resaltada ](images/vis-fonts-image6.png)<br/>                   | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, negrita o cursiva<br/> |
| ![ejemplo de fuente de texto editable ](images/vis-fonts-image7.png)<br/>                     | BodyText<br/>         | 9 pt. negro \# (000000) Segoe UI, en un cuadro<br/>       |
| ![ejemplo de fuente de texto deshabilitada ](images/vis-fonts-image8.png)<br/>                     | Disabled<br/>         | 9 pt. gris oscuro \# (323232) Segoe UI<br/>             |
| ![ejemplo de fuente de texto de vínculo ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt. blue \# (0066CC) Segoe UI<br/>                  |
| ![ejemplo de fuente de texto de vínculos (mantener el puntero) ](images/vis-fonts-image10.png)<br/>               | Acceso frecuente<br/>              | 9 pt. azul claro \# (3399FF) Segoe UI<br/>            |
| ![ejemplo de fuente de texto de encabezado de grupo ](images/vis-fonts-image11.png)<br/>                |                             | 11 pt. blue \# (003399) Segoe UI<br/>                 |
| ![ejemplo de fuente de texto de nombre de archivo (en la vista de contenido) ](images/vis-fonts-image12.png)<br/> |                             | 11 pt. black ( \# 000000) Segoe UI<br/>                |
| ![ejemplo de fuente de texto del documento ](images/vis-fonts-image13.png)<br/>                    | (ninguno)<br/>           | 9 pt. black ( \# 000000) Calibri<br/>                  |
| ![ejemplo de fuente de texto de encabezados de documento ](images/vis-fonts-image14.png)<br/>           | (ninguno)<br/>           | 17 pt. black ( \# 000000) Calibri<br/>                 |



 

-   **Elija fuentes y optimice los diseños de ventana en función de la tecnología de interfaz de usuario y la versión de destino Windows:**



| Tecnología de interfaz de usuario | Versión de Windows destino | Fuentes para las que usar y optimizar |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | Todo<br/>                                        | Usar elementos de tema de WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 o WinForms<br/>               | Windows Vista o posterior<br/>                     | Use la fuente Segoe UI adecuada.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Componentes extensibles o versiones Windows Vista<br/> | Para usar Windows XP y Windows 2000, use la pseudo font dlg 2 de MS Shell de 8 puntos, que se asigna aInfooma.<br/> Para dirigirse a versiones anteriores de Windows, use la pseudo font dlg de MS Shell de 8 puntos, que se asigna aLcoma en Windows 2000 y Windows XP, y a MS Sans Serif en Windows 95, Windows 98, Windows Edition Edition y Windows NT 4.0.<br/> |



 

-   **Desarrolladores:**
    -   En el caso de los elementos que usan un diseño fijo (como Windows de diálogo y WinForms), codifie de forma fija la fuente adecuada de la tabla anterior.
    -   Para los elementos que usan el diseño dinámico (como Windows Presentation Foundation), use las fuentes de tema. Use API de tema como DrawThemeText para dibujar texto basado en el símbolo de tema. Asegúrese de tener una alternativa basada en las métricas del sistema en caso de que el servicio de tema no se esté ejecutando.
-   **Para Segoe UI, use un tamaño de fuente de 9 puntos o mayor.** La fuente Segoe UI está optimizada para estos tamaños, por lo que debe evitar el uso de tamaños más pequeños.
-   **Coincide siempre con los colores de texto del sistema con sus colores de fondo correspondientes.** Por ejemplo, si elige COLOR STATICTEXT para el color de texto, también debe elegir \_ COLOR STATIC para el color de \_ fondo.
-   **Cree siempre nuevas fuentes basadas en variaciones de tamaño proporcional de la fuente del sistema.** Dadas las métricas de fuente del sistema, puede crear variaciones en negrita, cursiva, más grandes y más pequeñas.
-   Mostrar grandes bloques de texto de solo lectura (como términos de licencia) en un fondo claro en lugar de un fondo gris. Los fondos grises sugieren que el texto está deshabilitado y desaconseja la lectura.
-   **Considere una longitud de línea máxima de 65 caracteres** para facilitar la lectura del texto. (Los caracteres incluyen letras, signos de puntuación y espacios).

### <a name="attributes"></a>Atributos

-   La mayoría del texto de la interfaz de usuario debe ser sin formato sin ningún atributo. Los atributos se pueden usar de la siguiente manera:
    -   **Negrita.** Use en etiquetas de control para facilitar el análisis del texto. Use con moderación para llamar la atención sobre el texto que los usuarios deben leer. El uso de demasiada negrita abate su impacto.
    -   **Cursiva.** Use para hacer referencia al texto literalmente en lugar de comillas. Use con moderación para resaltar palabras específicas. Use para [avisos en](glossary.md) cuadros [de texto](ctrl-text-boxes.md) y [listas desplegables editables.](/windows/desktop/uxguide/ctrl-drop)
    -   **Negrita cursiva.** No lo use.
    -   **Subrayar.** No use excepto los vínculos. Use cursiva en su lugar para el énfasis.
-   No todas las fuentes admiten negrita y cursiva, por lo que nunca deben ser fundamentales para comprender el texto.


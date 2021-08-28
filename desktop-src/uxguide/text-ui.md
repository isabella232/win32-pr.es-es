---
title: Interfaz de usuario text
description: Obtenga información sobre el texto de la interfaz de usuario que aparece en las superficies de la interfaz de usuario.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0d1d9a6166a6a0a0f0dae267ce6c0eda0d901d0d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982738"
---
# <a name="user-interface-text"></a>Interfaz de usuario text

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

El texto de la interfaz de usuario aparece en las superficies de la interfaz de usuario. Este texto incluye etiquetas de control y texto estático:

-   Las etiquetas de control identifican los controles y se colocan directamente en los controles o junto a ellos.
-   El texto estático, que se denomina así porque no forma parte de un control interactivo, proporciona a los usuarios instrucciones o explicaciones detalladas para que puedan tomar decisiones informadas.

**Nota:** Las instrucciones relacionadas con [el estilo y el tono,](text-style-tone.md) [las](vis-fonts.md)fuentes y [las etiquetas de control comon](controls.md) se presentan en artículos independientes.

## <a name="usage-patterns"></a>Patrones de uso

El texto de la interfaz de usuario tiene varios patrones de uso:



|   Uso                                                                                                                                                                                          |    Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto de la barra de título**<br/> use texto de la barra de título para identificar una ventana o el origen de un cuadro de diálogo. <br/>                                                                            | ![captura de pantalla de la barra de título de opciones de carpeta](images/text-ui-image1.png)<br/> En este ejemplo, el texto de la barra de título identifica una ventana.<br/>                                                                                                                                                                                                                                                                                                             |
| **Instrucciones principales**<br/> use la instrucción principal destacada para explicar concisamente qué hacer en la ventana o página. <br/>                                                      | La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. Las instrucciones principales buenas comunican el objetivo del usuario en lugar de centrarse solo en manipular la interfaz de usuario. <br/> ![captura de pantalla de la pregunta: ¿desea la ayuda más reciente? ](images/text-ui-image2.png)<br/> En este ejemplo, el texto de instrucción principal interactúa directamente con el usuario con una pregunta en términos de beneficio o interés propios del usuario.<br/>             |
| **Instrucciones complementarias**<br/> cuando sea necesario, use una instrucción complementaria para presentar información adicional útil para comprender o usar la ventana o página. <br/> | Puede proporcionar información más detallada, proporcionar contexto y definir terminología. instrucciones complementarias que se elaboran en la instrucción principal sin simplemente volver a elaborarla. <br/> ![captura de pantalla de texto al cambiar a la cuenta de administrador ](images/text-ui-image3.png)<br/> En este ejemplo, las instrucciones complementarias proporcionan dos posibles cursos de acción que deben realizarse en respuesta a la información presentada en la instrucción principal.<br/> |
| **Etiquetas de control**<br/> etiquetas directamente en los controles o junto a ellos. <br/>                                                                                                           | ![captura de pantalla de las opciones de reloj de escritorio ](images/text-ui-image4.png)<br/> En este ejemplo, las etiquetas de control identifican la configuración del reloj de escritorio que los usuarios pueden seleccionar o modificar.<br/>                                                                                                                                                                                                                                                                       |
| **Explicaciones complementarias**<br/> una elaboración de las etiquetas de control (normalmente para vínculos de comandos, botones de radio y casillas). <br/>                                    | ![Captura de pantalla que muestra un cuadro de diálogo de configuración de seguridad.](images/text-ui-image5.png)<br/> En este ejemplo, las explicaciones complementarias aclaran las opciones.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Conceptos de diseño

Los desarrolladores de software suelen pensar que el texto se relega a la documentación del producto y al soporte técnico. "Primero escribiremos el código y, a continuación, contrataremos a alguien para que nos ayude a explicar lo que hemos desarrollado". Sin embargo, en realidad, se escribe texto importante anteriormente en el proceso, ya que la interfaz de usuario se concibe y codifica. Después de todo, este texto se ve con más frecuencia y por más personas que cualquier otro tipo de escritura técnica.

**El texto comprensible es fundamental para una interfaz de usuario eficaz.** Professional escritores y editores deben trabajar con desarrolladores de software en el texto de la interfaz de usuario como parte integral del proceso de diseño. Hacer que funcionen pronto en el texto porque los problemas de texto a menudo revelan problemas de diseño. Si su equipo tiene problemas para explicar un diseño, a menudo es el diseño, no la explicación, el que necesita mejorar.

### <a name="a-design-model-for-ui-text"></a>Un modelo de diseño para el texto de la interfaz de usuario

Cuando piense en el texto de la interfaz de usuario y su ubicación en las superficies de la interfaz de usuario, tenga en cuenta estos hechos:

-   Durante la lectura inmersiva centrada, las personas leen en un orden de izquierda a derecha, de arriba a abajo (en las culturas occidental).
-   Cuando se usa software, los usuarios no están inmersos en la propia interfaz de usuario, sino en su trabajo. Por lo tanto, los usuarios no leen el texto de la interfaz de usuario que lo analizan.
-   Al examinar una ventana, es posible que parezca que los usuarios leen texto cuando en realidad lo filtran. A menudo no comprenden realmente el texto de la interfaz de usuario a menos que perciban la necesidad de.
-   Dentro de una ventana, los distintos elementos de la interfaz de usuario reciben distintos niveles de atención. Los usuarios tienden a leer primero las etiquetas de control, especialmente aquellas que parecen pertinentes para completar la tarea en cuestión. Por el contrario, los usuarios tienden a leer texto estático solo cuando creen que lo necesitan.

En el caso de un modelo de diseño general, no suponga que los usuarios leen cuidadosamente el texto en un orden de izquierda a derecha, de arriba a abajo. En su lugar, suponga que los usuarios empiezan por examinar rápidamente toda la ventana y, a continuación, leen el texto de la interfaz de usuario en aproximadamente el orden siguiente:

-   Controles interactivos en el centro
-   Botones [de confirmación](glossary.md)
-   Controles interactivos encontrados en otro lugar
-   Instrucción principal
-   Explicaciones complementarias
-   Título de la ventana
-   Otro texto estático en el cuerpo principal
-   Notas al pie

También debe suponer que una vez que los usuarios han decidido qué hacer, dejarán de leer y hacerlo inmediatamente.

### <a name="eliminate-redundancy"></a>Eliminación de la redundancia

El texto redundante no solo toma un espacio de pantalla valioso, sino que también se ve reducido la eficacia de las ideas o acciones importantes que intenta transmitir. También es una pérdida de tiempo del lector, y mucho más en un contexto en el que el examen es la norma. **Windows se esfuerza por explicar lo que los usuarios deben hacer una vez correcta y concisamente.**

Revise cada ventana y elimine palabras e instrucciones duplicadas, tanto dentro como entre controles. No evite que el texto importante sea explícito siempre que sea necesario, pero no sea redundante y no explique lo obvio.

### <a name="avoid-over-communication"></a>Evitar la comunicación en exceso

Incluso si el texto no es redundante, puede ser demasiado wordy en un esfuerzo por explicar cada detalle. **El exceso de texto desaconseja leer el ojo tiende a omitirlo de forma irónica, lo que provoca menos comunicación en lugar de más.** En el texto de la interfaz de usuario, comunique de forma concisa la información esencial. Si se necesita más información para algunos usuarios o algunos escenarios, proporcione un vínculo al contenido de ayuda más detallado [o](winenv-help.md)quizás a una entrada de glosario para aclarar un término.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con 6 párrafos](images/text-ui-image6.png)

En este ejemplo, hay demasiado texto para examinar fácilmente. Aunque no está previsto por el diseñador, hay tanto texto que lo más probable es que los usuarios haga clic en Siguiente sin leer nada.

Para evitar texto que desaconseja la lectura, puede crear el texto para hacer que cada palabra cuente. Lo que no agrega restas, por lo que debe usar texto simple y conciso.

### <a name="use-the-inverted-pyramid"></a>Uso de la pirámide invertida

La escritura académica suele usar un estilo estructural "piramidal" que basa los hechos, trabaja con esos hechos y se acumula hasta una conclusión que forma una estructura similar a la piramidal. Por el contrario, los escritores usan un estilo de "pirámide invertida" que comienza con la conclusión de la "conclusión" fundamental que deben tener los lectores. A continuación, rellena progresivamente más detalles que los lectores pueden estar interesados en quizás solo para examinar. La ventaja de este estilo es que llega directamente al punto y permite a los lectores dejar de leer en cualquier momento que elijan y seguir con la información esencial.

Debe aplicar la estructura piramidal invertida al texto de la interfaz de usuario. Llegue directamente al punto con la información esencial, deje que los usuarios dejen de leer en el momento que elijan y use un vínculo de Ayuda para presentar el resto de la pirámide.

![captura de pantalla del mensaje al unirse al programa de Windows ](images/text-ui-image7.png)

En este ejemplo, la información esencial está en la consulta del texto de instrucción principal, la información útil adicional está en las instrucciones complementarias y los detalles están disponibles haciendo clic en un vínculo de Ayuda.

**Si solo hace cinco cosas...**

1.  Trabajar en texto pronto porque los problemas de texto a menudo revelan problemas de diseño.
2.  Diseñe el texto para el examen.
3.  Elimine el texto redundante.
4.  Usar texto fácil de entender; no se comunican en exceso.
5.  Cuando sea necesario, proporcione vínculos al contenido de ayuda para obtener información más detallada.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Quite el texto redundante.** Busque texto redundante en los títulos de la ventana, las instrucciones principales, las instrucciones complementarias, las áreas de contenido, los vínculos de comandos y los botones de confirmación. Por lo general, deje texto completo en las instrucciones principales y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **Evite grandes bloques de texto de la interfaz de usuario.** Entre las formas de hacerlo se incluyen:
    -   Fragmentar texto en oraciones y párrafos más cortos.
    -   Cuando sea necesario, proporcione [vínculos de Ayuda](winenv-help.md) a información útil, pero no esencial.
-   **Elija nombres de objeto y etiquetas que comuniquen y diferencien claramente lo que hace el objeto.** Los usuarios no deben tener que averiguar qué significa realmente el objeto ni cómo difiere de otros objetos.

    Incorrecto:

    ![captura de pantalla de la lista de monitores sin nombre](images/text-ui-image8.png)

    Mejor:

    ![captura de pantalla de la lista de adaptadores de red específicos](images/text-ui-image9.png)

    En el ejemplo incorrecto, los nombres de objeto no se diferencian en absoluto; el mejor ejemplo muestra una diferencia fuerte por nombre de producto.

-   **Si desea asegurarse de que los usuarios leen texto específico relacionado con una acción, colómelo en un control interactivo.**
    -   **Aceptable:**
    -   ![captura de pantalla de la advertencia de formato mediante el botón Aceptar ](images/text-ui-image10.png)
    -   En este ejemplo, existe la posibilidad de que los usuarios no lean el texto que explica lo que están confirmando.
    -   **Mejor:**
    -   ![captura de pantalla del botón de formato y advertencia de formato ](images/text-ui-image11.png)
    -   En este ejemplo, puede estar seguro de que al menos los usuarios entiendan que están a punto de dar formato a un disco.
-   **Use un espacio entre oraciones.** No dos.

### <a name="text-fonts-sizes-and-colors"></a>Fuentes, tamaños y colores de texto

-   **Use texto azul solo para vínculos e instrucciones principales.**
-   **Use texto verde solo para direcciones URL en los resultados de la búsqueda.**

Las siguientes fuentes y colores son los valores predeterminados para Windows.



| Patrón                                                                                     | Símbolo de tema                            | Fuente, Color                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![primera columna: texto de la barra de título ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. black \# (000000) Segoe UI<br/>                 |
| ![primera columna: instrucciones principales ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. blue \# (003399) Segoe UI<br/>                 |
| ![primera columna: instrucciones secundarias ](images/text-ui-image14.png)<br/>      | Instrucción<br/>      | 9 pt. black \# (000000) Segoe UI<br/>                 |
| ![primera columna: texto normal ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. black \# (000000) Segoe UI<br/>                 |
| ![primera columna: texto resaltado ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, negrita o cursiva<br/> |
| ![primera columna: texto editable ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. negro \# (000000) Segoe UI, en un cuadro<br/>       |
| ![primera columna: texto deshabilitado ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 pt. gris oscuro \# (323232) Segoe UI<br/>             |
| ![primera columna: vínculo ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. blue \# (0066CC) Segoe UI<br/>                  |
| ![primera columna: vínculos (mantener el puntero) ](images/text-ui-image20.png)<br/>               | Acceso frecuente<br/>              | 9 pt. azul claro \# (3399FF) Segoe UI<br/>            |
| ![primera columna: encabezado de grupo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. blue \# (003399) Segoe UI<br/>                 |
| ![primera columna: nombre de archivo (en la vista de contenido) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. black \# (000000) Segoe UI<br/>                |
| ![primera columna: texto del documento ](images/text-ui-image23.png)<br/>               | (ninguno)<br/>           | 9 pt. black ( \# 000000) Calibri<br/>                  |
| ![primera columna: encabezados de documento ](images/text-ui-image24.png)<br/>           | (ninguno)<br/>           | 17 pt. black ( \# 000000) Calibri<br/>                 |



 

Para obtener más información y ejemplos, vea [Fuentes](vis-fonts.md) y [colores.](vis-color.md)

### <a name="other-text-characteristics"></a>Otras características de texto

**Negrita**

-   **Use negrita con moderación para llamar la atención sobre el texto que los usuarios deben leer.** Por ejemplo, los usuarios que analizan una lista de opciones de botón de radio pueden apreciar ver las etiquetas en negrita para destacar del texto que agrega información complementaria sobre cada opción. Tenga en cuenta que el uso de demasiada negrita disminuirá su impacto.
-   **Con los datos etiquetados, use negrita para resaltar lo que sea más importante para los datos en su conjunto.**
    -   Para datos principalmente genéricos (donde los datos tienen poco significado sin sus etiquetas, como con números o fechas), use etiquetas en negrita y datos sin formato para que los usuarios puedan examinar y comprender más fácilmente los tipos de datos.
    -   En el caso de los datos principalmente autoexplicativos, use etiquetas sin formato y datos en negrita para que los usuarios puedan centrarse en los propios datos.
    -   Como alternativa, puede usar texto gris oscuro para desacenter la información menos importante en lugar de usar negrita para resaltar la información más importante.

        ![captura de pantalla de la vista en miniatura del Explorador de Windows ](images/text-ui-image25.png)

        En este ejemplo, en lugar de resaltar los datos mediante negrita, las etiquetas se desasocian mediante gris oscuro.

-   **No todas las fuentes admiten negrita, por lo que nunca debe ser fundamental comprender el texto.**

**Cursiva**

-   Use para hacer referencia al texto literalmente. No use comillas para este propósito.

    **Correcto:**

    Los términos documento y archivo se suelen usar indistintamente.

-   Use para [avisos en](glossary.md) cuadros [de texto y](ctrl-text-boxes.md) listas [desplegables editables.](/windows/desktop/uxguide/ctrl-drop)

    ![captura de pantalla del cuadro de texto de búsqueda ](images/text-ui-image26.png)

    En este ejemplo, el símbolo del sistema del cuadro Buscar tiene el formato de texto cursiva.

-   Use con moderación para resaltar palabras específicas para ayudar a comprender.
-   **No todas las fuentes admiten cursiva, por lo que nunca debe ser fundamental comprender el texto.**

**Negrita cursiva**

-   No use en el texto de la interfaz de usuario.

**Subrayar**

-   No use, excepto los vínculos.
-   No use para énfasis. Use cursiva en su lugar.

### <a name="punctuation&quot;></a>Signos de puntuación

**Puntos**

-   **No coloque al final de las etiquetas de control, las instrucciones principales ni los vínculos de Ayuda.**
-   Coloque al final de instrucciones complementarias, explicaciones complementarias o cualquier otro texto estático que forte una oración completa.

**Signos de interrogación**

-   **Coloque al final de todas las preguntas.** A diferencia de los puntos, los signos de interrogación se usan para todos los tipos de texto.

**Signos de exclamación**

-   En aplicaciones empresariales, evite.
    -   **Excepciones:** Los signos de exclamación se usan a veces en el contexto de la finalización de la descarga (&quot;Done!") y para llamar la atención sobre el contenido web ("New!").

**Comas**

-   En una lista de tres o más elementos, coloque siempre una coma después del elemento siguiente al último de la lista.

**Colones**

-   **Use dos puntos al final de las etiquetas de control externo.** Esto es especialmente importante para la accesibilidad porque algunas tecnologías de asistencia buscan dos puntos para identificar las etiquetas de control.
-   Use dos puntos para introducir una lista de elementos.

**Elipses**

-   **Los puntos suspensivos significan incompleta.** Use puntos suspensivos en el texto de la interfaz de usuario de la siguiente manera:
    -   **Comandos:** Indique que un comando necesita información adicional. No use puntos suspensivos siempre que una acción muestre otra ventana solo cuando se requiera información adicional. Para obtener más información, vea [Botones de comandos](ctrl-command-buttons.md).
    -   **Datos:** Indique que el texto está truncado.
    -   **Etiquetas:** Indique que una tarea está en curso (por ejemplo, "Búsqueda...").

        **Sugerencia:** El texto truncado en una ventana o página con espacio sin usar indica un diseño deficiente o un tamaño de ventana predeterminado demasiado pequeño. Procure diseños y tamaños de ventana predeterminados que eliminen o reduzcan la cantidad de texto truncado. Para obtener más información, vea [Diseño](vis-layout.md).

-   **No haga que los puntos suspensivos se hagan interactivos.** Para mostrar texto truncado, permita a los usuarios cambiar el tamaño del control para ver más texto o usar un [control de divulgación progresiva en su](ctrl-progressive-disclosure-controls.md) lugar.

**Comillas y apóstrofos**

-   Para hacer referencia al texto literalmente, use el formato cursiva en lugar de las comillas.
-   Coloque los títulos de ventana y las etiquetas de control entre comillas solo si es necesario para evitar confusiones y no se puede dar formato con negrita en su lugar.
-   En el caso de las comillas, se prefieren comillas dobles (" "); evite las comillas simples.

    **Correcto:**

    ¿Está seguro de que desea eliminar la "carpeta cat de Sparky"?

    **Incorrecto:**

    ¿Está seguro de que desea eliminar la carpeta cat de Sparky?

### <a name="capitalization"></a>Uso de mayúsculas

-   **Use mayúsculas de estilo de título para títulos, mayúsculas de estilo oración para todos los demás elementos de la interfaz de usuario.** Esto es más adecuado para el [tono Windows .](text-style-tone.md)

    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar mayúsculas de estilo de título para botones de comandos, menús y encabezados de columna si es necesario para evitar mezclar estilos de mayúsculas.

        ![captura de pantalla de la hoja de propiedades genérica ](images/text-ui-image27.png)

    En este ejemplo genérico se muestran las mayúsculas y las puntuaciones correctas para las hojas de propiedades.

    ![captura de pantalla del cuadro de diálogo genérico ](images/text-ui-image28.png)

    En este ejemplo genérico se muestran las mayúsculas y las puntuaciones correctas para los diálogos.

-   **Para los nombres de características y tecnologías, sea conservador en mayúsculas.** Normalmente, solo los componentes principales se deben incluir en mayúsculas (con mayúsculas de estilo de título).

    **Correcto:**

    Analysis Services, cubos, dimensiones

    Analysis Services es un componente principal de SQL Server, por lo que la mayúscula de estilo de título es adecuada; Los cubos y las dimensiones son elementos comunes del software de análisis de base de datos, por lo que no es necesario capitalizarlos.

-   **Para los nombres de características y tecnologías, sea coherente en mayúsculas.** Si el nombre aparece más de una vez en una pantalla de interfaz de usuario, siempre debería aparecer de la misma manera. Del mismo modo, en todas las pantallas de interfaz de usuario del programa, el nombre debe presentarse de forma coherente.
-   No en mayúsculas los nombres de los elementos genéricos de la interfaz de usuario, como la barra de herramientas, el menú, la barra de desplazamiento, el botón y el icono.
    -   **Excepciones:** Barra de direcciones, Barra de vínculos.
-   No use todas las letras mayúsculas para las teclas de teclado. En su lugar, siga la mayúscula que usan los teclados estándar o en minúsculas si la tecla no está etiquetada en el teclado.

    **Correcto:**

    barra espaciadora, Tab, Entrar, Subir página, Ctrl+Alt+Supr

    **Incorrecto:**

    BARRA ESPACIADORA, TABULACIÓN, ENTRAR, PG ARRIBA, CTRL+ALT+SUPR

-   **No use todas las letras mayúsculas como énfasis.** Los estudios han demostrado que esto es difícil de leer y los usuarios tienden a considerarlo "insensibilidad". Para las advertencias, use un icono de advertencia y una explicación clara de la situación. No es necesario agregar, por ejemplo, el término ADVERTENCIA en todas las letras mayúsculas.

Para obtener más información, vea la sección "Texto" o "Etiquetas" en las directrices de componentes de interfaz de usuario específicos.

### <a name="dates-and-times"></a>Fechas y horas

-   **No codifite de forma hard-code el formato de fechas y horas.** Respete la elección del usuario de la configuración regional y las opciones de personalización para los formatos de fecha y hora. El usuario los selecciona en el elemento del panel de control Región e Idioma.

    ![captura de pantalla con formato de fecha: lunes, 6 de julio de 2009](images/text-ui-image29.png)![captura de pantalla de formato de fecha: 6 de julio de 2009](images/text-ui-image30.png)

    En estos ejemplos de Microsoft Outlook, ambos formatos para la fecha larga son correctos. Reflejan las distintas opciones que los usuarios han realizado en el elemento del panel de control Región e Idioma.

-   **Use el formato de fecha larga para escenarios que se benefician de tener información adicional.** Use el formato de fecha corta para los contextos que no tienen espacio suficiente para el formato largo. Aunque los usuarios eligen qué información les gustaría incluir en los formatos largo y corto, los diseñadores eligen qué formato mostrar en sus programas en función del escenario y el contexto.

    ![captura de pantalla de formato con fechas de inicio y vencimiento](images/text-ui-image31.png)

    En este ejemplo, el formato de fecha larga ayuda a los usuarios a organizar tareas y fechas límite.

### <a name="globalization-and-localization"></a>Globalización y localización

La globalización significa crear documentos o productos que se puedan usar en cualquier país, región o referencia cultural. La localización significa adaptar documentos o productos para su uso en una configuración regional que no sea el país o región de origen. Considere la globalización y localización al escribir texto de la interfaz de usuario. El programa puede traducirse a otros idiomas y usarse en culturas muy diferentes de las suyas propias.

-   Para los controles con contenido variable (como vistas de lista y vistas de árbol), elija un ancho adecuado para **los datos válidos más largos.**
-   Incluya espacio suficiente en la superficie de la interfaz de usuario para un **30 %** adicional (hasta un 200 % para texto más corto) para cualquier texto (pero no números) que se localizará. La traducción de un idioma a otro suele cambiar la longitud de línea del texto.
-   No cree cadenas a partir de subcadenas en tiempo de ejecución. En su lugar, use oraciones completas para que no haya ambigüedad para el traductor.
-   **No use un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase.** Este diseño no es localizable porque la estructura de oraciones varía según el lenguaje.

    **Incorrecto:**

    ![captura de pantalla del cuadro de texto dentro de una etiqueta de casilla ](images/text-ui-image32.png)

    **Correcto:**

    ![captura de pantalla del cuadro de texto después de una etiqueta de casilla ](images/text-ui-image33.png)

    En el ejemplo incorrecto, el cuadro de texto se coloca dentro de la etiqueta de casilla.

-   No haga que solo una parte de una frase sea un vínculo, ya que, cuando se traduce, es posible que ese texto no permanezca junto. Por lo tanto, el texto del vínculo debe formar una oración completa por sí mismo.
    -   **Excepción:** Los vínculos de glosario se pueden insertar en línea, como parte de una oración.

Para más información, consulte el Centro [para desarrolladores globales de Go.](https://msdn.microsoft.com/goglobal/)

### <a name="title-bar-text"></a>Texto de la barra de título

-   Elija el texto de la barra de título según el tipo de ventana:
    -   **Ventanas de programa** centradas en documentos de nivel superior: Use un formato de "nombre de programa de nombre de documento". Los nombres de documento se muestran primero para dar una sensación centrada en el documento.
    -   **Ventanas de programa de nivel superior que no están centradas en documentos:** Mostrar solo el nombre del programa.
    -   **Cuadros de diálogo:** Muestra el comando, la característica o el programa desde el que llegó el cuadro de diálogo. No use el título para explicar el propósito del cuadro de diálogo que es el propósito de las instrucciones principales. Para obtener más instrucciones, vea [Cuadros de diálogo](win-dialog-box.md).
    -   **Asistentes:** Muestra el nombre del asistente. Tenga en cuenta que la palabra "asistente" no debe incluirse en los nombres del asistente. Para obtener más instrucciones, vea [Asistentes](win-wizards.md).
-   **Para las ventanas de programa de nivel superior, si el título y el icono de la barra de título se muestran de forma destacada cerca de la parte superior de la ventana, puede ocultar el título y el icono de la barra de título para evitar redundancia.** Sin embargo, todavía tiene que establecer un título adecuado internamente para que lo use Windows.
-   **Para los cuadros de diálogo, no incluya las palabras "diálogo" o "progreso" en los títulos.** Estos conceptos están implícitos y dejar estas palabras desactivadas hace que los títulos sean más fáciles de examinar para los usuarios.

### <a name="main-instructions"></a>Instrucciones principales

-   **Use la instrucción principal para explicar concisamente qué deben hacer los usuarios en una ventana o página determinadas.** Las instrucciones principales buenas comunican el objetivo del usuario en lugar de centrarse solo en manipular la interfaz de usuario.
-   **Expresar la instrucción principal en forma de una dirección imperativa o una pregunta específica.**

    **Incorrecto:**

    ![captura de pantalla del nombre del programa como instrucción principal ](images/text-ui-image34.png)

    En este ejemplo, la instrucción principal simplemente indica el nombre del programa; no invita explícitamente a realizar un curso de acción para el usuario.

    **Excepciones:** Los mensajes de error, los mensajes de advertencia y las confirmaciones pueden usar estructuras de oración diferentes en sus instrucciones principales.

-   **Use verbos específicos siempre que sea posible.** Los verbos específicos (ejemplos: conectar, guardar, instalar) son más significativos para los usuarios que los genéricos (ejemplos: configurar, administrar, establecer).
    -   Para las páginas del panel de control y las páginas del asistente, si no puede usar un verbo específico, puede que prefiera omitir el verbo por completo.

        **Aceptable:**

        Escriba la configuración regional, la región y el idioma.

        **Mejor:**

        Configuración regional, región e idioma

    -   Para los diálogos, como mensajes de error y advertencias, no omita el verbo .

-   No se sienta cómodo de usar el texto de instrucción principal si agregarlo solo sería redundante o obvio desde el contexto de la interfaz de usuario.

    ![captura de pantalla del cuadro de diálogo Guardar como ](images/text-ui-image35.png)

    En este ejemplo, el contexto de la interfaz de usuario ya está muy claro; no es necesario agregar texto de instrucción principal.

-   **Sea conciso y use solo una sola oración completa.** Pare la instrucción principal hasta la información esencial. Si tiene que explicar algo más, considere la posibilidad de usar una instrucción complementaria.
-   Use mayúsculas de estilo de frase.
-   **No incluya períodos finales si la instrucción es una instrucción .** Si la instrucción es una pregunta, incluya un signo de interrogación final.
-   **En el caso de los diálogos de progreso, use** una frase de error que explique brevemente la operación en curso y termine con puntos suspensivos. Ejemplo: "Imprimir las imágenes..."
-   **Sugerencia:** Puede evaluar una instrucción principal mediante la lectura de lo que podría decir a un amigo al explicar qué hacer con la ventana o página. Si responder con la instrucción principal sería poco natural, poco útil o difícil, vuelva a trabajar la instrucción.

Para obtener más información, consulte la sección "Instrucción principal" en las directrices de componentes de interfaz de usuario específicos.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   Cuando sea necesario, use una instrucción complementaria para presentar información adicional útil para comprender o **usar la ventana o página,** como:
    -   Proporcionar contexto para explicar por qué se muestra la ventana si se inicia el programa o el sistema.
    -   Información de calificación que ayuda a los usuarios a decidir cómo actuar en la instrucción principal.
    -   Definir terminología importante.
-   **No use una instrucción complementaria si no es necesaria.** Prefiere comunicar todo con la instrucción principal si puede hacerlo de forma concisa.
-   **No repita la instrucción principal con una redacción ligeramente diferente.** En su lugar, omita la instrucción complementaria si no hay nada más que agregar.
-   Use oraciones completas y mayúsculas de estilo oración.

### <a name="control-labels"></a>Etiquetas de control

-   **Etiquete cada control o grupo de controles. Excepciones:**
    -   Los cuadros de texto y las listas desplegables se pueden etiquetar mediante avisos.
    -   Por lo general, los controles de divulgación progresiva no están etiquetados.
    -   **Los controles subordinados usan la etiqueta de su control asociado.** Los controles de giro siempre son controles subordinados.
    -   **Omita las etiquetas de control que vuelvan a restablecer la instrucción principal.** En este caso, la instrucción principal toma la clave de acceso.

        **Aceptable:**

        ![captura de pantalla del cuadro de texto con instrucciones y etiqueta ](images/text-ui-image36.png)

        En este ejemplo, la etiqueta del cuadro de texto es simplemente una nueva instrucción de la instrucción principal.

        **Mejor:**

        ![captura de pantalla del cuadro de texto solo con instrucciones ](images/text-ui-image37.png)

        En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma la clave de acceso.

-   Colocación de etiquetas:
    -   El propio control etiqueta directamente los globos, las casillas, los botones de comando, los cuadros de grupo, los vínculos, las pestañas y las sugerencias.
    -   Las listas desplegables, los cuadros de lista, las vistas de lista, las barras de progreso, los controles deslizantes, los cuadros de texto y las vistas de árbol se etiquetan arriba, vacían a la izquierda o a la izquierda.
    -   Los controles de divulgación progresiva normalmente no están etiquetados. Los botones de contenido adicional se etiquetan a la derecha.
-   **Asigne una clave de acceso única para cada control interactivo, excepto** para los vínculos. Para obtener más información, vea [Teclado](inter-keyboard.md).
-   **Mantenga las etiquetas breves.** Sin embargo, tenga en cuenta que agregar una palabra o dos a una etiqueta puede ayudar a la claridad y, a veces, elimina la necesidad de explicaciones complementarias.
-   **Prefiere etiquetas específicas sobre las genéricas.** Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta.

    **Incorrecto:**

    ![captura de pantalla del botón de comando Aceptar ](images/text-ui-image38.png)

    **Correcto:**

    ![captura de pantalla del botón publicar comando ](images/text-ui-image39.png)

    En el ejemplo correcto, se usa una etiqueta específica para el botón de confirmación.

-   **Para las listas de etiquetas,** como los botones de radio, use expresiones paralelas e intente mantener la longitud aproximadamente igual para todas las etiquetas.
-   **Para las listas de etiquetas, centre el texto de la etiqueta en las diferencias entre las opciones.** Si todas las opciones tienen el mismo texto introductorio, mueva ese texto a la etiqueta de grupo.

    **Incorrecto:**

    ![captura de pantalla de etiquetas con primeras frases duplicadas](images/text-ui-image40.png)

    **Correcto:**

    ![captura de pantalla de la primera frase que se ha movido a la etiqueta de grupo](images/text-ui-image41.png)

    El ejemplo correcto mueve la expresión introductoria idéntica a la etiqueta, por lo que las dos opciones se diferencian más claramente.

-   **En general, prefiere expresiones positivas.** Por ejemplo, use do en lugar de do not y notify en lugar de no notificar.
    -   **Excepción:** La etiqueta de casilla "Don't show this message again" (No volver a mostrar este mensaje) se usa ampliamente.
-   **Omita los verbos informativos que se aplican a todos los controles del tipo especificado.** En su lugar, centre las etiquetas en lo que es único sobre los controles. Por ejemplo, no significa que los usuarios necesiten escribir en un control de cuadro de texto o que los usuarios necesiten hacer clic en un vínculo.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: "type your name" ](images/text-ui-image42.png)

    **Correcto:**

    ![captura de pantalla de la etiqueta: "su nombre" ](images/text-ui-image43.png)

    En los ejemplos incorrectos, las etiquetas de control tienen verbos informativos que se aplican a todos los controles de su tipo.

-   En algunos casos, las siguientes anotaciones entre paréntesis para controlar las etiquetas pueden resultar útiles:
    -   **Si una opción es opcional, considere la posibilidad de agregar "(optional)" a la etiqueta.**
    -   **Si se recomienda encarecidamente una opción, agregue "(recommended)" a la etiqueta.** Esto significa que la configuración es opcional, pero debe establecerse de todos modos.
    -   **Si una opción está pensada solo para usuarios avanzados, considere la posibilidad de agregar "(advanced)" a la etiqueta.**
-   Puede especificar unidades (segundos, conexiones, entre paréntesis) después de la etiqueta.

    ![captura de pantalla de la etiqueta: tamaño inicial (mb) ](images/text-ui-image44.png)

    En este ejemplo se muestra que la unidad de medida es megabytes (MB).

Para obtener más información, vea la sección "Texto" o "Etiquetas" en las directrices de componentes de interfaz de usuario específicos.

### <a name="supplemental-explanations"></a>Explicaciones complementarias

-   **Use explicaciones complementarias cuando los controles requieran más información de la que puede transmitir su etiqueta.** Pero no use una explicación complementaria si no es necesario prefiere comunicarse todo con la etiqueta de control si puede hacerlo de forma concisa. Normalmente, las explicaciones complementarias se usan con vínculos de comandos, botones de radio y casillas.
-   Cuando sea necesario, **use negrita en las etiquetas de control para** facilitar el examen del texto cuando haya explicaciones complementarias.

    ![captura de pantalla del cuadro de diálogo configuración de seguridad ](images/text-ui-image45.png)

    En este ejemplo, las etiquetas de botón de radio están en negrita para que sean más fáciles de examinar.

-   **Agregar una explicación complementaria a un control de un grupo no significa que tenga que proporcionar explicaciones para todos los demás controles del grupo.** Proporcione la información pertinente en la etiqueta si puede y use explicaciones solo cuando sea necesario. No tenga explicaciones complementarias que simplemente vuelvan a establecer la etiqueta para mantener la coherencia.

    ![captura de pantalla de tres botones de radio ](images/text-ui-image46.png)

    En este ejemplo, dos controles del grupo incluyen explicaciones complementarias, pero el tercero no.

-   Si una explicación complementaria sigue un vínculo de comando, escriba el texto complementario en segunda persona.

    **Ejemplo:** Vínculo de comando: Creación de una configuración de red inalámbrica y guardado en una unidad flash USB

    Explicación complementaria: esto creará la configuración que puede transferir al enrutador con una unidad flash USB. Haga esto solo si tiene un enrutador inalámbrico que admita la configuración de la unidad flash USB.

-   Use oraciones completas y signos de puntuación finales.

### <a name="commit-button-labels"></a>Etiquetas de botón Confirmar

En la tabla siguiente se muestran las etiquetas de botón de confirmación más comunes y su uso.




| Etiqueta | Value |
|--------|-------|
| <strong>Etiqueta de botón</strong><br /> | <strong>Significado</strong><br /> | <strong>Cuándo se deben usar</strong><br /> | <strong>Clave de acceso</strong><br /> | 
| <strong>OK (CORRECTO)</strong><br /> | <ul><li>En los cuadros de diálogo: aplique los cambios o confirme en la tarea y cierre la ventana.</li><li>En las ventanas de propiedades de propietario: aplique los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se apliquen) y cierre la ventana.</li><li>En ventanas de propiedades de propiedad: mantenga los cambios, cierre la ventana y aplique los cambios cuando se apliquen los cambios de la ventana de propietario.</li></ul> | <ul><li>Se usa con ventanas que no son específicas de tareas, como hojas de propiedades.</li><li>En el caso de las ventanas que se usan para realizar una tarea específica, use una etiqueta específica en su lugar que comience con un verbo (ejemplo: Imprimir).</li><li>Para las ventanas en las que los usuarios no pueden realizar cambios, use Cerrar.</li></ul> | Entrar<br /> | 
| <strong>Sí/No</strong><br /> | Sí es la respuesta afirmativa a una pregunta sí o ninguna, mientras que No es la respuesta negativa.<br /> | <ul><li>Use los botones Sí y No solo para responder a preguntas sí o no. Nunca use Aceptar y Cancelar para preguntas sí o ninguna.</li><li>Prefiere respuestas específicas sobre los botones Sí y No. Aunque no hay ningún problema con el uso de Sí y No, las respuestas específicas se pueden entender más rápidamente, lo que da lugar a una toma de decisiones eficaz.</li><li>Sin embargo, considere la posibilidad de usar respuestas Sí y No si la expresión de respuestas específicas resulta larga o difícil.</li><li>No use los botones Sí y No si el significado de la respuesta No es claro. Si es así, use respuestas específicas en su lugar.</li><li>Sí y No siempre se deben usar como un par.</li></ul> | Y and N<br /> | 
| <strong>Cancelar</strong><br /> | <ul><li>En los cuadros de diálogo: descarte todos los cambios o el trabajo en curso, vuelva al estado anterior (sin ningún efecto secundario perceptible) y cierre la ventana.</li><li>En las hojas de propiedades: descarte todos los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se apliquen) y cierre la ventana.</li><li>En los elementos del panel de control: descarte todos los cambios o el trabajo en curso, vuelva al estado anterior y vuelva a la página central desde la que se inició la tarea. Si no hay ninguna página central de este tipo, cierre la ventana del elemento del panel de control en su lugar.</li></ul> | <ul><li>Use cuando se puedan descartar todos los cambios o acciones pendientes y se pueda deshacer cualquier efecto secundario.</li><li>Para los cambios que no se pueden descartar, use Cerrar. Para las acciones en curso que se pueden detener, use Detener. Si inicialmente se pueden descartar cambios o acciones, puede usar Cancelar inicialmente y, después, cambiar a Cerrar o Detener una vez que no se pueda deshacer.</li></ul> | Esc<br /> | 
| <strong>Cerrar</strong><br /> | Cierre la ventana. Los cambios o efectos secundarios no se descartan.<br /> | <ul><li>Use cuando no se puedan descartar los cambios o efectos secundarios. Use Cerrar en lugar de Cancelar para las ventanas principales.</li><li>Use para ventanas en las que los usuarios no puedan realizar cambios.</li></ul> | Alt+F4, Ctrl+F4<br /> | 
| <strong>Detención</strong><br /> | Detenga una tarea en ejecución y cierre la ventana. No se descartan los trabajos en curso ni los efectos secundarios.<br /> | <ul><li>Use cuando el trabajo esté en curso y los efectos secundarios no se puedan descartar o no, normalmente con barras de progreso o animaciones.</li></ul> | Esc<br /> | 
| <strong>Aplicar</strong><br /> | En las hojas de propiedades del propietario: aplique los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se apliquen), pero deje la ventana abierta. Esto permite a los usuarios evaluar los cambios antes de cerrar la hoja de propiedades. En hojas de propiedades de propiedad: no use.<br /> | <ul><li>Use solo en hojas de propiedades.</li><li>Proporcione un botón Aplicar solo si la hoja de propiedades tiene valores (al menos uno) con efectos que los usuarios pueden evaluar de forma significativa. Normalmente, los botones Aplicar se usan cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluarlo y realizar más cambios en función de esa evaluación. Si no es así, quite el botón Aplicar en lugar de deshabilitarlo.</li></ul> | A<br /> | 
| <strong>Siguiente</strong><br /> | En asistentes y tareas de varios pasos: avance al paso siguiente sin confirmar la tarea.<br /> | <ul><li>Use solo en asistentes y tareas de varios pasos para avanzar al paso siguiente sin compromiso.</li><li>El efecto de un botón Siguiente siempre se puede deshacer haciendo clic en Atrás.</li></ul> | N<br /> | 
| <strong>Finalizar</strong><br /> | En asistentes y tareas de varios pasos: cierre la ventana. Si la tarea aún no se ha realizado, realice la tarea. Si esa tarea ya se ha realizado, no se descartan los cambios o efectos secundarios.<br /> | <ul><li>Use solo en asistentes y tareas de varios pasos. Sin embargo, se desaconseja el uso de Finish porque normalmente hay un botón de confirmación mejor y más específico:<ul><li>Si al hacer clic en el botón se confirma en la tarea (por lo que la tarea aún no se ha realizado), use una etiqueta específica que comience con un verbo (ejemplos: Imprimir, Conectar, Iniciar) que sea una respuesta a la instrucción principal.</li><li>Si la tarea ya se ha realizado en el asistente, use Cerrar en su lugar.</li></ul></li><li>Sin embargo, puede usar Finalizar cuando:<ul><li>La etiqueta específica sigue siendo genérica, como Guardar, Seleccionar, Elegir u Obtener.</li><li>La tarea implica cambiar una configuración o una colección de valores.</li></ul></li></ul> | Entrar<br /> | 
| <strong>Listo</strong><br /> | No es aplicable.<br /> | <ul><li>No lo use. La realización de un comando es gramaticalmente incorrecta.</li></ul> | No es aplicable.<br /> | 




 


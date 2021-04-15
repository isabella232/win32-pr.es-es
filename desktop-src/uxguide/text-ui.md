---
title: Texto de la interfaz de usuario
description: El texto de la interfaz de usuario aparece en las superficies de la IU.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1c1a60ba0bfef33dcf1e72c5ba19b11c4a5f38a2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104568724"
---
# <a name="user-interface-text"></a>Texto de la interfaz de usuario

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

El texto de la interfaz de usuario aparece en las superficies de la IU. Este texto incluye etiquetas de control y texto estático:

-   Las etiquetas de control identifican los controles y se colocan directamente en los controles o junto a ellos.
-   Texto estático, al que se llama porque no forma parte de un control interactivo, proporciona a los usuarios instrucciones detalladas o explicaciones para que puedan tomar decisiones fundamentadas.

**Nota:** Las instrucciones relacionadas con el [estilo y el tono](text-style-tone.md), las [fuentes](vis-fonts.md)y las etiquetas de [control](controls.md) de at se presentan en artículos independientes.

## <a name="usage-patterns"></a>Patrones de uso

El texto de la interfaz de usuario tiene varios patrones de uso:



|                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto de la barra de título**<br/> Use el texto de la barra de título para identificar una ventana o el origen de un cuadro de diálogo. <br/>                                                                            | ![captura de pantalla de la barra de título de opciones de carpeta](images/text-ui-image1.png)<br/> En este ejemplo, el texto de la barra de título identifica una ventana.<br/>                                                                                                                                                                                                                                                                                                             |
| **Instrucciones principales**<br/> Use la instrucción principal destacada para explicar brevemente qué hacer en la ventana o la página. <br/>                                                      | La instrucción debe ser una instrucción específica, una dirección imperativa o una pregunta. las buenas instrucciones principales comunican el objetivo del usuario en lugar de centrarse simplemente en manipular la interfaz de usuario. <br/> ![captura de pantalla de pregunta: ¿desea obtener más ayuda? ](images/text-ui-image2.png)<br/> En este ejemplo, el texto de la instrucción principal atrae directamente al usuario con una pregunta en lo que se refiere a la ventaja o al interés del usuario.<br/>             |
| **Instrucciones complementarias**<br/> cuando sea necesario, use una instrucción complementaria para presentar información adicional útil para comprender o usar la ventana o la página. <br/> | Puede proporcionar información más detallada, proporcionar contexto y definir la terminología. instrucciones complementarias que se detallan en la instrucción principal sin simplemente volver a escribirla. <br/> ![captura de pantalla de texto al cambiar a la cuenta de administrador ](images/text-ui-image3.png)<br/> En este ejemplo, las instrucciones complementarias proporcionan dos posibles cursos de acción que se deben llevar a cabo en respuesta a la información que se presenta en la instrucción principal.<br/> |
| **Etiquetas de control**<br/> etiquetas directamente en los controles o junto a ellos. <br/>                                                                                                           | ![captura de pantalla de las opciones del reloj del escritorio ](images/text-ui-image4.png)<br/> En este ejemplo, las etiquetas de control identifican la configuración del reloj de escritorio que los usuarios pueden seleccionar o modificar.<br/>                                                                                                                                                                                                                                                                       |
| **Explicaciones complementarias**<br/> una elaboración de las etiquetas de control (normalmente para los vínculos de comandos, botones de radio y casillas). <br/>                                    | ![Captura de pantalla que muestra un cuadro de diálogo de configuración de seguridad.](images/text-ui-image5.png)<br/> En este ejemplo, las explicaciones complementarias aclaran las opciones.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Conceptos de diseño

Los desarrolladores de software suelen pensar en el texto como relegados a la documentación del producto y al soporte técnico. "En primer lugar, vamos a escribir el código y luego contratar a alguien para que nos ayude a explicar lo que hemos desarrollado". Pero en realidad, el texto importante se escribe anteriormente en el proceso, ya que la interfaz de usuario está concebida y codificada. Este texto es, después de todo, se ha encontrado con más frecuencia y más personas que quizás cualquier otro tipo de escritura técnica.

**El texto comprensible es fundamental para la interfaz de usuario eficaz.** Los redactores y editores profesionales deberían trabajar con desarrolladores de software en texto de la interfaz de usuario como parte integral del proceso de diseño. Hacer que funcionen en el texto al principio porque los problemas de texto suelen revelar problemas de diseño. Si el equipo tiene problemas para explicar un diseño, a menudo es el diseño, no la explicación, que necesita mejorar.

### <a name="a-design-model-for-ui-text"></a>Un modelo de diseño para el texto de la interfaz de usuario

Cuando piense en el texto de la interfaz de usuario y su ubicación en las superficies de la interfaz de usuario, tenga en cuenta estos hechos:

-   Durante la lectura envolvente enfocada, las personas leen de izquierda a derecha y de arriba abajo (en las referencias culturales occidentales).
-   Cuando se usa software, los usuarios no se sumergin en la propia interfaz de usuario, sino en su trabajo. Por lo tanto, los usuarios no leen el texto de la interfaz de usuario que lo examinan.
-   Al examinar una ventana, es posible que los usuarios parezcan leer texto cuando en realidad lo están filtrando. A menudo no comprenden realmente el texto de la interfaz de usuario a menos que perciban la necesidad de.
-   Dentro de una ventana, los distintos elementos de la interfaz de usuario reciben distintos niveles de atención. Los usuarios tienden a leer las etiquetas de control en primer lugar, especialmente las que parecen relevantes para completar la tarea a mano. Por el contrario, los usuarios suelen leer texto estático cuando piensan que necesitan.

En el caso de un modelo de diseño general, no suponga que los usuarios lean cuidadosamente el texto de un orden de izquierda a derecha y de arriba a abajo. En su lugar, suponga que los usuarios empiezan con el examen rápido de toda la ventana y, a continuación, leen el texto de la interfaz de usuario en aproximadamente el orden siguiente:

-   Controles interactivos en el centro
-   [Botones de confirmación](glossary.md)
-   Controles interactivos que se encuentran en otro lugar
-   Instrucción principal
-   Explicaciones complementarias
-   Título de la ventana
-   Otro texto estático en el cuerpo principal
-   Notas al pie

También debe preocuparse de que, una vez que los usuarios hayan decidido qué hacer, dejarán de leerse inmediatamente y lo hacen.

### <a name="eliminate-redundancy"></a>Eliminar redundancia

El texto redundante no solo toma un valioso espacio de pantalla, sino que debilita la eficacia de las ideas o acciones importantes que intenta transmitir. También es un desperdicio de la hora del lector y todo lo demás en un contexto en el que el análisis es la norma. **Windows se esfuerza por explicar qué deben hacer los usuarios una vez bien y conciso.**

Revise cada ventana y elimine las palabras y las instrucciones duplicadas, tanto dentro como entre los controles. No Evite que el texto importante sea explícito siempre que sea necesario, pero no sea redundante y no explique el obvio.

### <a name="avoid-over-communication"></a>Evitar la comunicación excesiva

Aunque el texto no sea redundante, puede ser simplemente una palabra en un esfuerzo para explicar cada detalle. **Demasiados textos desaconsejan la lectura del ojo, lo que tiende a saltar a la derecha, lo que da lugar a menos comunicación, en lugar de más.** En texto de la interfaz de usuario, comunique de manera concisa la información esencial. Si es necesario más información para algunos usuarios o algunos escenarios, proporcione un vínculo a un [contenido de ayuda](winenv-help.md)más detallado o quizás a una entrada de glosario para clarificar un término.

**Incorrecto:**

![captura de pantalla del cuadro de diálogo con 6 párrafos](images/text-ui-image6.png)

En este ejemplo, hay demasiado texto para examinar fácilmente. Aunque el diseñador no lo pretendía, hay tantas texto que es más probable que los usuarios haga clic en siguiente sin leer nada.

Para evitar el texto que desaconseja la lectura, cree su texto para que recuento de palabras. Lo que no agrega restas, por lo que debe usar texto simple y conciso.

### <a name="use-the-inverted-pyramid"></a>Usar la pirámide invertida

La escritura académica normalmente usa un estilo estructural "piramidal" que define una base de hechos, trabaja con esos hechos y se basa en una conclusión en una estructura similar a una pirámide. Por el contrario, los periodistas usan un estilo "piramidal invertido" que comienza con la conclusión de la "ventaja" fundamental que deben tener los lectores. A continuación, se rellenan progresivamente más detalladamente si es posible que los lectores le interesen simplemente examinar. La ventaja de este estilo es que se obtiene justo hasta el punto y permite a los lectores dejar de leer en cualquier punto que elijan y seguir entendiendo la información esencial.

Debe aplicar la estructura piramidal invertida al texto de la interfaz de usuario. Obtenga acceso al punto con la información esencial, deje que los usuarios dejen de leer en cualquier momento que elijan y use un vínculo de ayuda para presentar el resto de la pirámide.

![captura de pantalla del mensaje al unirse al programa de Windows ](images/text-ui-image7.png)

En este ejemplo, la información esencial está en la consulta del texto de la instrucción principal, hay información útil adicional en las instrucciones complementarias y los detalles están disponibles haciendo clic en un vínculo de ayuda.

**Si solo hace cinco cosas...**

1.  Trabaje en el texto pronto porque los problemas de texto suelen revelar problemas de diseño.
2.  Diseñe el texto para el examen.
3.  Elimine el texto redundante.
4.  Usar texto fácil de entender; no se comunican excesivamente.
5.  Cuando sea necesario, proporcione vínculos al contenido de la ayuda para obtener información más detallada.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Quite el texto redundante.** Busque texto redundante en títulos de ventana, instrucciones principales, instrucciones adicionales, áreas de contenido, vínculos de comandos y botones de confirmación. Por lo general, deje texto completo en las instrucciones principales y los controles interactivos, y quite cualquier redundancia de los demás lugares.
-   **Evite bloques grandes de texto de la interfaz de usuario.** Estas son algunas formas de hacerlo:
    -   Fragmentación del texto en oraciones y párrafos más cortos.
    -   Cuando sea necesario, proporcionar [vínculos de ayuda](winenv-help.md) a información útil, pero no esencial.
-   **Elija los nombres de objeto y las etiquetas que se comunican claramente y diferencian lo que hace el objeto.** Los usuarios no deben tener que averiguar qué significa realmente el objeto o cómo se diferencia de otros objetos.

    Incorrecto:

    ![captura de pantalla de la lista de monitores sin nombre](images/text-ui-image8.png)

    Mejor:

    ![captura de pantalla de la lista de adaptadores de red específicos](images/text-ui-image9.png)

    En el ejemplo incorrecto, los nombres de objeto no se diferencian en absoluto; el mejor ejemplo muestra una diferencia fuerte por nombre de producto.

-   **Si desea asegurarse de que los usuarios lean texto específico relacionado con una acción, colóquelo en un control interactivo.**
    -   **Aceptable:**
    -   ![captura de pantalla de la advertencia de formato con el botón Aceptar ](images/text-ui-image10.png)
    -   En este ejemplo, hay una posibilidad de que los usuarios no lean el texto que explica lo que están confirmando.
    -   **Manera**
    -   ![captura de pantalla del botón de advertencia y formato de formato ](images/text-ui-image11.png)
    -   En este ejemplo, puede asegurarse de que al menos los usuarios saben que están a punto de formatear un disco.
-   **Use un espacio entre oraciones.** No dos.

### <a name="text-fonts-sizes-and-colors"></a>Fuentes de texto, tamaños y colores

-   **Use el texto azul solo para los vínculos y las instrucciones principales.**
-   **Use texto verde solo para las direcciones URL de los resultados de la búsqueda.**

Las siguientes fuentes y colores son valores predeterminados para Windows.



| Patrón                                                                                     | Símbolo de tema                            | Fuente, color                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![primera columna: texto de la barra de título ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![primera columna: instrucciones principales ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. Segoe UI azul ( \# 003399)<br/>                 |
| ![primera columna: instrucciones secundarias ](images/text-ui-image14.png)<br/>      | Instrucción<br/>      | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![primera columna: texto normal ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. negro ( \# 000000) Segoe UI<br/>                 |
| ![primera columna: texto resaltado ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. Black ( \# 000000) Segoe UI, negrita o cursiva<br/> |
| ![primera columna: texto modificable ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. negro ( \# 000000) Segoe UI, en un cuadro<br/>       |
| ![primera columna: texto deshabilitado ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 pt. Segoe UI gris oscuro ( \# 323232)<br/>             |
| ![primera columna: vínculo ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. Segoe UI azul ( \# 0066CC)<br/>                  |
| ![primera columna: vínculos (mantener el mouse) ](images/text-ui-image20.png)<br/>               | Acceso frecuente<br/>              | 9 pt. Segoe UI azul claro ( \# 3399FF)<br/>            |
| ![primera columna: encabezado de grupo ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. Segoe UI azul ( \# 003399)<br/>                 |
| ![primera columna: nombre de archivo (en la vista de contenido) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. negro ( \# 000000) Segoe UI<br/>                |
| ![primera columna: texto del documento ](images/text-ui-image23.png)<br/>               | (ninguno)<br/>           | 9 pt. negro ( \# 000000) Calibri<br/>                  |
| ![primera columna: encabezados del documento ](images/text-ui-image24.png)<br/>           | (ninguno)<br/>           | 17 PT. negro ( \# 000000) Calibri<br/>                 |



 

Para obtener más información y ejemplos, vea [Fonts](vis-fonts.md) and [color](vis-color.md).

### <a name="other-text-characteristics"></a>Otras características de texto

**Negrita**

-   **Use en negrita con moderación para atraer la atención a los usuarios de texto que deben leer.** Por ejemplo, los usuarios que examinan una lista de opciones de botón de radio aprecian la visualización de las etiquetas en negrita, para destacar del texto que agrega información complementaria acerca de cada opción. Tenga en cuenta que el uso excesivo de negrita reduce su impacto.
-   **Con datos etiquetados, utilice negrita para resaltar lo que sea más importante para los datos en conjunto.**
    -   En el caso de datos principalmente genéricos (en los que los datos tienen poco significado sin sus etiquetas, como con números o fechas), use etiquetas en negrita y datos sin formato para que los usuarios puedan explorar y comprender más fácilmente los tipos de datos.
    -   Para los datos principalmente autoexplicativos, use etiquetas sin formato y datos en negrita para que los usuarios puedan centrarse en los propios datos.
    -   Como alternativa, puede usar texto gris oscuro para desenfatizar la información menos importante en lugar de usar negrita para resaltar la información más importante.

        ![captura de pantalla de la vista en miniatura del explorador de Windows ](images/text-ui-image25.png)

        En este ejemplo, en lugar de resaltar los datos con negrita, las etiquetas se desdestacan mediante el uso de gris oscuro.

-   **No todas las fuentes admiten negrita, por lo que nunca debe ser crucial para comprender el texto.**

**Cursiva**

-   Use para hacer referencia al texto literalmente. No utilice comillas para este fin.

    **Correcto:**

    Los términos documento y archivo se suelen usar indistintamente.

-   [Se](glossary.md) usa para los mensajes en [cuadros de texto](ctrl-text-boxes.md) y [listas desplegables modificables](/windows/desktop/uxguide/ctrl-drop).

    ![captura de pantalla del cuadro de texto de búsqueda ](images/text-ui-image26.png)

    En este ejemplo, el símbolo del sistema en el cuadro de búsqueda tiene el formato de texto en cursiva.

-   Use de forma moderada para enfatizar palabras específicas como ayuda para la comprensión.
-   **No todas las fuentes admiten cursiva, por lo que nunca debe ser crucial para comprender el texto.**

**Negrita cursiva**

-   No se usa en el texto de la interfaz de usuario.

**Raya**

-   No utilice, excepto los vínculos.
-   No lo use para enfatizar. En su lugar, use cursiva.

### <a name="punctuation&quot;></a>Signos de puntuación

**Puntos**

-   **No coloque al final de las etiquetas de control, las instrucciones principales o los vínculos de ayuda.**
-   Coloque al final de instrucciones complementarias, explicaciones complementarias o cualquier otro texto estático que forme una oración completa.

**Signos de interrogación**

-   **Coloque al final de todas las preguntas.** A diferencia de los puntos, se usan signos de interrogación para todos los tipos de texto.

**Signos de exclamación**

-   En aplicaciones empresariales, evite.
    -   **Excepciones:** Los signos de exclamación a veces se usan en el contexto de finalización de descarga (&quot;Done!") y para llamar la atención al contenido web ("nuevo").

**Comas**

-   En una lista de tres o más elementos, coloque siempre una coma después del elemento siguiente al último de la lista.

**Dos puntos**

-   **Use dos puntos al final de las etiquetas de control externas.** Esto es especialmente importante para la accesibilidad porque algunas tecnologías de ayuda buscan dos puntos para identificar las etiquetas de control.
-   Use un signo de dos puntos para introducir una lista de elementos.

**Puntos suspensivos**

-   **Los puntos suspensivos significan incompletos.** Use puntos suspensivos en el texto de la interfaz de usuario de la siguiente manera:
    -   **Comandos:** Indicar que un comando necesita información adicional. No use puntos suspensivos cuando una acción muestre otra ventana solo cuando se requiera información adicional. Para obtener más información, consulte [botones de comando](ctrl-command-buttons.md).
    -   **Datos:** Indica que el texto se ha truncado.
    -   **Etiquetas:** Indicar que una tarea está en curso (por ejemplo, "buscando...").

        **Sugerencia:** El texto truncado en una ventana o página con espacio sin usar indica un diseño deficiente o un tamaño de ventana predeterminado demasiado pequeño. Procuran los diseños y los tamaños de ventana predeterminados que eliminan o reducen la cantidad de texto truncado. Para obtener más información, vea [Diseño](vis-layout.md).

-   **No haga que los puntos suspensivos sean interactivos.** Para mostrar el texto truncado, deje que los usuarios cambien el tamaño del control para ver más texto o usar un [control de divulgación progresiva](ctrl-progressive-disclosure-controls.md) en su lugar.

**Comillas y apóstrofos**

-   Para hacer referencia al texto literalmente, use el formato de cursiva en lugar de Comillas.
-   Coloque los títulos de ventana y las etiquetas de control entre comillas solo si es necesario para evitar confusiones y no puede dar formato al uso de negrita en su lugar.
-   Para las comillas, se prefieren comillas dobles (""); Evite las comillas simples.

    **Correcto:**

    ¿Está seguro de que desea eliminar la carpeta CAT de Sparky?

    **Incorrecto:**

    ¿Está seguro de que desea eliminar la carpeta CAT de Sparky?

### <a name="capitalization"></a>Uso de mayúsculas

-   **Use mayúsculas y minúsculas de estilo de título para títulos, uso de mayúsculas y minúsculas para todos los demás elementos de la interfaz de usuario.** Hacerlo es más adecuado para el [tono de Windows](text-style-tone.md).

    -   **Excepción:** En el caso de las aplicaciones heredadas, puede usar el uso de mayúsculas de estilo de título para botones de comandos, menús y encabezados de columna si es necesario para evitar la combinación de estilos de capitalización.

        ![captura de pantalla de la hoja de propiedades genérica ](images/text-ui-image27.png)

    Este ejemplo genérico muestra las mayúsculas y minúsculas correctas para las hojas de propiedades.

    ![captura de pantalla del cuadro de diálogo genérico ](images/text-ui-image28.png)

    Este ejemplo genérico muestra las mayúsculas y minúsculas correctas para los diálogos.

-   **En el caso de los nombres de características y tecnologías, es conservador en mayúsculas.** Normalmente, solo los componentes principales deben escribirse en mayúsculas (mediante el uso de mayúsculas del estilo de título).

    **Correcto:**

    Analysis Services, cubos, dimensiones

    Analysis Services es un componente importante de SQL Server, por lo que la capitalización de estilo de título es adecuada; los cubos y las dimensiones son elementos comunes del software de análisis de base de datos, por lo que no es necesario ponerlos en mayúsculas.

-   **En el caso de los nombres de características y tecnologías, sea coherente en mayúsculas.** Si el nombre aparece más de una vez en una pantalla de la interfaz de usuario, siempre debe aparecer de la misma manera. Del mismo modo, en todas las pantallas de la interfaz de usuario del programa, el nombre debe aparecer de forma coherente.
-   No ponga en mayúsculas los nombres de los elementos genéricos de la interfaz de usuario, como la barra de herramientas, el menú, la barra de desplazamiento, el botón y el icono.
    -   **Excepciones:** Barra de direcciones, barra de vínculos.
-   No use todas las letras mayúsculas para las teclas del teclado. En su lugar, siga las mayúsculas y minúsculas utilizadas por los teclados estándar, o en minúsculas si la tecla no está etiquetada en el teclado.

    **Correcto:**

    barra espaciadora, Tab, entrar, Re Pág, Ctrl + Alt + Supr

    **Incorrecto:**

    BARRA ESPACIADORA, TAB, ENTRAR, REPÁG, CTRL + ALT + SUPR

-   **No use todas las letras mayúsculas para enfatizar.** Los estudios han demostrado que es difícil de leer y que los usuarios tienden a considerarlo como "llamativo". En el caso de las advertencias, use un icono de advertencia y una explicación con claridad de la situación. No es necesario agregar, por ejemplo, el término ADVERTENCIA en todas las letras mayúsculas.

Para obtener más información, vea la sección "texto" o "etiquetas" en las instrucciones específicas del componente de la interfaz de usuario.

### <a name="dates-and-times"></a>Fechas y horas

-   **No codifique el formato de fechas y horas.** Respete las opciones de configuración regional y de personalización del usuario para los formatos de fecha y hora. El usuario los selecciona en el elemento del panel de control región y lenguaje.

    ![captura de pantalla de formato de fecha: lunes, 6 de julio de 2009](images/text-ui-image29.png)![captura de pantalla del formato de fecha: 06 de julio de 2009](images/text-ui-image30.png)

    En estos ejemplos de Microsoft Outlook, ambos formatos para la fecha larga son correctos. Reflejan diferentes opciones que los usuarios han realizado en el elemento del panel de control de región y lenguaje.

-   **Use el formato de fecha larga para escenarios que se benefician de tener información adicional.** Use el formato de fecha corta para los contextos que no tengan espacio suficiente para el formato largo. Aunque los usuarios eligen qué información desean incluir en los formatos largo y corto, los diseñadores eligen el formato que se va a mostrar en sus programas según el escenario y el contexto.

    ![captura de pantalla del formato con las fechas de inicio y vencimiento](images/text-ui-image31.png)

    En este ejemplo, el formato de fecha larga ayuda a los usuarios a organizar tareas y fechas límite.

### <a name="globalization-and-localization"></a>Globalización y localización

Globalización significa crear documentos o productos que se pueden usar en cualquier país, región o cultura. La localización significa adaptar documentos o productos para su uso en una configuración regional que no sea la del país o la región de origen. Considere la globalización y la localización al escribir texto de la interfaz de usuario. El programa puede traducirse en otros idiomas y usarse en referencias culturales muy distintas de las suyas propias.

-   En el caso de los controles con contenido variable (como vistas de lista y vistas de árbol), **Elija un ancho adecuado para los datos válidos más largos.**
-   **Incluya espacio suficiente en la superficie de la interfaz de usuario para un 30% adicional** (hasta el 200 por ciento para el texto más corto) para cualquier texto (pero no para los números) que se vaya a localizar. La conversión de un idioma a otro suele cambiar la longitud de línea del texto.
-   No componga cadenas de subcadenas en tiempo de ejecución. En su lugar, use frases completas para que no haya ambigüedad para el traductor.
-   **No utilice un control subordinado, los valores que contiene o su etiqueta de unidades para crear una frase o frase.** Este tipo de diseño no es localizable porque la estructura de oraciones varía con el lenguaje.

    **Incorrecto:**

    ![captura de pantalla de un cuadro de texto dentro de una etiqueta de casilla ](images/text-ui-image32.png)

    **Correcto:**

    ![captura de pantalla de un cuadro de texto después de una etiqueta de casilla ](images/text-ui-image33.png)

    En el ejemplo incorrecto, el cuadro de texto se coloca dentro de la etiqueta de la casilla.

-   No haga que solo forme parte de una frase un vínculo, porque cuando se traduce, es posible que el texto no permanezca junto. Por lo tanto, el texto del vínculo debe formar una oración completa.
    -   **Excepción:** Los vínculos de Glosario se pueden insertar en línea, como parte de una oración.

Para obtener más información, vea el [Centro para desarrolladores de go global](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Texto de la barra de título

-   Elija el texto de la barra de título según el tipo de ventana:
    -   **Ventanas de programa de nivel superior centradas en documentos:** Use un formato de nombre de programa nombre de documento. Los nombres de documento se muestran en primer lugar para dar una sensación centrada en el documento.
    -   **Ventanas de programa de nivel superior que no están centradas en documentos:** Mostrar solo el nombre del programa.
    -   **Cuadros de diálogo:** Mostrar el comando, la característica o el programa desde el que procede el cuadro de diálogo. No use el título para explicar el propósito del cuadro de diálogo que es el propósito de las instrucciones principales. Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).
    -   **Asistentes:** Mostrar el nombre del asistente. Tenga en cuenta que la palabra "Asistente" no debe incluirse en los nombres de los asistentes. Para obtener más instrucciones, consulte [asistentes](win-wizards.md).
-   **En las ventanas de programa de nivel superior, si el título y el icono de la barra de título se muestran de forma destacada en la parte superior de la ventana, puede ocultar el título y el icono de la barra de título para evitar la redundancia.** Sin embargo, todavía tiene que establecer un título adecuado internamente para su uso por parte de Windows.
-   **En el caso de los cuadros de diálogo, no incluya las palabras "Dialog" o "Progress" en los títulos.** Estos conceptos están implícitos y si se dejan estas palabras, los títulos se facilitan a los usuarios.

### <a name="main-instructions"></a>Instrucciones principales

-   **Use la instrucción principal para explicar de manera concisa qué deben hacer los usuarios en una determinada ventana o página.** Las buenas instrucciones principales comunican el objetivo del usuario en lugar de centrarse simplemente en manipular la interfaz de usuario.
-   **Exprese la instrucción principal en forma de dirección imperativa o pregunta específica.**

    **Incorrecto:**

    ![captura de pantalla del nombre del programa como instrucción principal ](images/text-ui-image34.png)

    En este ejemplo, la instrucción principal simplemente indica el nombre del programa; no invita explícitamente a un curso de acción que el usuario realice.

    **Excepciones:** Los mensajes de error, los mensajes de advertencia y las confirmaciones pueden usar estructuras de oraciones diferentes en sus instrucciones principales.

-   **Use verbos específicos siempre que sea posible.** Los verbos específicos (ejemplos: Connect, Save, install) son más significativos para los usuarios que los genéricos (por ejemplo: configurar, administrar, establecer).
    -   En el caso de las páginas del panel de control y las páginas del asistente, si no puede usar un verbo específico, puede que prefiera omitir el verbo por completo.

        **Aceptable:**

        Escriba la configuración regional, la región y el idioma

        **Manera**

        Configuración regional, región e idioma

    -   En el caso de los cuadros de diálogo, como los mensajes de error y las advertencias, no omita el verbo.

-   No dude en usar el texto de la instrucción principal si agregarlo solo sería redundante o obvio en el contexto de la interfaz de usuario.

    ![captura de pantalla del cuadro de diálogo Guardar como ](images/text-ui-image35.png)

    En este ejemplo, el contexto de la interfaz de usuario ya está muy claro; no es necesario agregar texto de instrucción principal.

-   **Sea conciso usar una sola oración completa.** Reduzca la instrucción principal a la información esencial. Si debe explicar algo más, considere la posibilidad de usar una instrucción complementaria.
-   Use mayúsculas de estilo de frase.
-   **No incluya los períodos finales si la instrucción es una instrucción.** Si la instrucción es una pregunta, incluya un signo de interrogación final.
-   **En el caso de los cuadros de diálogo de progreso, utilice una frase de gerundio que explique brevemente la operación en curso y** termine con puntos suspensivos. Ejemplo: "imprimir imágenes..."
-   **Sugerencia:** Puede evaluar una instrucción principal deimaginando lo que diría a un amigo al explicar qué hacer con la ventana o la página. Si responder con la instrucción principal sería no natural, no práctico o complicado, retrabaje la instrucción.

Para obtener más información, vea la sección "instrucción principal" en las instrucciones específicas del componente de interfaz de usuario.

### <a name="supplemental-instructions"></a>Instrucciones complementarias

-   Cuando sea necesario, **use una instrucción complementaria para presentar información adicional útil para comprender o usar la ventana o la página,** por ejemplo:
    -   Proporcionar contexto para explicar por qué se muestra la ventana si es un programa o un sistema iniciado.
    -   Información calificada que ayuda a los usuarios a decidir cómo actuar en la instrucción principal.
    -   Definir terminología importante.
-   **No use una instrucción complementaria Si no es necesario.** Prefiera comunicar todo con la instrucción principal si puede hacerlo de manera concisa.
-   **No repita la instrucción principal con un texto ligeramente diferente.** En su lugar, omita la instrucción complementaria Si no hay nada más que agregar.
-   Use frases completas y uso de mayúsculas del estilo de oraciones.

### <a name="control-labels"></a>Etiquetas de control

-   **Etiquete todos los controles o grupos de controles. Excepciones**
    -   Los cuadros de texto y las listas desplegables se pueden etiquetar mediante mensajes.
    -   Normalmente, los controles de divulgación progresiva no tienen etiqueta.
    -   **Los controles subordinados utilizan la etiqueta de su control asociado.** Los controles de número siempre son controles subordinados.
    -   **Omita las etiquetas de control que representen la instrucción principal.** En este caso, la instrucción principal toma la clave de acceso.

        **Aceptable:**

        ![captura de pantalla de un cuadro de texto con una instrucción y una etiqueta ](images/text-ui-image36.png)

        En este ejemplo, la etiqueta del cuadro de texto es simplemente una resituación de la instrucción principal.

        **Manera**

        ![captura de pantalla de un cuadro de texto con solo instrucciones ](images/text-ui-image37.png)

        En este ejemplo, se quita la etiqueta redundante, por lo que la instrucción principal toma la clave de acceso.

-   Ubicación de la etiqueta:
    -   Los globos, las casillas, los botones de comando, los cuadros de grupo, los vínculos, las pestañas y las sugerencias se etiquetan directamente por el propio control.
    -   Las listas desplegables, los cuadros de lista, las vistas de lista, las barras de progreso, los controles deslizantes, los cuadros de texto y las vistas de árbol se etiquetan arriba, vaciar a la izquierda o a la izquierda.
    -   Normalmente, los controles de divulgación progresiva no tienen etiqueta. Los botones de cheurones se etiquetan a la derecha.
-   **Asigne una clave de acceso única para cada control interactivo** , excepto para los vínculos. Para obtener más información, consulte [teclado](inter-keyboard.md).
-   **Conserve las etiquetas breves.** Sin embargo, tenga en cuenta que agregar una palabra o dos a una etiqueta puede ayudar a aclarar y, a veces, elimina la necesidad de explicaciones complementarias.
-   **Prefiere etiquetas específicas sobre las genéricas.** Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta.

    **Incorrecto:**

    ![captura de pantalla del botón de comando aceptar ](images/text-ui-image38.png)

    **Correcto:**

    ![captura de pantalla del botón de comando publicar ](images/text-ui-image39.png)

    En el ejemplo correcto, se usa una etiqueta específica para el botón confirmar.

-   **En el caso de las listas de etiquetas, como botones de radio, use frases paralelas** e intente mantener la longitud sobre la misma en todas las etiquetas.
-   **En las listas de etiquetas, Centre el texto de la etiqueta en las diferencias entre las opciones.** Si todas las opciones tienen el mismo texto de introducción, mueva el texto a la etiqueta de grupo.

    **Incorrecto:**

    ![captura de pantalla de etiquetas con primeras frases duplicadas](images/text-ui-image40.png)

    **Correcto:**

    ![captura de pantalla de la primera frase movida a la etiqueta de grupo](images/text-ui-image41.png)

    En el ejemplo correcto se mueve la frase de introducción idéntica a la etiqueta, por lo que las dos opciones se diferencian más claramente.

-   **En general, se prefiere la formulación positiva.** Por ejemplo, use do en lugar de no y Notify en lugar de no notificar.
    -   **Excepción:** La etiqueta de la casilla "no volver a mostrar este mensaje" se usa con frecuencia.
-   **Omite los verbos de instrucciones que se aplican a todos los controles del tipo dado.** En su lugar, se centran en lo que es único sobre los controles. Por ejemplo, va sin indicar que los usuarios deben escribir en un control de cuadro de texto o que los usuarios tengan que hacer clic en un vínculo.

    **Incorrecto:**

    ![captura de pantalla de la etiqueta: ' escriba su nombre ' ](images/text-ui-image42.png)

    **Correcto:**

    ![captura de pantalla de la etiqueta: ' your name ' ](images/text-ui-image43.png)

    En los ejemplos incorrectos, las etiquetas de control tienen verbos de instrucciones que se aplican a todos los controles de su tipo.

-   En algunos casos, las siguientes anotaciones entre paréntesis para controlar las etiquetas pueden resultar útiles:
    -   **Si una opción es opcional, considere la posibilidad de agregar "(opcional)" a la etiqueta.**
    -   **Si se recomienda una opción, agregue "(recomendado)" a la etiqueta.** Esto significa que la configuración es opcional, pero debe establecerse de todos modos.
    -   **Si una opción está pensada solo para usuarios avanzados, considere la posibilidad de agregar "(avanzado)" a la etiqueta.**
-   Puede especificar unidades (segundos, conexiones, etc.) entre paréntesis después de la etiqueta.

    ![captura de pantalla de la etiqueta: tamaño inicial (MB) ](images/text-ui-image44.png)

    Este ejemplo muestra que la unidad de medida es megabytes (MB).

Para obtener más información, vea la sección "texto" o "etiquetas" en las instrucciones específicas del componente de la interfaz de usuario.

### <a name="supplemental-explanations"></a>Explicaciones complementarias

-   **Use explicaciones complementarias cuando los controles requieran más información de la que se puede transmitir por su etiqueta.** Pero no use una explicación complementaria Si no es necesario para comunicar todo con la etiqueta de control si puede hacerlo de manera concisa. Normalmente, las explicaciones complementarias se utilizan con vínculos de comandos, botones de radio y casillas.
-   Cuando sea necesario, **utilice negrita en las etiquetas de control para facilitar el análisis del texto** cuando haya explicaciones complementarias.

    ![captura de pantalla del cuadro de diálogo Configuración de seguridad ](images/text-ui-image45.png)

    En este ejemplo, las etiquetas de botón de radio están en negrita para facilitar su examen.

-   **Agregar una explicación complementaria a un control de un grupo no significa que tenga que proporcionar explicaciones para todos los demás controles del grupo.** Proporcione la información relevante en la etiqueta si puede y use explicaciones solo cuando sea necesario. No tenga explicaciones complementarias que simplemente representen la coherencia de la etiqueta.

    ![captura de pantalla de tres botones de radio ](images/text-ui-image46.png)

    En este ejemplo, dos controles del grupo incluyen explicaciones complementarias, pero el tercero no.

-   Si una explicación complementaria sigue a un vínculo de comando, escriba el texto complementario en la segunda persona.

    **Ejemplo:** Comando link: creación de la configuración de red inalámbrica y guardado en una unidad flash USB

    Explicación complementaria: se creará una configuración que se puede transferir al enrutador con una unidad flash USB. Haga esto solo si tiene un enrutador inalámbrico que admita la configuración de la unidad flash USB.

-   Usar frases completas y puntuación final.

### <a name="commit-button-labels"></a>Etiquetas del botón de confirmación

En la tabla siguiente se muestran las etiquetas de botón de confirmación más comunes y su uso.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Etiqueta del botón</strong><br/></td>
<td><strong>Significado</strong><br/></td>
<td><strong>Cuándo se deben usar</strong><br/></td>
<td><strong>Clave de acceso</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK (CORRECTO)</strong><br/></td>
<td><ul>
<li>En los cuadros de diálogo: Aplique los cambios o confirme la tarea y cierre la ventana.</li>
<li>En ventanas de propiedades de propietario: Aplique los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se aplicó) y cierre la ventana.</li>
<li>En ventanas de propiedades de propiedad: Mantenga los cambios, cierre la ventana y aplique los cambios cuando se apliquen los cambios de la ventana propietaria.</li>
</ul></td>
<td><ul>
<li>Se usa con ventanas que no son específicas de las tareas, como las hojas de propiedades.</li>
<li>En el caso de las ventanas que se usan para realizar una tarea específica, utilice en su lugar una etiqueta específica que empiece por un verbo (por ejemplo: imprimir).</li>
<li>En Windows en el que los usuarios no pueden realizar cambios, use cerrar.</li>
</ul></td>
<td>Entrar<br/></td>
</tr>
<tr class="odd">
<td><strong>Sí/no</strong><br/></td>
<td>Sí es la respuesta afirmativa a una pregunta sí o no, mientras que no es la respuesta negativa.<br/></td>
<td><ul>
<li>Use los botones sí y no solo para responder a preguntas sí o no. Nunca use aceptar y Cancelar para responder a preguntas o respuestas.</li>
<li>Prefiere respuestas específicas sobre los botones sí y no. Aunque no hay ningún problema con el uso de sí y no, las respuestas específicas se pueden entender más rápidamente, lo que da lugar a una toma de decisiones eficaz.</li>
<li>Sin embargo, considere la posibilidad de usar respuestas sí y no si la formulación de respuestas específicas resulta ser larga o complicada.</li>
<li>No use los botones sí y no si el significado de la respuesta no es claro. Si es así, use respuestas específicas en su lugar.</li>
<li>Sí y no deben usarse siempre como un par.</li>
</ul></td>
<td>Y y N<br/></td>
</tr>
<tr class="even">
<td><strong>Cancelar</strong><br/></td>
<td><ul>
<li>En los cuadros de diálogo: descartar todos los cambios o el trabajo en curso, revertir al estado anterior (no dejar ningún efecto secundario perceptible) y cerrar la ventana.</li>
<li>En las hojas de propiedades: descartar todos los cambios pendientes (realizados desde que se abrió la ventana o la última vez que se aplicó) y cerrar la ventana.</li>
<li>En elementos del panel de control: descartar todos los cambios o el trabajo en curso, revertir al estado anterior y volver a la página del concentrador desde la que se inició la tarea. Si no hay ninguna página del concentrador, cierre la ventana elemento del panel de control en su lugar.</li>
</ul></td>
<td><ul>
<li>Use cuando se puedan descartar todos los cambios o acciones pendientes y se pueden deshacer los efectos secundarios.</li>
<li>En el caso de los cambios que no se pueden descartar, use cerrar. Para las acciones en curso que se pueden detener, utilice STOP. Si los cambios o acciones inicialmente se pueden descartar, puede usar cancelar inicialmente y cambiar a cerrar o detener una vez que no se puede deshacer.</li>
</ul></td>
<td>Esc<br/></td>
</tr>
<tr class="odd">
<td><strong>Cerrar</strong><br/></td>
<td>Cierre la ventana. No se descartan los cambios ni los efectos secundarios.<br/></td>
<td><ul>
<li>Se usa cuando no se pueden descartar los cambios o efectos secundarios. Use cerrar en lugar de cancelar para las ventanas principales.</li>
<li>Se usa para ventanas en las que los usuarios no pueden realizar cambios.</li>
</ul></td>
<td>Alt + F4, Ctrl + F4<br/></td>
</tr>
<tr class="even">
<td><strong>Detención</strong><br/></td>
<td>Detener una tarea que se está ejecutando actualmente y cerrar la ventana. No se descartan los trabajos en curso o los efectos secundarios.<br/></td>
<td><ul>
<li>Se usa cuando el trabajo en curso y los efectos secundarios no se pueden descartar, normalmente con barras de progreso o animaciones.</li>
</ul></td>
<td>Esc<br/></td>
</tr>
<tr class="odd">
<td><strong>Aplicar</strong><br/></td>
<td>En hojas de propiedades de propietario: Aplique los cambios pendientes (realizados desde que se abrió la ventana o la última aplicación), pero deje la ventana abierta. Esto permite a los usuarios evaluar los cambios antes de cerrar la hoja de propiedades. En las hojas de propiedades de propiedad: no use.<br/></td>
<td><ul>
<li>Úselo solo en hojas de propiedades.</li>
<li>Proporcione un botón Aplicar solo si la hoja de propiedades tiene valores de configuración (al menos uno) con efectos que los usuarios pueden evaluar de forma significativa. Normalmente, se usan botones aplicar cuando la configuración realiza cambios visibles. Los usuarios deben poder aplicar un cambio, evaluar el cambio y realizar cambios adicionales en función de esa evaluación. Si no es así, quite el botón aplicar en lugar de deshabilitarlo.</li>
</ul></td>
<td>A<br/></td>
</tr>
<tr class="even">
<td><strong>Siguiente</strong><br/></td>
<td>En los asistentes y en las tareas de varios pasos: avance al paso siguiente sin confirmar la tarea.<br/></td>
<td><ul>
<li>Use solo en asistentes y tareas de varios pasos para avanzar al siguiente paso sin compromiso.</li>
<li>El efecto de un botón siguiente siempre se puede deshacer haciendo clic en atrás.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Finalizar</strong><br/></td>
<td>En los asistentes y en las tareas de varios pasos: cierre la ventana. Si aún no se ha realizado la tarea, realice la tarea. Si ya se ha realizado esa tarea, no se descartarán los cambios o efectos secundarios.<br/></td>
<td><ul>
<li>Úselo solo en los asistentes y en las tareas de varios pasos. Sin embargo, no se recomienda el uso de Finish porque normalmente hay un botón de confirmación mejor y más específico:
<ul>
<li>Si al hacer clic en el botón se confirma la tarea (por lo que no se ha realizado ya la tarea), use una etiqueta específica que comience por un verbo (ejemplos: Print, Connect, Start) que es una respuesta a la instrucción principal.</li>
<li>Si la tarea ya se ha realizado en el asistente, utilice Close en su lugar.</li>
</ul></li>
<li>Sin embargo, puede usar finalizar cuando:
<ul>
<li>La etiqueta específica sigue siendo genérica, como guardar, seleccionar, elegir o obtener.</li>
<li>La tarea implica cambiar una configuración o una colección de valores de configuración.</li>
</ul></li>
</ul></td>
<td>Entrar<br/></td>
</tr>
<tr class="even">
<td><strong>Listo</strong><br/></td>
<td>No es aplicable.<br/></td>
<td><ul>
<li>No use. El hecho de que un comando sea gramaticalmente incorrecto.</li>
</ul></td>
<td>No es aplicable.<br/></td>
</tr>
</tbody>
</table>



 


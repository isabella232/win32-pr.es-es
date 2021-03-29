---
title: Cómo la automatización de la interfaz de usuario expone objetos incrustados
description: En este tema se describe cómo Microsoft UI Automation expone objetos incrustados o elementos secundarios en un documento o contenedor de texto.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- UI Automation, información general sobre el patrón de texto
- Automatización de la interfaz de usuario, información general sobre controles de texto
- Automatización de la interfaz de usuario, patrón de control Text
- Automatización de la interfaz de usuario, información general sobre objetos incrustados
- Automatización de la interfaz de usuario, exponer objetos incrustados
- Automatización de la interfaz de usuario, escenarios para objetos incrustados
- patrones de texto, acerca de
- controles de texto, acerca de
- Text (patrón de control)
- patrones de control, texto
- objetos incrustados
- exponer objetos incrustados
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: b85d7fa9e068400e3a339625acad1036a4cdd111
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791782"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Cómo la automatización de la interfaz de usuario expone objetos incrustados

En este tema se describe cómo automatización de la interfaz de usuario de Microsoft usa los patrones de control Text y TextRange para exponer objetos incrustados (elementos secundarios/descendientes) en un documento o contenedor de texto.

Para la automatización de la interfaz de usuario, un objeto incrustado es cualquier elemento que tenga límites no textuales como una imagen, un hipervínculo, una tabla o un tipo de documento (hoja de cálculo de Microsoft Excel, archivo de Microsoft Windows Media, etc.).

> [!NOTE]
> Esto difiere de la definición OLE de modelo de objetos componentes (COM) (vea [objetos incrustados](../com/embedded-objects.md)), donde se crea un elemento en una aplicación y se incrusta o vincula en otra aplicación. El hecho de que el objeto pueda editarse en su aplicación original es irrelevante en el contexto de la automatización de la interfaz de usuario.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Objetos incrustados y el árbol de automatización de la interfaz de usuario

Los objetos incrustados se tratan como elementos individuales en la vista de control del árbol de automatización de la interfaz de usuario. Se exponen como elementos secundarios del contenedor de texto para que se pueda tener acceso a ellos a través del mismo modelo de objetos que otros controles de la automatización de la interfaz de usuario.

En la tabla siguiente se muestran ejemplos de elementos contenedores y no contenedores.

:::row:::
   :::column span="2":::

      **Elementos de contenedor**

   :::column-end:::
   :::column span="":::

      **Elementos que no son contenedores**

   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::

- Calendario
- ComboBox
- DataGrid
- Documento
- Editar
- Grupo
- Encabezado
- HeaderItem
- List
- Menú

   :::column-end:::
   :::column span="":::

- MenuBar
- Panel
- SplitButton
- Pestaña
- Tabla
- Barra de herramientas
- Árbol
- TreeItem
- Periodo

   :::column-end:::
   :::column span="":::

- Link
- Casillas
- Botón

  :::column-end:::
:::row-end:::

La siguiente imagen muestra un contenedor de texto (documento) con una tabla e imagen incrustada.

![Ilustración en la que se muestra un documento con una tabla e imagen incrustada](images/embeddedtable.jpg)

En el diagrama siguiente se muestra la vista de contenido de automatización de la interfaz de usuario del documento anterior.

![diagrama de la vista de contenido de automatización de la interfaz de usuario de un documento con objetos incrustados](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Objetos incrustados "compatibles" y "no compatibles"

Algunos proveedores de automatización de la interfaz de usuario usan el mismo almacén de texto para cada objeto TextPattern que contienen.  Los objetos respaldados por el mismo almacén de texto que su contenedor se conocen como objetos incrustados "compatibles". Estos objetos pueden ser objetos TextPattern y, en este caso, sus intervalos de texto son comparables a los intervalos de texto obtenidos de su contenedor. Esto permite a los proveedores exponer información del cliente sobre los objetos TextPattern individuales como si fueran un proveedor de texto grande.

Sin embargo, los proveedores pueden usar almacenes de texto diferentes para los distintos objetos TextPattern insertados en un contenedor TextPattern. Los objetos no respaldados por el almacén de texto del contenedor se conocen como objetos incrustados "no compatibles". Estos tipos de objetos incrustados pueden ser o no objetos basados en TextPattern.  

En la tabla siguiente se enumeran algunos ejemplos de objetos incrustados compatibles y no compatibles.

|   | Objetos incrustados compatibles | Objetos incrustados no compatibles |
| --- | --- | --- |
| Objetos incrustados que no son TextPattern | Botón en Microsoft Edge<br>Tabla de datos en Microsoft Edge | Botón de RichTextBlock en el marco XAML de Microsoft<br>Imágenes con texto alternativo en Microsoft Edge<br>ListView con ListItems en RichTextBlock en el marco XAML de Microsoft |
| Objetos incrustados de TextPattern | Control de entrada de tipo "Text" en Microsoft Edge<br>Tabla en un documento de Word | Elemento TextBox en un documento de Microsoft Word |

## <a name="exposing-embedded-objects"></a>Exponer objetos incrustados

Los patrones de control [Text y TextRange](uiauto-implementingtextandtextrange.md) exponen propiedades y métodos que facilitan la navegación y la consulta de objetos incrustados.

El contenido textual (o texto interno) de un contenedor de texto y un objeto incrustado, como un hipervínculo o una celda de tabla, se expone como una secuencia de texto continua única en la vista de control y la vista de contenido del árbol de automatización de la interfaz de usuario; los límites de los objetos se omiten. Si un cliente de automatización de la interfaz de usuario recupera el texto para recitar, interpretar o analizar de alguna manera, el intervalo de texto se debe comprobar en casos especiales, como una tabla con contenido textual u otros objetos incrustados. Llame a [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) para obtener una interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para cada objeto incrustado y, a continuación, llame a [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) para obtener un intervalo de texto para cada elemento. Esto se realiza recursivamente hasta que se recupera todo el contenido textual.

> [!NOTE]
> Un intervalo degenerado (o contraído) es donde el extremo inicial y el extremo final son iguales. Los intervalos degenerados se suelen usar para indicar la posición del cursor de texto a través de los métodos [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) [getSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) y [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) .

En el diagrama siguiente se muestra una secuencia de texto con objetos incrustados y sus intervalos de intervalos.

![diagrama que muestra una secuencia de texto con objetos incrustados y sus intervalos de intervalos](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Objetos incrustados y TextUnit

Un objeto [ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) se puede atravesar y por un [TextUnit](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit)especificado. Los proveedores que contienen objetos incrustados se pueden recorrer de la misma manera, pero los objetos incrustados afectan al recorrido. Estas son algunas de las cosas que debe tener en cuenta:

- Cualquier objeto incrustado no compatible se representa mediante el carácter de reemplazo U + FFFC en el almacén de texto de TextPattern del elemento contenedor. También se considera una unidad de caracteres y una unidad de palabra.
- Los objetos incrustados compatibles pueden constar de varios caracteres y palabras.
- El elemento envolvente es el elemento situado más abajo que abarca todo el intervalo de texto.
- Los elementos secundarios de un intervalo también son elementos secundarios de un elemento contenedor que está parcial o totalmente dentro del intervalo.
- Idealmente (especialmente en el caso de elementos de contenedor como tabla), un límite de palabra no va más allá del límite del objeto. En el ejemplo siguiente, la palabra "bar" de unidad no contiene ninguna posición de texto que esté fuera de la `</td>` etiqueta ( `<br \>` no forma parte de la palabra "bar").

```Xaml
<table style="width:100%">
  <tr>
    <th>Name</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>Eve Jackson</td>
    <td>Foo Bar</td>
  </tr>
</table>
<br/>
```

- En general, `<br \>` se trata como una palabra individual que no va más allá de un límite de línea.
- Una excepción a la regla anterior es donde una unidad de texto de Word contiene objetos completos dentro de sí mismo. Por ejemplo, `<p>Hello <a href="#">link</a> here.</p>` , que incluye contenedores en línea, tiene las palabras "Hola", "vínculo" y "aquí". Donde "link" tiene un objeto TextPattern como elemento envolvente y un objeto de vínculo como su elemento secundario.
- En el caso de las unidades de carácter, el objeto es el elemento envolvente (las unidades de texto como esta no deberían tener elementos secundarios).
- Los objetos de anotación no deben representarse como objetos incrustados. Por ejemplo, la presencia de otros especificadores de autor en un documento con co-autoría.
- Los objetos incrustados ocupan al menos una posición del cursor. la anotación es simplemente metadatos.
- Cada límite de objeto (inicio y fin) se representa mediante una interrupción de formato en el intervalo del documento TextPattern.
- En el caso de HTML, cada etiqueta HTML no tiene necesariamente como resultado un objeto de automatización de la interfaz de usuario. Por ejemplo, el contenido de las <em></em> etiquetas de énfasis no debe representarse como elemento sino en una secuencia de texto en la que UIA_IsItalicAttributeId devuelve true.
- El punto de conexión inicial es inclusivo y es el punto de conexión preferido mientras el extremo final es exclusivo. Esto resulta útil cuando se genera el intervalo y los puntos de conexión inicial y final pertenecen a la misma posición para ese intervalo.

## <a name="comparing-embedded-objects"></a>Comparar objetos incrustados

Los objetos TextPattern anidados que se encuentran en una relación secundaria similar y comparten el mismo almacén de texto de respaldo se denominan comparables. En este caso, los intervalos de cualquiera de los objetos TextPattern se pueden comparar mediante [ITextRangeProvider:: Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) y [ITextRangeProvider:: CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Ambos dan como resultado un valor numérico válido que especifica su posición relativa.

Un objeto no TextPattern incrustado en un objeto TextPattern es comparable con TextPattern si el objeto tiene un intervalo válido en TextPattern ([ITextProvider:: RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) y el contenido detrás del intervalo de texto no está vacío y no es un carácter de reemplazo.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Objetos TextPattern incrustados y el documento TextUnit

En el caso de los objetos TextPattern incrustados, la unidad del [documento](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) solo reconoce el contenido incluido en ese elemento.

### <a name="word-textpattern-element-hierarchy"></a>Jerarquía de elementos TextPattern de Word

- El elemento de documento implementa TextPattern y [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) devuelve todo el intervalo de documentos de Word.
- Las páginas individuales del documento implementan TextPattern y [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) devuelven el contenido de esas páginas individuales (aunque las páginas compartan el mismo almacén de texto con todo el documento Textpattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Controles de entrada de texto y página web en Edge

- El elemento principal panel de página web implementa TextPattern y expone todo el contenido de la Página Web.
- Los controles de entrada de texto individuales admiten TextPattern, donde un intervalo de documentos representa el texto contenido en cada campo de entrada (aunque comparta el mismo almacén de texto con toda la página web).

## <a name="common-scenarios"></a>Escenarios comunes

En esta sección se presentan ejemplos de escenarios comunes que implican objetos incrustados: hipervínculos, imágenes y tablas. En los ejemplos siguientes, la llave de apertura ({) representa el punto de conexión de inicio del intervalo de texto y la llave de cierre (}) representa el punto de conexión final.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Ejemplo de hipervínculo 1: intervalo de texto que contiene un hipervínculo de texto incrustado

El siguiente intervalo de texto contiene un hipervínculo de texto incrustado.

  {La dirección URL https://www.microsoft.com está incrustada en el texto}.

La llamada a los métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)y [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                     | Resultado                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Devuelve la cadena "la dirección URL https://www.microsoft.com está incrustada en el texto".                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Devuelve el elemento de automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento de automatización que representa al propio proveedor de texto. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Devuelve un elemento de automatización de la interfaz de usuario que representa el control de hipervínculo.                                                                                      |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), donde el método [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) anterior devolvió el elemento de automatización de la interfaz de usuario. | Devuelve el intervalo que representa " https://www.microsoft.com ".                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Hipervínculo ejemplo 2: intervalo de texto que se extiende parcialmente por un hipervínculo de texto incrustado

El intervalo de texto siguiente abarca parcialmente un hipervínculo de texto incrustado.

  La dirección URL https://{www} está incrustada en el texto.

La llamada a los métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                            | Resultado                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Devuelve la cadena "www".                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Devuelve el elemento de automatización de la interfaz de usuario más interno que incluye el intervalo de texto; en este caso, el control de hipervínculo. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Devuelve **null** porque el intervalo de texto no abarca toda la cadena de dirección URL.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Ejemplo de hipervínculo 3: intervalo de texto que se extiende parcialmente por el contenido de un contenedor de texto

El intervalo de texto siguiente abarca parcialmente el contenido de un contenedor de texto. El contenedor de texto incluye un hipervínculo de texto incrustado que no forma parte del intervalo de texto.

  {La dirección URL} https://www.microsoft.com está incrustado en el texto.

La llamada a los métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                            | Resultado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Devuelve la cadena "La dirección URL".                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Devuelve el elemento de automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa al propio proveedor de texto.                                                                                     |
| [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Mueve el intervalo de texto a "https://" porque el texto del hipervínculo se compone de palabras individuales. En este caso, el hipervínculo no se considera un único objeto.<br/> La dirección URL {http} está incrustada en el texto.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Imagen de ejemplo 1: intervalo de texto que contiene una imagen incrustada

El siguiente intervalo de texto contiene una imagen incrustada de un control de navegación.

 {La imagen ![Ilustración de un control de navegación](images/shuttle.jpg) está incrustado en el texto}.

La llamada a los métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)y [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                    | Resultado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Devuelve la cadena "la imagen está incrustada en el texto". Cualquier texto alternativo asociado a la imagen no se incluye en la secuencia de texto.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Devuelve el elemento de automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa al propio proveedor de texto. |
| [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Devuelve un elemento de automatización de la interfaz de usuario que representa el control de imagen.                                                                               |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) donde el método [**IUIAutomationTextRange:: GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) anterior devolvió el elemento de automatización de la interfaz de usuario. | Devuelve el intervalo degenerado.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Ejemplo de imagen 2: intervalo de texto que se extiende parcialmente por el contenido de un contenedor de texto

El intervalo de texto siguiente abarca parcialmente el contenido de un contenedor de texto. El contenedor de texto incluye una imagen incrustada que no forma parte del intervalo de texto.

 {La imagen} ![Ilustración de un control de navegación](images/shuttle.jpg) está incrustado en el texto.

La llamada a los métodos [**IUIAutomationTextRange:: gettext**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                          | Resultado                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Devuelve la cadena "La imagen".                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Devuelve el elemento de automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa al propio proveedor de texto.                                                                                                                                   |
| [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) con parámetros de (**TextUnit \_ Word**, 2). | Mueve el intervalo de texto a "está". Dado que solo se consideran parte de la secuencia de texto los objetos incrustados basados en texto, la imagen de este ejemplo no afecta a [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) ni a su valor devuelto, en este caso, 2. |

### <a name="table"></a>Tabla

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Ejemplo 1 de tabla: obtiene el contenedor de texto del contenido de una celda.

En la tabla siguiente se obtiene el contenedor de texto del contenido de una celda.

| Celda con imagen                                            | Celda con texto |
|------------------------------------------------------------|----------------|
| ![Ilustración de un control de navegación](images/shuttle.jpg)           | X              |
| ![Ilustración de espacio y un telescopio](images/space.jpg) | Y              |
| ![Ilustración de un microscopio](images/microscope.jpg)     | Z              |

La llamada a los métodos [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)y [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                       | Resultado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parámetros (0,0).                                                                                                                        | Devuelve el elemento de automatización de la interfaz de usuario que representa el contenido de la celda de la tabla; en este caso, el elemento es un control de texto.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | Devuelve el intervalo de la imagen. ![Ilustración de un control de navegación](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para el objeto devuelto por el método [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) anterior. | Devuelve el elemento de automatización de la interfaz de usuario que representa la celda de la tabla. En este caso, el elemento es un control de texto que admite el patrón de control [TableItem](uiauto-implementingtableitem.md) . |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para el objeto devuelto por el método **GetEnclosingElement** anterior.                                                    | Devuelve el elemento de automatización de la interfaz de usuario que representa la tabla.                                                                                                                                   |
| [**IUIAutomationTextRange:: GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para el objeto devuelto por el método **GetEnclosingElement** anterior.                                                    | Devuelve el elemento de automatización de la interfaz de usuario que representa el propio proveedor de texto.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Ejemplo de tabla 2: obtiene el contenido de texto de una celda

En la tabla del ejemplo anterior se obtiene el contenido de texto de una celda.

La llamada a los métodos [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) y [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                          | Resultado                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parámetros (1,1).                                                                                                                                                            | Devuelve el elemento de automatización de la interfaz de usuario que representa el contenido de la celda de la tabla. En este caso, el elemento es un control de texto. |
| [**IUIAutomationTextPattern:: RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) donde el elemento de automatización de la interfaz de usuario es el objeto devuelto por el método [**IUIAutomationGridPattern:: GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) anterior. | Devuelve "Y".                                                                                                               |

Al desplazarse por un documento por la [**\_ línea TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si el intervalo de texto entra en una tabla incrustada, cada línea de texto de una celda se debe tratar como una línea.

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

- [Acerca de los patrones de control Text y TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Atributos de texto de automatización de la interfaz de usuario](uiauto-textattributes.md)
- [Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
- [Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)
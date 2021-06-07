---
title: Cómo Automatización de la interfaz de usuario expone objetos incrustados
description: En este tema se describe cómo Microsoft Automatización de la interfaz de usuario expone objetos incrustados o elementos secundarios en un documento o contenedor de texto.
ms.assetid: 5ecf5e94-5329-4abb-aedb-4e303688e5f7
keywords:
- Automatización de la interfaz de usuario,introducción al patrón de texto
- Automatización de la interfaz de usuario información general sobre los controles de texto
- Automatización de la interfaz de usuario,patrón de control Text
- Automatización de la interfaz de usuario información general sobre los objetos incrustados
- Automatización de la interfaz de usuario, exponer objetos incrustados
- Automatización de la interfaz de usuario, escenarios para objetos incrustados
- patrones de texto, acerca de
- controles de texto, acerca de
- Patrón de control de texto
- patrones de control, texto
- objetos incrustados
- exponer objetos incrustados
ms.topic: article
ms.date: 08/31/2019
ms.openlocfilehash: 8e9e0a8b9f70677778238908f8faf04e21ed9619
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443326"
---
# <a name="how-ui-automation-exposes-embedded-objects"></a>Cómo Automatización de la interfaz de usuario expone objetos incrustados

En este tema se describe cómo Microsoft Automatización de la interfaz de usuario usa los patrones de control Text y TextRange para exponer objetos incrustados (elementos secundarios o descendientes) en un documento o contenedor de texto.

Por Automatización de la interfaz de usuario, un objeto incrustado es cualquier elemento que tenga límites no textuales, como una imagen, un hipervínculo, una tabla o un tipo de documento (hoja de cálculo de Microsoft Excel, archivo de Microsoft Windows Media, entre otros).

> [!NOTE]
> Esto difiere de la definición OLE del Modelo de objetos componentes (COM) (vea [Objetos](../com/embedded-objects.md)incrustados), donde se crea un elemento en una aplicación y se inserta o vincula en otra aplicación. Si el objeto se puede editar en su aplicación original es irrelevante en el contexto de Automatización de la interfaz de usuario.

## <a name="embedded-objects-and-the-ui-automation-tree"></a>Objetos incrustados y el árbol de automatización de la interfaz de usuario

Los objetos incrustados se tratan como elementos individuales en la vista de control Automatización de la interfaz de usuario árbol. Se exponen como elementos secundarios del contenedor de texto para que se pueda acceder a ellos a través del mismo modelo de objetos que otros controles de Automatización de la interfaz de usuario.

En la tabla siguiente se enumeran ejemplos de elementos contenedor y que no son de contenedor.

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

- Vínculo
- Casillas
- Botón

  :::column-end:::
:::row-end:::

En la imagen siguiente se muestra un contenedor de texto (documento) con una tabla e imagen incrustadas.

![ilustración que muestra un documento con una tabla e imagen incrustadas](images/embeddedtable.jpg)

La Automatización de la interfaz de usuario de contenido del documento anterior se muestra en el diagrama siguiente.

![diagrama de la vista de contenido de automatización de la interfaz de usuario de un documento con objetos incrustados](images/contenttree.jpg)

### <a name="compatible-and-non-compatible-embedded-objects"></a>Objetos incrustados "Compatible" y "No compatible"

Algunos Automatización de la interfaz de usuario usan el mismo almacén de texto para cada objeto TextPattern que contienen.  Los objetos con el respaldo del mismo almacén de texto que su contenedor se conocen como objetos incrustados "compatibles". Estos objetos pueden ser objetos TextPattern y, en este caso, sus intervalos de texto son comparables a los intervalos de texto obtenidos de su contenedor. Esto permite a los proveedores exponer información de cliente sobre los objetos TextPattern individuales como si fueran un proveedor de texto grande.

Sin embargo, los proveedores pueden usar diferentes almacenes de texto para diferentes objetos TextPattern insertados en un contenedor TextPattern. Los objetos no con el respaldo del almacén de texto del contenedor se conocen como objetos incrustados "no compatibles". Estos tipos de objetos incrustados pueden o no ser objetos basados en TextPattern.  

En la tabla siguiente se enumeran algunos ejemplos de objetos incrustados compatibles y no compatibles.

| Objetos  | Objetos incrustados compatibles | Objetos incrustados no compatibles |
| --- | --- | --- |
| Objetos incrustados que no son TextPattern | Botón en Microsoft Edge<br>Tabla de datos en Microsoft Edge | Botón de RichTextBlock en el marco XAML de Microsoft<br>Imágenes con texto alternativo en Microsoft Edge<br>ListView con ListItems en RichTextBlock en el marco XAML de Microsoft |
| Objetos incrustados TextPattern | Control de entrada de tipo "text" en Microsoft Edge<br>Tabla en un documento de Word | Elemento TextBox de un documento de Microsoft Word |

## <a name="exposing-embedded-objects"></a>Exponer objetos incrustados

Los patrones de control [Text y TextRange](uiauto-implementingtextandtextrange.md) exponen propiedades y métodos que facilitan la navegación y la consulta de objetos incrustados.

El contenido textual (o texto interno) de un contenedor de texto y un objeto incrustado, como un hipervínculo o una celda de tabla, se expone como una única secuencia de texto continua en la vista de control y la vista de contenido del árbol de Automatización de la interfaz de usuario; Se omiten los límites de objeto. Si un cliente de Automatización de la interfaz de usuario está recuperando el texto que se va a reenlazar, interpretar o analizar de alguna manera, se debe comprobar el intervalo de texto en busca de casos especiales, como una tabla con contenido textual u otros objetos incrustados. Llame a [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) para obtener una interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para cada objeto incrustado y, a continuación, llame a [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) para obtener un intervalo de texto para cada elemento. Esto se realiza recursivamente hasta que se recupera todo el contenido textual.

> [!NOTE]
> Un intervalo degenerado (o contraído) es donde el punto de conexión inicial y el extremo final son iguales. Los intervalos degenerados se usan a menudo para indicar la posición del cursor de texto a través de los métodos [GetSelection](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-getselection) y [GetCaretRange](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange) de [ITextProvider.](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider)

En el diagrama siguiente se muestra una secuencia de texto con objetos incrustados y sus intervalos de intervalo.

![diagrama que muestra una secuencia de texto con objetos incrustados y sus intervalos](images/rangespans.jpg)

## <a name="embedded-objects-and-textunit"></a>Objetos incrustados y TextUnit

Un [objeto ITextProvider](/windows/win32/api/uiautomationcore/nn-uiautomationcore-itextprovider) se puede atravesar y por un [objeto TextUnit especificado.](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit) Los proveedores que contienen objetos incrustados se pueden recorrer de la misma manera, pero los objetos incrustados afectan al recorrido. Estos son algunos aspectos que debe tener en cuenta:

- Cualquier objeto incrustado no compatible se representa mediante el carácter de reemplazo U+FFFC en el almacén de texto del elemento de contenedor TextPattern. También se considera una unidad de caracteres y una unidad de palabras.
- Los objetos incrustados compatibles pueden constar de varios caracteres y palabras.
- El elemento que contiene es el elemento de la parte inferior que abarca todo el intervalo de texto.
- Los elementos secundarios de un intervalo también son elementos secundarios de un elemento contenedor que se incluye parcial o completamente dentro del intervalo.
- Idealmente (especialmente en el caso de elementos de contenedor como Table), un límite de palabras no va más allá del límite del objeto. En el ejemplo siguiente, la unidad de palabras "Bar" no contiene ninguna posición de texto que esté fuera de la etiqueta ( no forma parte de `</td>` `<br \>` la palabra "Bar").

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

- En general, `<br \>` se trata como una palabra individual de forma que no va más allá de un límite de línea.
- Una excepción a la regla anterior es que una unidad de texto de Word contiene objetos completos dentro de sí misma. Por ejemplo, , que incluye contenedores en `<p>Hello <a href="#">link</a> here.</p>` línea, tiene las palabras "Hello", "link" y "here". Donde "link" tiene un objeto TextPattern como elemento de entrada y un objeto de vínculo como elemento secundario.
- En el caso de las unidades de caracteres, el objeto es el elemento que contiene (las unidades de texto como esta no deben tener elementos secundarios).
- Los objetos annotation no deben representarse como objetos incrustados. Por ejemplo, la presencia de otros especificadores Author en un documento coautor.
- Los objetos incrustados toman al menos una posición de cursor; la anotación son solo metadatos.
- Cada límite de objeto (inicio y fin) se representa mediante un salto de formato en el intervalo de documentos TextPattern.
- Para HTML, cada etiqueta HTML no tiene por qué dar lugar a un Automatización de la interfaz de usuario objeto . Por ejemplo, el contenido de las etiquetas de énfasis no se debe representar como elemento, sino como una secuencia de texto donde <em></em> UIA_IsItalicAttributeId devuelve TRUE.
- El punto de conexión de inicio es inclusivo y es el punto de conexión preferido, mientras que el punto de conexión final es exclusivo. Esto resulta útil cuando el intervalo está degenerado y los puntos de conexión De inicio y Fin pertenecen a la misma posición para ese intervalo.

## <a name="comparing-embedded-objects"></a>Comparación de objetos incrustados

Los objetos TextPattern anidados que están en una relación secundaria similar y comparten el mismo almacén de texto de respaldo se denominan comparables. En este caso, los intervalos de cualquiera de los objetos TextPattern se pueden comparar mediante [ITextRangeProvider::Compare](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compare) e [ITextRangeProvider::CompareEndpoints](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-compareendpoints). Ambos tienen como resultado un valor numérico válido que especifica su posición relativa.

Un objeto que no es TextPattern insertado en un objeto TextPattern es comparable a TextPattern si el objeto tiene un intervalo válido en TextPattern ([ITextProvider::RangeFromChild](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextprovider-rangefromchild)) y el contenido subyacente del intervalo de texto no está vacío y no es un carácter de reemplazo.

## <a name="embedded-textpattern-objects-and-the-document-textunit"></a>Objetos TextPattern incrustados y Document TextUnit

En el caso de los objetos TextPattern incrustados, la [unidad Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) solo reconoce el contenido contenido dentro de ese elemento.

### <a name="word-textpattern-element-hierarchy"></a>Jerarquía de elementos TextPattern de Word

- El elemento de documento implementa TextPattern y [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) devuelve todo el intervalo de documentos de Word.
- Las páginas individuales del documento implementan TextPattern y [Document](/windows/win32/api/uiautomationcore/ne-uiautomationcore-textunit) devuelve el contenido de esas páginas individuales (aunque las páginas compartan el mismo almacén de texto con todo el documento TextPattern).

### <a name="webpage-and-text-input-controls-in-edge"></a>Controles de entrada de texto y página web en Edge

- El elemento Pane de la página web principal implementa TextPattern y expone todo el contenido de la página web.
- Los controles de entrada de texto individuales admiten TextPattern, donde un intervalo de documentos representa el texto contenido en cada campo de entrada (aunque compartan el mismo almacén de texto con toda la página web).

## <a name="common-scenarios"></a>Escenarios comunes

En esta sección se presentan ejemplos de escenarios comunes que implican objetos incrustados: hipervínculos, imágenes y tablas. En los ejemplos siguientes, la llave izquierda ({) representa el punto de conexión De inicio del intervalo de texto y la llave derecha (}) representa el extremo Final.

### <a name="hyperlink-example-1-a-text-range-that-contains-an-embedded-text-hyperlink"></a>Ejemplo 1 de HyperLink: intervalo de texto que contiene un hipervínculo de texto incrustado

El siguiente intervalo de texto contiene un hipervínculo de texto incrustado.

  {La dirección URL https://www.microsoft.com está incrustada en texto}.

Llamar a los métodos [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                     | Resultado                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                  | Devuelve la cadena "La dirección URL https://www.microsoft.com está incrustada en texto".                                                                               |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                          | Devuelve el elemento Automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento de automatización que representa el propio proveedor de texto. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                          | Devuelve un Automatización de la interfaz de usuario que representa el control de hipervínculo.                                                                                      |
| [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild), donde el método [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) anterior devolvió el elemento Automatización de la interfaz de usuario. | Devuelve el intervalo que representa " https://www.microsoft.com ".                                                                                            |
### <a name="hyperlink-example-2-a-text-range-that-partially-spans-an-embedded-text-hyperlink"></a>Ejemplo 2 de HyperLink: intervalo de texto que abarca parcialmente un hipervínculo de texto incrustado

El siguiente intervalo de texto abarca parcialmente un hipervínculo de texto incrustado.

  La dirección URL https://{www} está incrustada en texto.

Llamar a [**los métodos IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                            | Resultado                                                                                                         |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Devuelve la cadena "www".                                                                                      |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Devuelve el elemento Automatización de la interfaz de usuario más interno que incluye el intervalo de texto; en este caso, el control de hipervínculo. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                 | Devuelve **NULL** porque el intervalo de texto no abarca toda la cadena de dirección URL.                                   |

### <a name="hyperlink-example-3-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Ejemplo 3 de HyperLink: intervalo de texto que abarca parcialmente el contenido de un contenedor de texto

El siguiente intervalo de texto abarca parcialmente el contenido de un contenedor de texto. El contenedor de texto incluye un hipervínculo de texto incrustado que no forma parte del intervalo de texto.

  {La dirección URL} https://www.microsoft.com se incrusta en texto.

Llamar a [**los métodos IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                            | Resultado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                         | Devuelve la cadena "La dirección URL".                                                                                                                                                                                                     |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) | Devuelve el elemento Automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa el propio proveedor de texto.                                                                                     |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)                               | Mueve el intervalo de intervalo de texto a "https://" porque el texto del hipervínculo está hecho de palabras individuales. En este caso, el hipervínculo no se considera un único objeto.<br/> La dirección URL {http} está incrustada en el texto.<br/> |

### <a name="image-example-1-a-text-range-that-contains-an-embedded-image"></a>Ejemplo de imagen 1: intervalo de texto que contiene una imagen incrustada

El siguiente intervalo de texto contiene una imagen incrustada de un objeto .

 {La imagen ![ilustración de una lonía](images/shuttle.jpg) se incrusta en text}.

Llamar a los métodos [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement), [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                    | Resultado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                                                                                                                                                                 | Devuelve la cadena "La imagen está incrustada en texto". Cualquier texto ALT asociado a la imagen no se incluye en la secuencia de texto.                |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)                                                                                                                                                         | Devuelve el elemento Automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa el propio proveedor de texto. |
| [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren)                                                                                                                                                                         | Devuelve un Automatización de la interfaz de usuario que representa el control de imagen.                                                                               |
| [**IUIAutomationTextPattern::RangeFromChild,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) donde el método [**IUIAutomationTextRange::GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) Automatización de la interfaz de usuario devolvió el elemento Automatización de la interfaz de usuario anterior. | Devuelve el intervalo degenerado.                                                                                                                 |

### <a name="image-example-2-a-text-range-that-partially-spans-the-content-of-a-text-container"></a>Ejemplo de imagen 2: intervalo de texto que abarca parcialmente el contenido de un contenedor de texto

El siguiente intervalo de texto abarca parcialmente el contenido de un contenedor de texto. El contenedor de texto incluye una imagen incrustada que no forma parte del intervalo de texto.

 {La imagen} ![ilustración de una lonía](images/shuttle.jpg) se incrusta en texto.

Llamar a [**los métodos IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext), [**GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)y [**Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                          | Resultado                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext)                                       | Devuelve la cadena "La imagen".                                                                                                                                                                                                                                                 |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement)               | Devuelve el elemento Automatización de la interfaz de usuario más interno que incluye el intervalo de texto, en este caso, el elemento que representa el propio proveedor de texto.                                                                                                                                   |
| [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) con parámetros de (**TextUnit \_ Word**, 2). | Mueve el intervalo de texto a "está". Dado que solo los objetos incrustados basados en texto se consideran parte de la secuencia de texto, la imagen de este ejemplo no afecta a [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) ni a su valor devuelto, en este caso, 2. |

### <a name="table"></a>Tabla

### <a name="table-example-1-gets-the-text-container-from-the-content-of-a-cell"></a>Ejemplo de tabla 1: obtiene el contenedor de texto del contenido de una celda

En la tabla siguiente se obtiene el contenedor de texto del contenido de una celda.

| Celda con imagen                                            | Celda con texto |
|------------------------------------------------------------|----------------|
| ![ilustración de una lonía](images/shuttle.jpg)           | X              |
| ![ilustración del espacio y un ándes](images/space.jpg) | esté              |
| ![ilustración de un ándes](images/microscope.jpg)     | Z              |

Llamar a los métodos [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem), [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)e [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) da como resultado los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                       | Resultado                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parámetros (0, 0).                                                                                                                        | Devuelve el Automatización de la interfaz de usuario que representa el contenido de la celda de tabla; en este caso, el elemento es un control de texto.                                                               |
| [**iuiautomationtextpattern::rangefromchild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild)                                                                                                                                  | devuelve el intervalo de la imagen ![ilustración de una lonía](images/shuttle.jpg).                                                                                                            |
| [**GetEnclosingElement para**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) el objeto devuelto por el método [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) anterior. | Devuelve el Automatización de la interfaz de usuario que representa la celda de tabla. En este caso, el elemento es un control de texto que admite el patrón de control [TableItem.](uiauto-implementingtableitem.md) |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para el objeto devuelto por el método **GetEnclosingElement** anterior.                                                    | Devuelve el Automatización de la interfaz de usuario que representa la tabla.                                                                                                                                   |
| [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para el objeto devuelto por el método **GetEnclosingElement** anterior.                                                    | Devuelve el Automatización de la interfaz de usuario que representa el propio proveedor de texto.                                                                                                                 |

### <a name="table-example-2-gets-the-text-content-of-a-cell"></a>Ejemplo de tabla 2: obtiene el contenido de texto de una celda

La tabla del ejemplo anterior obtiene el contenido de texto de una celda.

Llamar a [**los métodos IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) e [**IUIAutomationTextPattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) produce los comportamientos descritos en la tabla siguiente.

| Método al que se llama                                                                                                                                                                                                                                                          | Resultado                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) con parámetros (1,1).                                                                                                                                                            | Devuelve el Automatización de la interfaz de usuario que representa el contenido de la celda de tabla. En este caso, el elemento es un control de texto. |
| [**IUIAutomationTextPattern::RangeFromChild,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) donde el elemento Automatización de la interfaz de usuario es el objeto devuelto por el método [**IUIAutomationGridPattern::GetItem**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationgridpattern-getitem) anterior. | Devuelve "Y".                                                                                                               |

Al desplazarse por un documento por [**línea TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit), si el intervalo de texto entra en una tabla incrustada, cada línea de texto de una celda debe tratarse como una línea.

## <a name="related-topics"></a>Temas relacionados

### <a name="conceptual"></a>Conceptual

- [Acerca de los patrones de control Text y TextRange](uiauto-about-text-and-textrange-patterns.md)
- [Automatización de la interfaz de usuario de texto](uiauto-textattributes.md)
- [Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
- [Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
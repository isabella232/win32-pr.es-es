---
title: Usar intervalos de texto
description: En este tema se describe cómo usar las propiedades y métodos de la interfaz IUIAutomationTextRange para tener acceso al contenido textual de un control basado en texto y manipularlo.
ms.assetid: 66BC7324-5322-4996-AF62-766936559F0E
keywords:
- clients,using text range objects
- controles basados en texto
- clients,text ranges
- clients,Patrón de control TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c409f39d437135854463e83c361a9afd22204758c360119bd0033e4fd11416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564004"
---
# <a name="using-text-ranges"></a>Usar intervalos de texto

En este tema se describe cómo usar las propiedades y métodos de la interfaz [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) para tener acceso al contenido textual de un control basado en texto y manipularlo. Contiene las secciones siguientes:

-   [¿Qué es un intervalo de texto?](#using-text-ranges)
-   [Adquisición de objetos de intervalo de texto](#acquiring-text-range-objects)
-   [Selección de texto en un intervalo de texto](#selecting-text-in-a-text-range)
-   [Recuperar texto de un intervalo de texto](#retrieving-text-from-a-text-range)
-   [Recuperar atributos de texto de un intervalo de texto](#retrieving-text-attributes-from-a-text-range)
-   [Recuperar objetos incrustados de un intervalo de texto](#retrieving-embedded-objects-from-a-text-range)
-   [Manipular un intervalo de texto](#manipulating-a-text-range)
-   [Desplazamiento de un intervalo de texto a la vista](#scrolling-a-text-range-into-view)
-   [Recuperar el elemento de encier de un intervalo de texto](#retrieving-the-enclosing-element-of-a-text-range)
-   [Comparación y clonación de intervalos de texto](#comparing-and-cloning-text-ranges)
-   [Recuperar anotaciones](#retrieving-annotations)
    -   [Recuperar tipos de anotaciones de un intervalo de texto](#retrieving-annotations-types-from-a-text-range)
    -   [Recuperar todas las anotaciones de un intervalo de texto](#retrieving-all-annotations-from-a-text-range)
    -   [Recuperar información sobre una anotación determinada](#retrieving-information-about-a-particular-annotation)
    -   [Recuperar el texto de destino de anotación](#retrieving-the-annotation-target-text)
-   [Recuperar estilos visuales](#retrieving-visual-styles)
-   [Invocar menús contextuales a partir de intervalos de texto](#invoking-context-menus-from-text-ranges)
-   [Temas relacionados](#related-topics)

## <a name="what-is-a-text-range"></a>¿Qué es un intervalo de texto?

El modelo Automatización de la interfaz de usuario de objetos de texto de Microsoft se basa en el concepto del intervalo *de texto*. Un intervalo de texto es un objeto que expone la interfaz [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) y representa un intervalo contiguo de texto en un control basado en texto. Cada intervalo de texto tiene un punto de conexión inicial y un punto de conexión final, y todo el contenido textual entre los dos puntos de conexión se considera parte del intervalo. Un intervalo de texto cuyo punto de conexión inicial y extremo final se encuentran en la misma ubicación se denomina intervalo *de texto degenerado* (o vacío). Un intervalo de texto degenerado se usa para marcar una ubicación específica dentro del texto de un control, como la ubicación del punto de inserción de texto.

## <a name="acquiring-text-range-objects"></a>Adquisición de objetos de intervalo de texto

Las aplicaciones cliente adquieren objetos de intervalo de texto mediante las propiedades y métodos de la [**interfaz IUIAutomationTextPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) La propiedad [**IUIAutomationTextRangePattern::D ocumentRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_documentrange) recupera un intervalo de texto que representa todo el contenido textual de un control basado en texto, mientras que otros métodos adquieren intervalos de texto que representan parte del contenido, como el texto seleccionado, el texto visible o un objeto insertado en el texto.

Los [**métodos IUIAutomationTextRangePattern::GetVisibleRanges**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges) y [**GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) pueden recuperar matrices de objetos de intervalo de texto. Si un control está parcialmente oculto por una ventana superpuesta u otro objeto, **GetVisibleRanges** devuelve una matriz que contiene un objeto de intervalo de texto para cada línea de texto parcialmente visible. De forma similar, si un control basado en texto admite la selección de varios intervalos de texto no unidos, **GetSelection** devuelve una matriz que contiene un objeto de intervalo de texto para cada intervalo seleccionado.

El [**método IUIAutomationTextRangePattern::RangeFromChild**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-rangefromchild) permite a una aplicación cliente recuperar un intervalo de texto que incluye un objeto incrustado en el contenido textual. El cliente especifica el puntero de interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de un objeto incrustado, como una imagen, una tabla o un hipervínculo, y el método devuelve un intervalo de texto que incluye el objeto. Sin embargo, si el objeto incrustado no tiene ningún texto asociado, el método devuelve un intervalo de texto degenerado.

Una aplicación cliente puede usar el método [**IUIAutomationTextRangePattern::RangeFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefrompoint) para recuperar un intervalo de texto para el texto visible o el objeto incrustado más cercano a las coordenadas de pantalla especificadas.

## <a name="selecting-text-in-a-text-range"></a>Selección de texto en un intervalo de texto

La [**interfaz IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) incluye una serie de métodos que permiten a una aplicación cliente controlar la selección de texto en un control basado en texto.

Las aplicaciones cliente pueden usar el método [**IUIAutomationTextRange::Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-select) para seleccionar el texto que corresponde a un intervalo de texto y para quitar la selección anterior, si la hubiera, del control de texto. Al llamar a **Select** con un intervalo de texto degenerado, se mueve el punto de inserción a la ubicación del intervalo de texto sin seleccionar ningún texto.

Si un control admite la selección de varios intervalos de texto no unidos, un cliente puede usar los métodos [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) y [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) para agregar intervalos de texto y quitarlos de la colección de intervalos de texto seleccionados. Si el control solo admite un intervalo de texto seleccionado a la vez, pero la operación de selección daría lugar a la selección de varios intervalos de texto no unidos, el método devuelve un error **E \_ INVALIDOPERATION** o extiende o trunca la selección actual. Una aplicación cliente puede detectar si un control admite la selección de uno o varios intervalos de texto, o ninguno en absoluto, comprobando la propiedad [**IUIAutomationTextPattern::SupportedTextSelection.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection)

Si un control basado en texto admite inserciones de texto, llamar a [**IUIAutomationTextRange::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-addtoselection) o [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-removefromselection) en un intervalo de texto degenerado del control mueve el punto de inserción, pero no selecciona ningún texto.

## <a name="retrieving-text-from-a-text-range"></a>Recuperar texto de un intervalo de texto

Las aplicaciones cliente pueden usar [**el método IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) para recuperar el texto sin formato de un intervalo de texto. El texto sin formato incluye todos los caracteres de control que se encuentran en el texto de origen, como retornos de carro y la marca Unicode de izquierda a derecha (LRM). El texto sin formato no incluye etiquetas de marcado como HTML que puedan estar presentes en el texto de origen. Además, los códigos de escape del texto de origen se convierten en equivalentes de texto sin formato. Por ejemplo, " &nbsp; " se convierte en un carácter de espacio simple.

Si un objeto incrustado abarca un intervalo de texto, el texto sin formato incluye el texto interno del objeto, pero no el texto alternativo (la propiedad name del objeto incrustado). Para obtener más información, vea [How Automatización de la interfaz de usuario Exposes Embedded Objects](uiauto-textpattern-and-embedded-objects-overview.md).

El [**método IUIAutomationTextRange::FindText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findtext) busca una cadena determinada en un intervalo de texto y, si se encuentra, devuelve un nuevo intervalo de texto que abarca la cadena.

## <a name="retrieving-text-attributes-from-a-text-range"></a>Recuperar atributos de texto de un intervalo de texto

Los atributos de texto determinan el estilo de formato del texto en un control basado en texto e incluyen elementos como el color de primer plano, el estilo de viñeta, el tamaño de fuente, y así sucesivamente. Automatización de la interfaz de usuario admite varios atributos de texto y define un identificador para cada atributo admitido. Una aplicación cliente puede consultar un intervalo de texto para el valor de un atributo de texto determinado especificando un identificador de atributo en una llamada al método [**IUIAutomationTextRange::GetAttributeValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) junto con un puntero a una estructura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) que recibe el valor del atributo. Para obtener información detallada sobre cada atributo de texto que Automatización de la interfaz de usuario, vea [Identificadores de atributo de texto](uiauto-textattribute-ids.md).

El valor recuperado por [**GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) representa el valor del atributo en todo el intervalo de texto. Si todo el texto del intervalo comparte el mismo valor para el atributo especificado, **GetAttributeValue** devuelve ese valor. Sin embargo, si el valor del atributo varía en el intervalo de texto, **GetAttributeValue** devuelve un [**puntero IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) a un objeto de token estático denominado **reservedMixedAttribute.** Para detectar si el valor de un atributo varía en un intervalo de texto, una aplicación cliente debe comparar los resultados de **GetAttributeValue** con el objeto **ReservedMixedAttribute** recuperado de la propiedad [**IUIAutomation::ReservedMixedAttributeValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue)

No se requiere un control basado en texto para admitir todos los Automatización de la interfaz de usuario de texto. Si un cliente llama al método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) y pasa el identificador de un atributo no admitido, el método devuelve un puntero [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) a un objeto de token estático denominado el objeto **ReservedNotSupported.** Para detectar si se admite un atributo determinado, una aplicación cliente debe comparar los resultados de **GetAttributeValue** con el objeto **ReservedNotSupported** recuperado de la propiedad [**IUIAutomation::ReservedNotSupportedValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue)

Las aplicaciones cliente pueden usar el método [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para buscar texto en un intervalo de texto que tenga un atributo de texto determinado. Si se encuentra, el método devuelve un nuevo intervalo de texto que abarca el texto correspondiente. Tenga en **cuenta que FindAttribute** devuelve un intervalo de texto para el texto correspondiente, incluso si el texto no está visible.

## <a name="retrieving-embedded-objects-from-a-text-range"></a>Recuperar objetos incrustados de un intervalo de texto

Un intervalo de texto puede incluir objetos incrustados como tablas, imágenes, hipervínculos, entre otros. Una aplicación cliente puede recuperar una colección de todos los objetos incrustados de un intervalo llamando al [**método IUIAutomationTextRange::GetChildren.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) También se incluyen en la colección los objetos incrustados que se superponen con el intervalo, pero que no están incluidos por completo en él. Si el intervalo no contiene objetos incrustados, **GetChildren** recupera una colección vacía.

Aunque depende del proveedor del control basado en texto, el [**método GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) normalmente no devuelve ningún elemento primario de los elementos incrustados. Por ejemplo, si un intervalo de texto contiene una tabla que tiene varias celdas secundarias, el método **GetChildren** normalmente devuelve solo el elemento table y no los elementos de celda.

Por motivos de rendimiento o arquitectura, es posible que [**GetChildren**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getchildren) no pueda recuperar objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para todos los objetos incrustados en un intervalo de texto. En su lugar, el proveedor podría devolver una colección que incluye elementos virtualizados. Para obtener más información, [vea Trabajar con elementos virtualizados.](uiauto-workingwithvirtualizeditems.md)

## <a name="manipulating-a-text-range"></a>Manipular un intervalo de texto

La [**interfaz IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) proporciona varios métodos para manipular y navegar por intervalos de texto en un control basado en texto. Los métodos [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move), [**MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)y [**ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) mueven un intervalo de texto o uno de sus puntos de conexión por la unidad de texto especificada, como carácter, palabra, párrafo, y así sucesivamente. Para obtener más información, [vea Automatización de la interfaz de usuario unidades de texto](/windows/desktop/WinAuto/uiauto-uiautomationtextunits).

A pesar de su nombre, [**el método ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) no expande necesariamente un intervalo de texto. En su lugar, "normaliza" un intervalo de texto moviendo los puntos de conexión para que el intervalo abarque exactamente la unidad de texto especificada. El intervalo se expande si es menor que la unidad especificada o se acorta si es mayor que la unidad especificada. En el diagrama siguiente se **muestra cómo ExpandToEnclosingUnit** normaliza un intervalo de texto moviendo los puntos de conexión del intervalo.

![diagrama que muestra las posiciones del punto de conexión antes y después de una llamada a expandtoenclosingunit](images/expandtoenclosingunit.jpg)

Si el intervalo de texto comienza al principio de una unidad de texto y termina al principio o antes del siguiente límite de la unidad de texto, el punto de conexión final se mueve al siguiente límite de unidad de texto (vea 1 y 2 en la ilustración anterior).

Si el intervalo de texto comienza al principio de una unidad de texto y termina en el siguiente límite de unidad o después de este, el punto de conexión final permanece o se mueve hacia atrás hasta el siguiente límite de unidad después del punto de conexión inicial (vea 3 y 4 en la ilustración anterior). Si hay más de un límite de unidad de texto entre los puntos de conexión inicial y final, el extremo final se mueve hacia atrás hasta el siguiente límite de unidad después del punto de conexión inicial, lo que da lugar a un intervalo de texto de una unidad de texto de longitud.

Si el intervalo de texto comienza en el centro de una unidad de texto, el punto de conexión inicial se mueve hacia atrás hasta el principio de la unidad de texto y el extremo final se mueve hacia delante o hacia atrás, según sea necesario, hasta el siguiente límite de unidad después del punto de conexión inicial (vea 5 a 8 en la ilustración anterior).

Cuando se llama al método [**IUIAutomationTextRange::Move,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move) el proveedor normaliza el intervalo de texto por la unidad de texto especificada. A continuación, el proveedor mueve el intervalo hacia atrás o hacia delante según el número especificado de unidades de texto. Al mover el intervalo, el proveedor omite los límites de los objetos incrustados en el texto. (Sin embargo, el propio límite de unidad puede verse afectado por la existencia de un objeto incrustado). En el diagrama siguiente se muestra cómo el **método Move** mueve un intervalo de texto, unidad por unidad, entre objetos incrustados y límites de unidad de texto.

![diagrama que muestra cómo el método de movimiento mueve los puntos de conexión de intervalo a través de los límites de objetos y unidades de texto](images/move.jpg)

El [**método IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit) mueve uno de los puntos de conexión hacia delante o hacia atrás mediante la unidad de texto especificada. En la ilustración siguiente se muestra cómo avanza un punto de conexión.

![diagrama que muestra cómo moveendpointbyunit mueve el punto de conexión de un intervalo](images/moveendpointbyunit.gif)

El [**método IUIAutomationTextRange::MoveEndpointByRange**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyrange) permite a una aplicación cliente establecer un punto de conexión de un intervalo de texto en la misma ubicación que el punto de conexión especificado de un segundo intervalo de texto.

## <a name="scrolling-a-text-range-into-view"></a>Desplazamiento de un intervalo de texto a la vista

El [**método IUIAutomationTextRange::ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-scrollintoview) desplaza un intervalo de texto para que el texto sea visible en la ventanilla del control basado en texto. Al llamar **a ScrollIntoView**, un cliente puede especificar si el texto debe alinearse con la parte superior o inferior de la ventanilla.

## <a name="retrieving-the-enclosing-element-of-a-text-range"></a>Recuperar el elemento de encier de un intervalo de texto

Una aplicación cliente puede usar el método [**IUIAutomationTextRange::GetEnclosingElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getenclosingelement) para recuperar el puntero de interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) del elemento más interno que incluye un intervalo de texto. El elemento que lo incluye suele ser el proveedor de texto que proporciona el intervalo de texto. Sin embargo, si el proveedor de texto admite elementos secundarios como tablas o hipervínculos, el elemento que lo incluye podría ser un descendiente del proveedor de texto.

## <a name="comparing-and-cloning-text-ranges"></a>Comparación y clonación de intervalos de texto

La [**interfaz IUIAutomationTextRange incluye**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) dos métodos para comparar intervalos de texto. El [**método IUIAutomationTextRange::Compare**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-compareendpoints) compara los puntos de conexión inicial y final de dos intervalos de texto y devuelve **TRUE** si ambos extremos son iguales. El **método IUIAutomationTextRange::CompareEndpoints** compara el punto de conexión inicial o final de los dos intervalos. El valor devuelto es cero si los puntos de conexión son iguales o un valor positivo o negativo que indica las posiciones relativas de los dos puntos de conexión.

Las aplicaciones cliente pueden usar [**el método IUIAutomationTextRange::Clone**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-clone) para crear una copia exacta del intervalo de texto. El nuevo intervalo de texto se puede manipular independientemente del intervalo de texto original.

## <a name="retrieving-annotations"></a>Recuperar anotaciones

Un intervalo de texto puede incluir anotaciones si el control basado en texto las admite. Hay muchos tipos diferentes de anotaciones. El archivo de encabezado UIAutomationClient.h define un conjunto de valores constantes con nombre que identifican los tipos de anotaciones que Automatización de la interfaz de usuario admite. Para obtener más información, vea [**Identificadores de tipo de anotación**](uiauto-annotation-type-identifiers.md).

Algunos tipos de anotaciones se representan mediante un elemento de automatización que admite el patrón de control [Annotation](uiauto-implementingannotation.md) [**(interfaz IUIAutomationAnnotationPattern).**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) Otros tipos de anotaciones se exponen a través del patrón de control [TextRange.](uiauto-about-text-and-textrange-patterns.md) Por ejemplo, un proveedor podría exponer un indicador de error ortográfico simple haciendo que el método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) devuelva un atributo de texto [**AnnotationTypes**](uiauto-textattribute-ids.md) [**de AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)y un valor NULL para el atributo de texto [**AnnotationObjects.**](uiauto-textattribute-ids.md)

### <a name="retrieving-annotations-types-from-a-text-range"></a>Recuperar tipos de anotaciones de un intervalo de texto

Puede recuperar una lista de los tipos de anotaciones presentes en un intervalo de texto mediante el método [**IUIAutomationTextRange::GetAttributeValue.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) Al llamar al método , especifique un identificador de atributo de texto [**de UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md) y un puntero a un parámetro de tipo [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant). Cuando el método devuelve un resultado, el parámetro **VARIANT** contiene una lista de identificadores de tipo de anotación, uno para cada tipo de anotación del intervalo de texto. Para obtener más información, vea [**Identificadores de tipo de anotación**](uiauto-annotation-type-identifiers.md).

### <a name="retrieving-all-annotations-from-a-text-range"></a>Recuperar todas las anotaciones de un intervalo de texto

Para recuperar las anotaciones de un intervalo de texto, llame al método [**IUIAutomationTextRange::GetAttributeValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) especificando un identificador de atributo de texto de [**UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) y un puntero a un parámetro de tipo [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Cuando el método devuelve un resultado, el parámetro **VARIANT** contiene una interfaz [**IUIAutomationElementArray**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) que representa una matriz de elementos de automatización, una para cada anotación del intervalo de texto. La [**propiedad IUIAutomationElementArray::Length**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-get_length) indica el número de elementos de la matriz y el método [**IUIAutomationElementArray::GetElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelementarray-getelement) recupera la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para un elemento determinado.

### <a name="retrieving-information-about-a-particular-annotation"></a>Recuperar información sobre una anotación determinada

Para recuperar información sobre una anotación determinada, recupere primero la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para el elemento annotation tal y como se describe en la sección anterior. A continuación, recupere la interfaz [**IUIAutomationAnnotationPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationannotationpattern) para la anotación llamando al método [**IUIAutomationElement::GetCurrentPatternAs**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) con un identificador de patrón de control de [**UIA \_ AnnotationPatternId,**](uiauto-controlpattern-ids.md)un identificador de interfaz de \_ IID IUIAutomationAnnotationPattern y la dirección de una variable que recibe el puntero **IUIAutomationAnnotation** para la anotación. Consulte las propiedades de la interfaz **IUIAutomationAnnotation** para recuperar el nombre del tipo de anotación y el identificador de tipo, el nombre del autor de la anotación, la fecha y hora de la anotación y la interfaz **IUIAutomationElement** para el elemento que se está anotando.

### <a name="retrieving-the-annotation-target-text"></a>Recuperar el texto de destino de anotación

Normalmente, una anotación se aplica a algún subconjunto del texto de un intervalo de texto. Después de recuperar la [**interfaz IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para una anotación, puede pasar la interfaz al método [**IUIAutomationTextRange2::RangeFromAnnotation**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider2-rangefromannotation) para recuperar un intervalo de texto que contenga el texto que es el destino de la anotación.

## <a name="retrieving-visual-styles"></a>Recuperar estilos visuales

Un proveedor implementa el patrón de control [Estilos](/windows/desktop/WinAuto/uiauto-implementingstyles) para describir un elemento de interfaz de usuario que tiene un estilo, color de relleno, patrón de relleno o forma específicos. Esto es especialmente útil al describir elementos de un documento, que con frecuencia tienen estos estilos. Estilos como este suelen llevar información útil para los clientes con discapacidades. Por ejemplo, los estilos pueden describir una cadena determinada como el título de un documento o un objeto de diagrama de flujo determinado como un rombo o un círculo.

Puede usar el método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar los nombres e identificadores de los estilos visuales que se usan en un intervalo de texto. Use el [**atributo de texto UIA \_ StyleNameAttributeId**](uiauto-textattribute-ids.md) para recuperar los nombres de estilo y [**UIA \_ StyleIdAttributeId para**](uiauto-textattribute-ids.md) recuperar los identificadores de estilo.

Un control basado en texto que admite estilos visuales puede implementar el patrón de control [Estilos](/windows/desktop/WinAuto/uiauto-implementingstyles) para permitir que los clientes accedan a información sobre un estilo visual utilizado por el control . Los clientes acceden al patrón de control Styles a través de [**la interfaz IUIAutomationStylesPattern.**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) Puede recuperar esta interfaz llamando al método [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) o [**GetCurrentPatternAs,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas) especificando [**UIA \_ StylesPatternId**](uiauto-controlpattern-ids.md) como identificador del patrón de control.

La [**interfaz IUIAutomationStylesPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationstylespattern) incluye propiedades y métodos que proporcionan la siguiente información sobre un estilo visual:

-   Nombre del estilo visual, como "Normal" o "Encabezado 1".
-   Identificador del estilo visual. Para obtener más información, vea [**Identificadores de estilo**](uiauto-style-identifiers.md).
-   Color utilizado para rellenar el control basado en texto.
-   Color del patrón utilizado para rellenar el control basado en texto.
-   Forma del control basado en texto.
-   Propiedades extendidas; es decir, una lista de valores y nombres de estilo específicos del control.

## <a name="invoking-context-menus-from-text-ranges"></a>Invocar menús contextuales desde intervalos de texto

A partir Windows 8.1, los intervalos de texto pueden admitir la [**interfaz IUIAutomationTextRange2.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange2) Esta interfaz admite el [**método ShowContextMenu.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange2-showcontextmenu) Puede llamar a este método para invocar cualquier menú contextual asociado a un intervalo de texto. El escenario para esto es la autocorrección de intervalos de texto o la selección de candidatos de IME. En estos casos, aparece un menú contextual que admite la interacción del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Patrones de control Text y TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 
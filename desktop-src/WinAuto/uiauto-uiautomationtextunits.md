---
title: Unidades de texto de Automatización de la interfaz de usuario
description: En este tema se describen las unidades de texto admitidas por la automatización de la interfaz de usuario de Microsoft \ 32; Patrón de control TextRange. Los proveedores y clientes de automatización de la interfaz de usuario usan unidades de texto para especificar la cantidad por la que se mueve o cambia el tamaño de un intervalo de texto.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Automatización de la interfaz de usuario, unidades de texto
- unidades de texto, acerca de
- Automatización de la interfaz de usuario, lista de unidades de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff4257c70b34cea01a149b30dff2bf2fbe691a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359018"
---
# <a name="ui-automation-text-units"></a>Unidades de texto de automatización de la interfaz de usuario

En este tema se describen las unidades de texto admitidas por el patrón de control [TextRange](uiauto-implementingtextandtextrange.md) de automatización de la interfaz de usuario de Microsoft. Los proveedores y clientes de automatización de la interfaz de usuario usan unidades de texto para especificar la cantidad por la que se mueve o cambia el tamaño de un intervalo de texto.

-   [Elementos de la API de unidad de texto](#text-unit-api-elements)
-   [Descripciones de unidad de texto](#text-unit-descriptions)
    -   [Carácter](#character)
    -   [Format](#format)
    -   [Word](#word)
    -   [Line](#line)
    -   [Paragraph](#paragraph)
    -   [Page](#page)
    -   [Documento](#document)
-   [Otros intervalos posibles](#other-potential-ranges)
-   [Temas relacionados](#related-topics)

## <a name="text-unit-api-elements"></a>Elementos de la API de unidad de texto

La API de automatización de la interfaz de usuario incluye los siguientes métodos que requieren que se especifique una unidad de texto:

-   [**ITextRangeProvider:: Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange:: Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

La enumeración [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) define las unidades de texto admitidas por los intervalos de texto de automatización de la interfaz de usuario. Para especificar la unidad de texto, se especifica un miembro de la enumeración [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) en una llamada a un método [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) o [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) . Las unidades de texto, de menor a mayor, son las siguientes:

-   [**\_Carácter TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Formato TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Palabra TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Línea TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Párrafo TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Página TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**\_Documento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Si un control basado en texto determinado no admite la unidad de texto especificada, el proveedor debe responder sustituyendo la unidad de texto más grande que sea compatible con el control. Por ejemplo, si [**se \_ especifica TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , pero no se admite, el método puede sustituir la [**\_ Página TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) o el [**\_ documento TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Las características lingüísticas del texto de origen pueden dificultar a un proveedor la determinación de los límites de texto en función de la unidad de texto especificada. Para obtener ayuda a la hora de determinar los límites de texto, un proveedor puede usar las funciones de la API de Uniscribe, como [**ScriptBreak**](/windows/desktop/api/usp10/nf-usp10-scriptbreak). Para obtener más información, [vea el sitio web de MSDN](/windows/desktop/Intl/uniscribe) .

## <a name="endpoint-inclusivity"></a>Punto de conexión inclusivity

Un punto de conexión de unidad de texto puede actuar como punto de conexión de [Inicio](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) y como extremo [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de los intervalos de texto adyacentes del mismo tipo. Si el final de una unidad de texto es también el inicio de otra unidad de texto, el rango que contiene el extremo [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) no comparte ningún atributo u objeto del intervalo adyacente que contenga el punto de conexión de [Inicio](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) .

Por ejemplo, una secuencia de texto, "Hello **World**", contiene dos unidades de palabra con distintos atributos de espesor de fuente (normal y negrita). En este caso, el extremo [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la palabra unidad "Hello" y el punto de conexión de [Inicio](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la palabra unidad "**World**" son los mismos, lo que da como resultado lo siguiente:

- El intervalo de "Hello" no comparte el atributo Bold de la palabra unidad "World" y no devuelve el valor del atributo Mixed para el atributo de texto de espesor de fuente.
- El intervalo de "**World**" tiene un espesor de fuente único (bold) y no comparte el espesor de fuente de la palabra "Hello" anterior.

Este es otro ejemplo en el que una secuencia de texto contiene dos unidades de palabra, una de las cuales es un vínculo: `[Foo]() Bar` . En este caso, el extremo [final](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la palabra Unit `[Foo]()` y el punto de conexión de [Inicio](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la palabra "bar" son los mismos, lo que da como resultado lo siguiente:

- El vínculo pertenece al intervalo de texto que contiene "foo".
- El vínculo es un elemento secundario del intervalo de texto "foo" y está incluido en [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- El intervalo de texto "bar" no tiene elementos secundarios y y está incluido en [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Notas adicionales:**

> Un intervalo degenerado (vacío) en un límite de unidad de texto con un intervalo de texto del mismo tipo presupone las propiedades de la unidad de texto adyacente inmediatamente.
>
> La llamada a [IUIAutomationTextRange:: ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) en un intervalo degenerado en un límite de unidad de texto con un intervalo de texto del mismo tipo, expande el intervalo degenerado en la unidad de texto siguiente.

## <a name="text-unit-descriptions"></a>Descripciones de unidad de texto

En esta sección se describe cada una de las unidades de texto admitidas por la automatización de la interfaz de usuario.

### <a name="character"></a>Carácter

[**TextUnit \_ Carácter**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa un solo carácter. La definición lingüística de un carácter varía según el idioma. En el caso de Inglés de EE. UU., un carácter normalmente se rodea por un espacio u otro carácter, como un signo de puntuación, un número o una letra.

Los caracteres de control, como los retornos de carro y la marca de izquierda a derecha (LTM) de Unicode no deben considerarse como caracteres, pero pueden incluirse en un intervalo de texto normalizado en función de la unidad de texto de caracteres.

Los signos de puntuación y los caracteres de separación de palabras, como los espacios, se deben considerar como caracteres.

### <a name="format"></a>Formato

[**TextUnit \_ Format**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) se usa para colocar el límite de un intervalo de texto en función de los atributos de formato del texto. Por ejemplo, si un intervalo de texto está actualmente situado en un solo carácter de una palabra, si se especifica el **\_ formato TextUnit** en una llamada a [**IUIAutomationTextRange:: ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) , el intervalo de texto se expande para incluir todo el texto que comparte los mismos atributos que el único carácter. El intervalo de texto resultante puede incluir o no la palabra completa. Además, el uso de la unidad de texto de formato no expandirá un intervalo de texto en el límite de un objeto incrustado, como una imagen o un hipervínculo.

A diferencia de las otras unidades de texto, que incluyen las unidades de texto más pequeñas que las mismas, el [**\_ formato de TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) puede ser menor o mayor que el resto de unidades. Por ejemplo, si un documento completo comparte los mismos atributos de texto y no contiene objetos incrustados, la expansión de un intervalo de texto con el **\_ formato TextUnit** crearía un nuevo intervalo que abarque todo el documento, mientras que al expandir el intervalo de texto [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) crearía un intervalo más pequeño.

### <a name="word"></a>Word

[**TextUnit \_ Palabra**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa una sola palabra completa. La definición lingüística de una palabra varía según el idioma. En Inglés de EE. UU., las palabras suelen estar rodeadas por espacios o caracteres de puntuación.

Cuando se utiliza [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) para establecer el límite de un intervalo de texto, el intervalo de texto resultante debe incluir cualquier carácter de separación de palabras que esté presente al final de la palabra, pero antes del inicio de la palabra siguiente.

### <a name="line"></a>Línea

[**TextUnit \_ La línea**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad de texto que representa una sola línea de texto, tal como se muestra en la ventanilla del control. Cuando se usa la **\_ línea TextUnit** para establecer el límite de un intervalo de texto, un proveedor debe establecer el límite inmediatamente después del punto en el que un carácter de control interrumpe la línea o donde la ventanilla del control ajusta el texto a una nueva línea. El límite debe establecerse cuando se inicia una nueva línea.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ El párrafo**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa un párrafo completo. Un párrafo debe comenzar justo antes del primer carácter de un párrafo y normalmente debe finalizar justo después del último carácter. Las líneas vacías que siguen a un párrafo se deben combinar en el párrafo, a menos que algo en el origen de texto indique lo contrario. Normalmente, el límite final de un párrafo también marca el límite final de una unidad de texto de [**\_ línea de TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) .

### <a name="page"></a>Página

[**TextUnit \_ La página**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa una página de texto completa de un documento. Los límites de una página se deben establecer en los puntos inmediatos en los que se inicia y finaliza una página.

### <a name="document"></a>Documento

[**TextUnit \_ El documento**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa todo el contenido de un documento tal como lo admite el patrón de control [Text](uiauto-implementingtextandtextrange.md) . No debe existir texto fuera de un intervalo de texto que contenga un documento. Los objetos que se insertan en un documento, como las notas de anotación que cruzan un límite de página, deben tratarse como objetos incrustados del documento y no como parte del contenido de texto del documento.

## <a name="other-potential-ranges"></a>Otros intervalos posibles

La especificación del patrón de control [TextRange](uiauto-implementingtextandtextrange.md) actual no permite que se agreguen nuevos valores de unidad de texto a la enumeración [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) , ni permite que se redefinan los valores de unidad de texto existentes. Para exponer otros intervalos posibles, como los encabezados y las anotaciones, un proveedor debe exponer estos intervalos como objetos incrustados con un intervalo de texto asociado. De este modo, también puede Agregar compatibilidad con los patrones de control adecuados. Esta solución es más flexible y extensible que definir nuevas unidades de texto.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider:: GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Conceptual

[Compatibilidad de UI Automation para el contenido textual](uiauto-ui-automation-textpattern-overview.md)

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
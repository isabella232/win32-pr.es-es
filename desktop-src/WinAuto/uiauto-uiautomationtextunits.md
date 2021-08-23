---
title: Unidades de texto de Automatización de la interfaz de usuario
description: En este tema se describen las unidades de texto admitidas por Microsoft Automatización de la interfaz de usuario \ 32; Patrón de control TextRange. Automatización de la interfaz de usuario proveedores y clientes usan unidades de texto para especificar la cantidad por la que se va a mover o cambiar el tamaño de un intervalo de texto.
ms.assetid: 3ec43a81-c4f1-4c73-865f-a60c751fc3fb
keywords:
- Automatización de la interfaz de usuario,unidades de texto
- unidades de texto, acerca de
- Automatización de la interfaz de usuario,lista de unidades de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c40604f3c524c1e9f3bcdb36458e099563eb7279fa61133dcfa7ea3fde90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118824168"
---
# <a name="ui-automation-text-units"></a>Automatización de la interfaz de usuario unidades de texto

En este tema se describen las unidades de texto admitidas por el patrón de control Automatización de la interfaz de usuario [TextRange](uiauto-implementingtextandtextrange.md) de Microsoft. Automatización de la interfaz de usuario proveedores y clientes usan unidades de texto para especificar la cantidad por la que se va a mover o cambiar el tamaño de un intervalo de texto.

-   [Elementos de text unit API](#text-unit-api-elements)
-   [Descripciones de unidades de texto](#text-unit-descriptions)
    -   [Carácter](#character)
    -   [Format](#format)
    -   [Word](#word)
    -   [Línea](#line)
    -   [Paragraph](#paragraph)
    -   [Page](#page)
    -   [Documento](#document)
-   [Otros intervalos potenciales](#other-potential-ranges)
-   [Temas relacionados](#related-topics)

## <a name="text-unit-api-elements"></a>Elementos de la API de unidad de texto

La API Automatización de la interfaz de usuario incluye los métodos siguientes que requieren que se especifique una unidad de texto:

-   [**ITextRangeProvider::Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-move)
-   [**ITextRangeProvider::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-expandtoenclosingunit)
-   [**ITextRangeProvider::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-moveendpointbyunit)
-   [**IUIAutomationTextRange::Move**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-move)
-   [**IUIAutomationTextRange::ExpandToEnclosingUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit)
-   [**IUIAutomationTextRange::MoveEndpointByUnit**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-moveendpointbyunit)

La [**enumeración TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) define las unidades de texto admitidas por Automatización de la interfaz de usuario de texto. Para especificar la unidad de texto, se especifica un miembro de la enumeración [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) en una llamada a un método [**ITextRangeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextrangeprovider) o [**IUIAutomationTextRange.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) Las unidades de texto, de menor a mayor, son las siguientes:

-   [**Carácter \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Formato \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Línea \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Párrafo de \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Página \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)
-   [**Documento de \_ TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

Si un control basado en texto determinado no admite la unidad de texto especificada, el proveedor debe responder sustituyendo la siguiente unidad de texto más grande admitida por el control . Por ejemplo, si [**se especifica TextUnit \_ Paragraph**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) pero no se admite, el método puede sustituir [**TextUnit \_ Page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) o [**TextUnit \_ Document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit).

Las características lingüísticas del texto de origen pueden dificultar que un proveedor determine los límites de texto en función de la unidad de texto especificada. Para obtener ayuda para determinar los límites de texto, un proveedor puede usar funciones de API de Uniscribe como [**ScriptBreak.**](/windows/desktop/api/usp10/nf-usp10-scriptbreak) Para obtener más información, [vea Uniscribe en](/windows/desktop/Intl/uniscribe) el sitio web de MSDN.

## <a name="endpoint-inclusivity"></a>Inclusividad del punto de conexión

Un punto de conexión de unidad de [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) texto puede actuar como punto de conexión [de](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) inicio y extremo para intervalos de texto adyacentes del mismo tipo. Si el final de una unidad de texto también es el [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) inicio de otra unidad de texto, el intervalo que contiene el punto de conexión End no comparte ningún atributo u objeto del intervalo adyacente que contiene el punto de conexión [De](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) inicio.

Por ejemplo, una secuencia de texto, **"Hola** mundo", contiene dos unidades de palabras con atributos de peso de fuente diferentes (normal y negrita). En este caso, el punto de conexión End de la unidad de palabras "Hello" y el punto de conexión [Start](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) de la palabra unidad "**world**" son los mismos, lo que da como resultado lo siguiente: [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

- El intervalo de "Hello" no comparte el atributo bold de la palabra unidad "world" y no devuelve el valor de atributo mixto para el atributo de texto de peso de fuente.
- El intervalo de "**world**" tiene un único grosor de fuente (negrita) y no comparte el grosor de la fuente de la unidad de palabras anterior "Hello".

Este es otro ejemplo en el que una secuencia de texto contiene dos unidades de palabras, una de las cuales es un vínculo: `[Foo]() Bar` . En este caso, el punto [de](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint) conexión End de la palabra unit y el punto de conexión Start de la unidad de palabras "Bar" son los mismos, lo que da como resultado `[Foo]()` lo siguiente: [](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

- El vínculo pertenece al intervalo de texto que contiene "Foo".
- El vínculo es un elemento secundario del intervalo de texto "Foo" y está incluido en [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).
- El intervalo de texto "Bar" no tiene ningún elemento secundarios y está incluido en [ITextProvider](https://review.docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).

**Notas adicionales:**

> Un intervalo degenerado (vacío) en un límite de unidad de texto con un intervalo de texto del mismo tipo asume las propiedades de la unidad de texto adyacente inmediatamente.
>
> Al llamar a [IUIAutomationTextRange::ExpandToEnclosingUnit](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit
) en un intervalo degenerado en un límite de unidad de texto con un intervalo de texto del mismo tipo, se expande el intervalo degenerado a la siguiente unidad de texto.

## <a name="text-unit-descriptions"></a>Descripciones de unidades de texto

En esta sección se describe cada una de las unidades de texto admitidas por Automatización de la interfaz de usuario.

### <a name="character"></a>Carácter

[**TextUnit \_ Character**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa un único carácter. La definición lingüística de un carácter varía según el idioma. En inglés de Estados Unidos, un carácter suele estar bordeado por un espacio u otro carácter, como una marca de puntuación, un número o una letra.

Los caracteres de control como retornos de carro y la marca Unicode de izquierda a derecha (LTM) no deben considerarse caracteres, pero pueden incluirse en un intervalo de texto que se normaliza en función de la unidad de texto de caracteres.

Los signos de puntuación y los caracteres de salto de palabras, como los espacios, deben considerarse caracteres.

### <a name="format"></a>Formato

[**TextUnit \_ El**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) formato se usa para colocar el límite de un intervalo de texto en función de los atributos de formato del texto. Por ejemplo, si un intervalo de texto está situado actualmente en un único carácter de una palabra, al especificar **TextUnit \_ Format** en una llamada a [**IUIAutomationTextRange::ExpandToEnclosingUnit,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-expandtoenclosingunit) se expande el intervalo de texto para incluir todo el texto que comparte todos los mismos atributos que el carácter único. El intervalo de texto resultante podría incluir o no toda la palabra. Además, el uso de la unidad de texto de formato no expandirá un intervalo de texto a través del límite de un objeto incrustado, como una imagen o un hipervínculo.

A diferencia de las otras unidades de texto, que incluyen las unidades de texto que son más pequeñas que ellas mismas, el formato [**TextUnit \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) puede ser menor o mayor que las otras unidades. Por ejemplo, si un documento completo comparte los mismos atributos de texto y no contiene objetos incrustados, expandir un intervalo de texto por **TextUnit \_ Format** crearía un nuevo intervalo que abarque todo el documento, mientras que expandir el intervalo de texto por [**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) crearía un intervalo más pequeño.

### <a name="word"></a>Word

[**TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa una sola palabra completa. La definición lingüística de una palabra varía según el idioma. Para el inglés de Estados Unidos, las palabras suelen estar bordeadas por espacios o caracteres de puntuación.

Cuando [**se usa TextUnit \_ Word**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) para establecer el límite de un intervalo de texto, el intervalo de texto resultante debe incluir cualquier carácter de salto de palabra que esté presente al final de la palabra, pero antes del inicio de la palabra siguiente.

### <a name="line"></a>Línea

[**TextUnit \_ Línea**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad de texto que representa una sola línea de texto como se presenta en la ventanilla del control. Cuando se usa **TextUnit \_ Line** para establecer el límite de un intervalo de texto, un proveedor debe establecer el límite inmediatamente después del punto en el que un carácter de control interrumpe la línea o donde la ventanilla del control ajusta el texto a una nueva línea. El límite debe establecerse donde se inicia una nueva línea.

### <a name="paragraph"></a>Paragraph

[**TextUnit \_ Paragraph**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) es una unidad lingüística de texto que representa un párrafo completo. Un párrafo debe comenzar justo antes del primer carácter de un párrafo y normalmente debe terminar justo después del último carácter. Cualquier línea vacía que sigue a un párrafo debe combinarse en el párrafo, a menos que algo en el origen del texto indique lo contrario. Normalmente, el límite final de un párrafo también marca el límite final de una unidad de texto [**TextUnit \_ Line.**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit)

### <a name="page"></a>Página

[**TextUnit \_ Page**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa una página de texto completa de un documento. Los límites de una página deben establecerse en los puntos inmediatos donde una página comienza y termina.

### <a name="document"></a>Documento

[**TextUnit \_ Document**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) representa todo el contenido de un documento según lo admitido por el [patrón de](uiauto-implementingtextandtextrange.md) control Text. No debe existir texto fuera de un intervalo de texto que contenga un documento. Los objetos que se insertan en un documento, como las notas de anotación que cruzan un límite de página, deben tratarse como objetos incrustados del documento y no como parte del contenido de texto del documento.

## <a name="other-potential-ranges"></a>Otros intervalos potenciales

La [especificación del patrón](uiauto-implementingtextandtextrange.md) de control TextRange actual no permite agregar nuevos valores de unidad de texto a la enumeración [**TextUnit**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textunit) ni permite volver a definir los valores de unidad de texto existentes. Para exponer otros intervalos potenciales, como encabezados y anotaciones, un proveedor debe exponer estos intervalos como objetos incrustados con un intervalo de texto asociado. De este modo, también puede agregar compatibilidad con los patrones de control adecuados. Esta solución es más flexible y extensible que definir nuevas unidades de texto.

## <a name="related-topics"></a>Temas relacionados

### <a name="reference"></a>Referencia

[TextPatternRangeEndpoint](/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textpatternrangeendpoint)

[ITextRangeProvider::GetChildren](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextrangeprovider-getchildren)





### <a name="conceptual"></a>Conceptual

[Automatización de la interfaz de usuario compatibilidad con contenido textual](uiauto-ui-automation-textpattern-overview.md)

[Trabajar con controles basados en texto](uiauto-workingwithtextbasedcontrols.md)
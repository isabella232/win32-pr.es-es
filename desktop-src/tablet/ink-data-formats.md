---
description: 'Hay una serie de formatos en los que se pueden almacenar datos de entrada de lápiz, entre los que se incluyen:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formatos de datos de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088483400f6e4452f888793dd7b0ce78966050b65c35db9baf6e79c2f00061c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032313"
---
# <a name="ink-data-formats"></a>Formatos de datos de entrada manuscrita

Hay una serie de formatos en los que se pueden almacenar datos de entrada de lápiz, entre los que se incluyen:

-   Formato serializado de entrada de lápiz (ISF)
-   HTML
-   Formato de texto enriquecido (RTF)
-   Formato binario
-   lenguaje de marcado extensible (XML) basados en formatos

Los distintos formatos son aplicables en circunstancias diferentes. Para interactuar más correctamente con el Portapapeles, las aplicaciones deben ser capaces de reconocer y generar tantos formatos como sea posible.

El formato más importante y básico que se puede usar para almacenar la entrada de lápiz es Ink Serialized Format (ISF). ISF proporciona una representación compacta pero completa de un único [**objeto Ink.**](inkdisp-class.md)

Un formato igualmente importante es HTML. Los datos de entrada de lápiz se pueden representar en HTML de forma que las aplicaciones que no reconocen la entrada de lápiz puedan verlos como una imagen. Además, se mantiene la fidelidad total de la entrada de lápiz. Por estos motivos, y dado que es un formato que se entiende normalmente y que permite la representación de muchos tipos diferentes de contenido, Microsoft recomienda HTML como formato para compartir la entrada de lápiz.

También es posible almacenar la entrada de lápiz en otros formatos. Si usa RTF como formato, puede pegar la entrada de lápiz en aplicaciones que no reconocen la entrada de lápiz, como Microsoft Word 2002. Para ello, se insertan objetos OLE que contienen entrada manuscrita dentro de RTF. Todavía se pueden usar otros formatos, como los formatos binarios o basados en XML.

Los formatos que elija para una aplicación determinada para copiar, pegar o serializar la entrada de lápiz deben basarse en las necesidades y recursos específicos de las aplicaciones. Como mínimo, una aplicación debe poder copiar y pegar ISF, lo que permite el nivel más bajo de interoperabilidad de entrada de lápiz. Tanto ISF como la capacidad de copiar y pegar ISF están integrados en la plataforma de Tablet PC. Sin embargo, muchas aplicaciones necesitan representar contenido más complejo, como una selección que contiene varios objetos de entrada de lápiz o texto con formato. En tal caso, una aplicación puede copiar y pegar HTML. Esto permite una máxima flexibilidad. HTML es ampliamente comprensible y fácil de generar. Por último, las aplicaciones que ya generan RTF o que tienen una gran necesidad de comunicarse con aplicaciones anteriores también deben generar un formato RTF.

> [!Note]  
> A lo largo de la discusión sobre la interoperabilidad de la entrada de lápiz, el mapa de bits, ISF y GIF son formatos de imagen. El objeto de entrada de lápiz de texto (tInk) y el objeto ink de boceto (sInk) son objetos OLE. Binary, HTML, XML y RTF son formatos de documento en los que se consumen las imágenes.

 

La plataforma tablet PC proporciona API para ayudarle a generar e interpretar estos formatos. Hay muchas opciones que, juntas, deben ajustarse a las necesidades de interoperabilidad y persistencia de cualquier aplicación. Para obtener más información sobre los formatos de entrada de lápiz, vea [Formatos de persistencia.](persistence-formats.md)

 

 




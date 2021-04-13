---
description: 'Hay una serie de formatos en los que se pueden almacenar los datos de tinta, entre los que se incluyen:'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formatos de datos de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360163"
---
# <a name="ink-data-formats"></a>Formatos de datos de tinta

Hay una serie de formatos en los que se pueden almacenar los datos de tinta, entre los que se incluyen:

-   Formato serializado de tinta (ISF)
-   HTML
-   Formato de texto enriquecido (RTF)
-   Formato binario
-   Formatos basados en lenguaje de marcado extensible (XML)

Los distintos formatos se aplican en diferentes circunstancias. Para interactuar más correctamente con el portapapeles, las aplicaciones deben ser capaces de reconocer y generar tantos formatos diferentes como sea posible.

El formato más importante y básico que se puede usar para almacenar tinta es el formato serializado de tinta (ISF). ISF proporciona una representación compacta pero completa de un solo objeto de [**entrada de lápiz**](inkdisp-class.md) .

Un formato igualmente importante es HTML. Los datos de tinta se pueden representar en HTML de forma que las aplicaciones que no reconozcan la tinta puedan verlos como una imagen. Además, se mantiene la fidelidad total de la tinta. Por estos motivos, y dado que se trata de un formato comúnmente entendido que permite la representación de muchos tipos diferentes de contenido, Microsoft recomienda HTML como formato para compartir la tinta.

También es posible almacenar la entrada manuscrita en otros formatos. Mediante el uso de RTF como formato, puede pegar la entrada manuscrita en aplicaciones que no reconozcan la tinta, como Microsoft Word 2002. Para ello, se insertan objetos OLE que contienen entradas manuscritas dentro del RTF. Todavía se pueden usar otros formatos, como los formatos binarios o basados en XML.

Los formatos que elija para una aplicación determinada para copiar, pegar o serializar la tinta deberían basarse en las necesidades y los recursos específicos de las aplicaciones. Como mínimo, una aplicación debe ser capaz de copiar y pegar el ISF, lo que permite el nivel más bajo de interoperabilidad de entrada de lápiz. Tanto ISF como la capacidad de copiar y pegar el ISF están integrados en la plataforma de Tablet PC. Sin embargo, muchas aplicaciones necesitan representar contenido más complejo, como una selección que contiene varios objetos de entrada de lápiz o texto con formato. En tal caso, una aplicación puede copiar y pegar HTML. Esto permite una cantidad máxima de flexibilidad. El código HTML está ampliamente entendido y es fácil de generar. Por último, las aplicaciones que ya producen RTF o que tienen una gran necesidad de comunicarse con aplicaciones más antiguas también deben generar un formato RTF.

> [!Note]  
> A lo largo de la explicación de la interoperabilidad de entradas manuscritas, mapa de bits, ISF y GIF son formatos de imagen. El objeto de entrada manuscrita de texto (tInk) y el objeto de tinta de boceto (receptor) son objetos OLE. Binario, HTML, XML y RTF son formatos de documento en los que se consumen las imágenes.

 

La plataforma de Tablet PC proporciona API que le ayudarán a generar e interpretar estos formatos. Hay muchas opciones que juntas deben ajustarse a las necesidades de interoperabilidad y persistencia de cualquier aplicación. Para obtener más información sobre los formatos de tinta, vea [formatos de persistencia](persistence-formats.md).

 

 




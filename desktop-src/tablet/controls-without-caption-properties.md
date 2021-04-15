---
description: Introducción al uso de controles sin propiedades de título para Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controles sin propiedades de título
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539436"
---
# <a name="controls-without-caption-properties"></a>Controles sin propiedades de título

Cuando un control no tiene su propia propiedad Caption, realice los pasos siguientes para asegurarse de que las ayudas de accesibilidad pueden identificar los controles:

-   Cree un control de texto estático con un nombre descriptivo y significativo.
-   Coloque la etiqueta estática para que preceda inmediatamente al control al que se hace referencia, en el orden de tabulación.
-   Asegúrese de que el texto de la etiqueta termina con dos puntos, por ejemplo, "configuración:"
-   Coloca el texto de la etiqueta inmediatamente a la izquierda o delante del control al que se hace referencia.
-   Haga que el texto estático sea invisible si no es adecuado para mostrarlo visualmente. Para ello, asigne el atributo adecuado en el script de recursos. Esto puede ser adecuado cuando el nombre o la función de un control se proporciona visualmente a través de un control de texto estático, como un gráfico o un botón de radio relacionado.

El uso correcto de los controles estáticos es la única manera de implementar correctamente las teclas de acceso subrayadas para los controles que no tienen etiquetas intrínsecas. Para obtener más información sobre el uso de controles que no tienen propiedades de título, vea la sección [accesibilidad](/windows/desktop/accessibility) .

 

 

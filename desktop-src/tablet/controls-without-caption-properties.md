---
description: Introducción al uso de controles sin propiedades de título para tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controles sin propiedades de título
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256809"
---
# <a name="controls-without-caption-properties"></a>Controles sin propiedades de título

Cuando un control no tenga su propia propiedad caption, siga estos pasos para asegurarse de que las ayuda de accesibilidad puedan identificar los controles:

-   Cree un control de texto estático con un nombre descriptivo y descriptivo.
-   Coloque la etiqueta estática para que preceda inmediatamente al control al que se hace referencia, en orden de tabulación.
-   Asegúrese de que el texto de la etiqueta termina con dos puntos, por ejemplo, "Configuración:"
-   Coloque el texto de la etiqueta inmediatamente a la izquierda o antes del control al que se hace referencia.
-   Haga que el texto estático sea invisible si no es adecuado mostrarlo visualmente. Para ello, asigne el atributo adecuado en el script de recursos. Esto puede ser adecuado cuando el nombre o la función de un control se proporciona visualmente por medios distintos del control de texto estático, como un gráfico o un botón de radio relacionado.

El uso adecuado de los controles estáticos es la única manera de implementar correctamente las claves de acceso subrayadas para los controles que no tienen etiquetas intrínsecas. Para obtener más información sobre el uso de controles que no tienen propiedades de título, vea la [sección Accesibilidad.](/windows/desktop/accessibility)

 

 

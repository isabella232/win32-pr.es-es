---
description: En el tema siguiente se describe cómo funciona Windows API de plataforma de evaluación de Windows como servicio (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Acerca de la plataforma de evaluación de WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79493900d508a8a613953f1f9b7bbd0f67e2a200761148b7fe31d9fb31ce3609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958955"
---
# <a name="about-the-waas-assessment-platform"></a>Acerca de la plataforma de evaluación de WaaS

En el tema siguiente se describe cómo funciona Windows API de plataforma de evaluación de Windows como servicio (WaaS).

WaaS Assessment API ofrece al autor de la llamada la siguiente información:

-   Si un dispositivo está en las actualizaciones más recientes de Microsoft.
-   Si el dispositivo ha alcanzado el final del soporte técnico.
-   Los tiempos de lanzamiento de las actualizaciones aplicables más recientes para el dispositivo.
-   Una evaluación de por qué un dispositivo no está actualizado y el posible impacto que puede tener en el dispositivo.

La plataforma de evaluación de WaaS usa el modelo de API COM y se ejecuta automáticamente al menos una vez al día. Este ciclo detecta la información de versión aplicable. Durante el período almacenado en caché, se realizan evaluaciones con respecto a la información de versión almacenada en caché. Si se realiza una llamada fuera de la ventana de expiración de la caché, se realiza una nueva llamada y evaluación, se almacena en caché y se devuelve. Cuando se realiza una llamada, el cliente de evaluación de WaaS se pone en contacto con el servicio de evaluación de WaaS con los atributos del dispositivo y recibe un dossier de información aplicable al dispositivo. A continuación, el cliente usa esta información en la información que recopila sobre el dispositivo para realizar la evaluación.

> [!NOTE]
> El código debe tener privilegios de administrador para llamar a Waas Assessment API. Para más información sobre el desarrollo de aplicaciones que requieren privilegios de administrador, consulte [este artículo.](../secauthz/developing-applications-that-require-administrator-privilege.md)

 

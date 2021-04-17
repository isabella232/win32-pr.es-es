---
description: En el siguiente tema se describe cómo funciona la API de la plataforma de evaluación de Windows como servicio (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Acerca de la plataforma de evaluación de WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667597"
---
# <a name="about-the-waas-assessment-platform"></a>Acerca de la plataforma de evaluación de WaaS

En el siguiente tema se describe cómo funciona la API de la plataforma de evaluación de Windows como servicio (WaaS).

La API de evaluación de WaaS ofrece al llamador la siguiente información:

-   Si un dispositivo está en las últimas actualizaciones de Microsoft.
-   Si el dispositivo ha alcanzado el final del soporte técnico.
-   Los tiempos de lanzamiento de las actualizaciones aplicables más recientes para el dispositivo.
-   Una evaluación de la razón por la que un dispositivo no está actualizado y el posible impacto que puede tener en el dispositivo.

La plataforma de evaluación de WaaS usa el modelo de API de COM y se ejecuta automáticamente al menos una vez al día. Este ciclo captura la información de la versión aplicable. Durante el período de almacenamiento en caché, las evaluaciones se realizan en la información de la versión almacenada en caché. Si se realiza una llamada fuera de la ventana de expiración de la caché, se realiza una nueva llamada y evaluación, se almacena en caché y se devuelve. Cuando se realiza una llamada, el cliente de evaluación de WaaS se pone en contacto con el servicio de evaluación de WaaS con los atributos del dispositivo y recibe un expediente de información aplicable al dispositivo. Después, el cliente usa esta información en la información que recopila sobre el dispositivo para realizar la evaluación.

> [!NOTE]
> El código debe tener privilegios de administrador para llamar a la API de evaluación de WAAS. Para obtener más información sobre cómo desarrollar aplicaciones que requieran privilegios de administrador, consulte [este artículo](../secauthz/developing-applications-that-require-administrator-privilege.md).

 

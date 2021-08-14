---
description: Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticación implícita de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e5374515acb0604ee14a6770b9523e9bf31fd0e2d6c946fec26d2ad789c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921834"
---
# <a name="microsoft-digest-authentication"></a>Autenticación implícita de Microsoft

Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente. El servidor comprueba que el cliente no se ha autenticado y, a continuación, realiza la autenticación inicial mediante el acceso a los servicios de un controlador de dominio. Para obtener una descripción detallada de este procedimiento, vea [Autenticación inicial mediante Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Cuando la autenticación inicial se realiza correctamente, el servidor recibe una clave de [*sesión implícita*](../secgloss/s-gly.md). El servidor almacena en caché esta clave y la usa para autenticar las solicitudes posteriores de recursos del cliente. Esta autenticación es local, es decir, no requiere acceso a un controlador de dominio. Para obtener una descripción detallada de este procedimiento, vea [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Cuando se usa HTTP, no se mantiene ninguna conexión entre el cliente y el servidor. Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, Microsoft Digest almacena en caché la información recibida después de la autenticación correcta. Para obtener información sobre este proceso, vea [Mantener el contexto de seguridad entre conexiones](maintaining-the-security-context-between-connections.md).

 

 

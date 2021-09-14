---
description: Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticación implícita de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173477"
---
# <a name="microsoft-digest-authentication"></a>Autenticación implícita de Microsoft

Microsoft Digest realiza una autenticación inicial cuando el servidor recibe la primera respuesta de desafío de un cliente. El servidor comprueba que el cliente no se ha autenticado y, a continuación, realiza la autenticación inicial mediante el acceso a los servicios de un controlador de dominio. Para obtener una descripción detallada de este procedimiento, vea [Autenticación inicial mediante Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Cuando la autenticación inicial se realiza correctamente, el servidor recibe una clave de [*sesión implícita*](../secgloss/s-gly.md). El servidor almacena en caché esta clave y la usa para autenticar las solicitudes posteriores de recursos del cliente. Esta autenticación es local, es decir, no requiere acceso a un controlador de dominio. Para obtener una descripción detallada de este procedimiento, vea [Authenticating Subsequent Requests Using Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Cuando se usa HTTP, no se mantiene ninguna conexión entre el cliente y el servidor. Para reducir el tráfico del controlador de dominio y mejorar el rendimiento, Microsoft Digest la información recibida después de una autenticación correcta. Para obtener información sobre este proceso, vea [Mantener el contexto de seguridad entre conexiones](maintaining-the-security-context-between-connections.md).

 

 

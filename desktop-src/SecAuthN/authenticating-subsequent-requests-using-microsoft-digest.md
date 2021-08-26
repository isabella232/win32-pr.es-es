---
description: El servidor envía al cliente una referencia a su contexto de seguridad compartido mediante la directiva opaca del desafío Digest.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Autenticación de solicitudes posteriores con Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25954612a99fa0a0a9710f5e8e0679948cc3bac5ceae669a06ec40bd5c22241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101434"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Autenticación de solicitudes posteriores con Microsoft Digest

El servidor envía al cliente una referencia a su contexto [*de seguridad compartido*](/windows/desktop/SecGloss/s-gly) mediante la directiva opaca del desafío Digest. Después de una autenticación correcta, el cliente debe especificar este valor en las solicitudes posteriores al servidor de destino. Incluir el valor opaco en las solicitudes de recursos a los que se puede acceder mediante el contexto de seguridad existente elimina la necesidad de volver a autenticarse en el controlador de dominio. Estas solicitudes se autentican de nuevo en el servidor mediante la clave de [*sesión*](/windows/desktop/SecGloss/s-gly) implícita almacenada en caché después de la autenticación inicial.

En el diagrama siguiente se ilustran los pasos que ha llevado a través del cliente y el servidor durante una solicitud posterior de recursos protegidos por acceso.

![autenticación de solicitudes posteriores mediante la síntesis de Microsoft](images/digest2.png)

Para solicitar recursos adicionales después de una autenticación correcta, el cliente llama a Microsoft Digest [**función MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una respuesta de desafío implícita. El valor opaco se incluye en la directiva opaca de la respuesta de desafío enviada al servidor como un encabezado de autorización (que se muestra como solicitud HTTP).

El servidor llama a [**la función AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) para determinar si hay un contexto de [*seguridad existente*](/windows/desktop/SecGloss/s-gly) para el cliente. Cuando se encuentra un contexto existente, la función devuelve SEC E COMPLETE NEEDED para indicar que el servidor debe llamar a \_ \_ la función \_ [**CompleteAuthToken.**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) Esta función realiza la autenticación del cliente [](initial-authentication-using-microsoft-digest.md) mediante la clave [*de*](/windows/desktop/SecGloss/s-gly) sesión implícita almacenada en caché durante la autenticación inicial en lugar de volver a autenticarse en el controlador de dominio.

 

 

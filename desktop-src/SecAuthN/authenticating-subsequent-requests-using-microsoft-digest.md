---
description: El servidor envía al cliente una referencia a su contexto de seguridad compartido mediante la Directiva opaca del desafío de síntesis.
ms.assetid: 543c4bed-b224-4da7-9746-12c9993a40af
title: Autenticación de solicitudes posteriores con Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eecccc3be68fb541994e63cdfc5035187e04aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816222"
---
# <a name="authenticating-subsequent-requests-with-microsoft-digest"></a>Autenticación de solicitudes posteriores con Microsoft Digest

El servidor envía al cliente una referencia a su [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) compartido mediante la Directiva opaca del desafío de síntesis. Después de una autenticación correcta, el cliente debe especificar este valor en las solicitudes posteriores al servidor de destino. Si se incluye el valor opaco en las solicitudes de recursos a los que se puede acceder mediante el contexto de seguridad existente, se elimina la necesidad de volver a autenticarse en el controlador de dominio. Estas solicitudes se vuelven a autenticar en el servidor, mediante la [*clave de sesión*](/windows/desktop/SecGloss/s-gly) de síntesis almacenada en caché después de la autenticación inicial.

En el diagrama siguiente se muestran los pasos realizados por el cliente y el servidor durante una solicitud posterior de recursos protegidos de acceso.

![autenticación de solicitudes posteriores mediante el Resumen de Microsoft](images/digest2.png)

Para solicitar recursos adicionales después de una autenticación correcta, el cliente llama a la función Microsoft Digest [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una respuesta de desafío de síntesis. El valor opaco se incluye en la Directiva opaca de la respuesta de desafío enviada al servidor como un encabezado de autorización (se muestra como solicitud HTTP).

El servidor llama a la función [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) para determinar si hay un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) existente para el cliente. Cuando se encuentra un contexto existente, la función devuelve la hora \_ E \_ completa \_ necesaria para indicar que el servidor debe llamar a la función [**CompleteAuthToken**](/windows/desktop/api/Sspi/nf-sspi-completeauthtoken) . Esta función realiza la autenticación del cliente mediante la [*clave de sesión*](/windows/desktop/SecGloss/s-gly) de síntesis almacenada en la memoria caché durante la [autenticación inicial](initial-authentication-using-microsoft-digest.md) en lugar de volver a autenticarse en el controlador de dominio.

 

 

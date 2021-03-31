---
description: La semántica de los contextos de datagramas o sin conexión difiere ligeramente de la de los contextos orientados a la conexión.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextos de datagramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154773"
---
# <a name="datagram-contexts"></a>Contextos de datagramas

La semántica de los contextos de [*datagramas*](/windows/desktop/SecGloss/d-gly)o sin conexión difiere ligeramente de la de los contextos orientados a la conexión. En el [*contexto*](/windows/desktop/SecGloss/c-gly)sin conexión de un datagrama, un servidor no puede determinar si el cliente se ha cerrado o ha finalizado la conexión. En otras palabras, no se pasa ningún aviso de finalización de la aplicación de transporte al servidor como sucedería en un contexto orientado a la conexión.

Para utilizar un contexto de datagrama, un cliente establece la \_ \_ marca de datagrama req de ISC en su llamada a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .

> [!IMPORTANT]
> El paquete de [Microsoft Kerberos](microsoft-kerberos.md) no admite contextos de datagramas en modo de usuario a usuario.

 

Para admitir mejor algunos modelos, especialmente RPC de estilo DCE, se aplican las reglas siguientes cuando el cliente usa un contexto de datagrama:

-   El [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) no genera un [*BLOB*](/windows/desktop/SecGloss/b-gly) de autenticación (objeto binario grande) en la primera llamada a [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta). Sin embargo, el cliente puede utilizar el contexto de seguridad devuelto en una llamada a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma para un mensaje.
-   El paquete de seguridad debe permitir que el contexto se vuelva a establecer varias veces para permitir que el servidor Quite la conexión sin previo aviso. Esto implica que cualquier clave utilizada en las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) se puede restablecer a un [*Estado*](/windows/desktop/SecGloss/s-gly)coherente.
-   El paquete de seguridad permite al llamador especificar la información de la secuencia y proporciona esa información de secuencia en el lado del receptor. Esto se suma a cualquier información de secuencia mantenida por el paquete.

Un paquete de seguridad establece la \_ marca de datagrama de marca SECPKG \_ para indicar que admite la semántica de datagramas.

 

 

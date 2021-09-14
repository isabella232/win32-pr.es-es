---
description: La semántica de los contextos sin conexión o datagramas difiere ligeramente de los contextos orientados a conexiones.
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: Contextos de datagrama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361865"
---
# <a name="datagram-contexts"></a>Contextos de datagrama

La semántica de los [*contextos de datagrama*](/windows/desktop/SecGloss/d-gly)o sin conexión difiere ligeramente de la de los contextos orientados a la conexión. En el contexto sin [](/windows/desktop/SecGloss/c-gly)conexión de un datagrama, un servidor no puede determinar cuándo el cliente ha cerrado o terminado de otro modo la conexión. En otras palabras, no se pasa ningún aviso de terminación de la aplicación de transporte al servidor como se produciría en un contexto orientado a la conexión.

Para usar un contexto de datagrama, un cliente establece la marca DATAGRAM DE ISC REQ en su llamada a la \_ \_ función [**InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)

> [!IMPORTANT]
> El [paquete de Microsoft Kerberos](microsoft-kerberos.md) no admite contextos de datagramas en modo de usuario a usuario.

 

Para admitir mejor algunos modelos, especialmente RPC de estilo DCE, se aplican las siguientes reglas cuando el cliente usa un contexto de datagrama:

-   El [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) no genera un [*BLOB*](/windows/desktop/SecGloss/b-gly) de autenticación (objeto binario grande) en la primera llamada a [**InitializeSecurityContext (general).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Sin embargo, el cliente puede usar el contexto de seguridad devuelto en una llamada a la [**función MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma para un mensaje.
-   El paquete de seguridad debe permitir que el contexto se vuelva a establecer varias veces para permitir que el servidor coloque la conexión sin previo aviso. Esto implica que todas las claves usadas en las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) se pueden restablecer a un estado [*coherente.*](/windows/desktop/SecGloss/s-gly)
-   El paquete de seguridad permite al autor de la llamada especificar información de secuencia y proporciona esa información de secuencia en el lado receptor. Esto se suma a cualquier información de secuencia mantenida por el paquete.

Un paquete de seguridad establece la marca DATAGRAM SECPKG \_ FLAG para indicar que admite la semántica de \_ datagramas.

 

 

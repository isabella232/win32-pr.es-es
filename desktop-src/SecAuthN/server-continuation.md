---
description: Según el código de retorno de una llamada anterior a AcceptSecurityContext (General), el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuación del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06863a0e94fcfe65c7ab695d30be92044fe7341ffa0eb9091c5f1a81acdffc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918294"
---
# <a name="server-continuation"></a>Continuación del servidor

Según el código de retorno de una llamada anterior a [**AcceptSecurityContext (General),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente. Para continuar con el protocolo de autenticación, el servidor repite las llamadas **a AcceptSecurityContext (General).**

El estado devuelto por [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) se comprueba para ver si el servidor debe esperar mensajes adicionales del cliente. En la mayoría de los protocolos de autenticación, hay un número máximo de intercambios incluso para la autenticación mutua. Actualmente, los [*protocolos*](../secgloss/k-gly.md) NTLM y Kerberos hacen autenticación mutua con tres intercambios.

 

 

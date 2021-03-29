---
description: En función del código de retorno de una llamada anterior a AcceptSecurityContext (general), el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuación del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667111"
---
# <a name="server-continuation"></a>Continuación del servidor

En función del código de retorno de una llamada anterior a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), el servidor puede esperar una respuesta del cliente y puede participar en intercambios adicionales con el cliente. Para continuar el protocolo de autenticación, el servidor repite las llamadas a **AcceptSecurityContext (general)**.

El estado devuelto por [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) se comprueba para ver si el servidor tiene que esperar más mensajes del cliente. En la mayoría de los protocolos de autenticación, hay un número máximo de intercambios incluso para la autenticación mutua. Actualmente, los protocolos NTLM y [*Kerberos*](../secgloss/k-gly.md) realizan la autenticación mutua con tres intercambios.

 

 

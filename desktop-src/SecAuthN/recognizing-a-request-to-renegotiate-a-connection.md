---
description: La función DecryptMessage (general) intercepta las solicitudes de renegociación procedentes del remitente del mensaje. Notifica a la aplicación mediante el descifrado de los datos del mensaje y la devolución del \_ \_ valor de RENEGOCIAR s s.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconocimiento de una solicitud para volver a negociar una conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082612"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Reconocimiento de una solicitud para volver a negociar una conexión

La función [**DecryptMessage (general)**](decryptmessage--general.md) intercepta las solicitudes de renegociación procedentes del remitente del mensaje. Notifica a la aplicación mediante el descifrado de los datos del mensaje y la devolución del \_ \_ valor de RENEGOCIAR s s.

La aplicación debe controlar estas solicitudes llamando a [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) (Servers) o [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) (clientes) y pasando el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN. Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.

 

 




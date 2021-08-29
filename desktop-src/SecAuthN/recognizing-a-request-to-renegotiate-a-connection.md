---
description: La función DecryptMessage (General) captura las solicitudes de renegociación procedentes del remitente del mensaje. Notifica a la aplicación descifrando los datos del mensaje y devolviendo el valor SEC \_ I \_ RENEGOTIATE.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconocer una solicitud para volver a negociar una conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 799ed36292b9542795036a697869a00176d7f068eebb6981edd28adbec2e0d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919684"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Reconocer una solicitud para volver a negociar una conexión

La [**función DecryptMessage (General)**](decryptmessage--general.md) captura las solicitudes de renegociación procedentes del remitente del mensaje. Notifica a la aplicación descifrando los datos del mensaje y devolviendo el valor SEC \_ I \_ RENEGOTIATE.

La aplicación debe controlar estas solicitudes llamando a [**AcceptSecurityContext (General) (servidores)**](acceptsecuritycontext--general.md) o [**InitializeSecurityContext (general) (clientes)**](initializesecuritycontext--general.md) y pasando el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN. Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.

 

 




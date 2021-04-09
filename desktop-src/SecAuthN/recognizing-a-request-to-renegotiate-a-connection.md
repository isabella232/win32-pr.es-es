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
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a><span data-ttu-id="b275e-104">Reconocimiento de una solicitud para volver a negociar una conexión</span><span class="sxs-lookup"><span data-stu-id="b275e-104">Recognizing a Request to Renegotiate a Connection</span></span>

<span data-ttu-id="b275e-105">La función [**DecryptMessage (general)**](decryptmessage--general.md) intercepta las solicitudes de renegociación procedentes del remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b275e-105">The [**DecryptMessage (General)**](decryptmessage--general.md) function traps requests for renegotiation coming from the message sender.</span></span> <span data-ttu-id="b275e-106">Notifica a la aplicación mediante el descifrado de los datos del mensaje y la devolución del \_ \_ valor de RENEGOCIAR s s.</span><span class="sxs-lookup"><span data-stu-id="b275e-106">It notifies your application by decrypting the message data and returning the SEC\_I\_RENEGOTIATE value.</span></span>

<span data-ttu-id="b275e-107">La aplicación debe controlar estas solicitudes llamando a [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md) (Servers) o [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md) (clientes) y pasando el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="b275e-107">Your application must handle such requests by calling [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) (servers) or [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md) (clients) and passing the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="b275e-108">Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="b275e-108">After this initial call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 




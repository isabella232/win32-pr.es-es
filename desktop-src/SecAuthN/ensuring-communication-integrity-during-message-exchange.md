---
description: Una vez establecido un contexto de seguridad, la aplicación puede usar las funciones de compatibilidad de mensajes para transmitir mensajes resistentes a manipulaciones.
ms.assetid: 43d7b940-1816-429f-be6e-40978efed278
title: Garantizar la integridad de la comunicación durante el intercambio de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70545abf11a933cd3bb6d0c32f3312637fcccbe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154090"
---
# <a name="ensuring-communication-integrity-during-message-exchange"></a><span data-ttu-id="1afc9-103">Garantizar la integridad de la comunicación durante el intercambio de mensajes</span><span class="sxs-lookup"><span data-stu-id="1afc9-103">Ensuring Communication Integrity During Message Exchange</span></span>

<span data-ttu-id="1afc9-104">Una vez establecido un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) , la aplicación puede usar las funciones de [compatibilidad de mensajes](authentication-functions.md) para transmitir mensajes resistentes a manipulaciones.</span><span class="sxs-lookup"><span data-stu-id="1afc9-104">After a [*security context*](/windows/desktop/SecGloss/s-gly) is established, the application can use the [message support](authentication-functions.md) functions to transmit tamper-resistant messages.</span></span>

<span data-ttu-id="1afc9-105">El cliente o servidor pasa el contexto de seguridad y un mensaje a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para generar una firma segura que impida que el mensaje se modifique mientras está en tránsito.</span><span class="sxs-lookup"><span data-stu-id="1afc9-105">The client or server passes the security context and a message to the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to generate a secure signature that prevents the message from being modified while in transit.</span></span> <span data-ttu-id="1afc9-106">El receptor del mensaje llama a la función [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="1afc9-106">The receiver of the message calls the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function.</span></span> <span data-ttu-id="1afc9-107">**VerifySignature** usa la información de la firma para comprobar que el mensaje recibido no se modificó durante la transmisión.</span><span class="sxs-lookup"><span data-stu-id="1afc9-107">**VerifySignature** uses the information in the signature to verify that the message received was not modified during transmission.</span></span> <span data-ttu-id="1afc9-108">El cliente y el servidor también pueden intercambiar mensajes cifrados mediante [**EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="1afc9-108">The client and server can also exchange encrypted messages using [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span>

<span data-ttu-id="1afc9-109">El servidor en una conexión autenticada también puede establecer conexiones con otros equipos remotos en el nombre del cliente después de llamar a [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="1afc9-109">The server in an authenticated connection can also make connections with other remote computers in the name of the client after calling [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext).</span></span>

 

 

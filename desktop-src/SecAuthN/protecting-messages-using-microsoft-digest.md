---
description: Explica cómo proteger los mensajes mediante Microsoft Digest.
ms.assetid: 15509d51-80c0-4d5c-aa24-4dc17de3f12c
title: Protección de mensajes mediante Microsoft Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573eafcf66e23188546abd3acd316095ec100187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652759"
---
# <a name="protecting-messages-using-microsoft-digest"></a><span data-ttu-id="f63ad-103">Protección de mensajes mediante Microsoft Digest</span><span class="sxs-lookup"><span data-stu-id="f63ad-103">Protecting Messages Using Microsoft Digest</span></span>

## <a name="http-and-sasl"></a><span data-ttu-id="f63ad-104">HTTP y SASL</span><span class="sxs-lookup"><span data-stu-id="f63ad-104">HTTP and SASL</span></span>

<span data-ttu-id="f63ad-105">Como forma de detectar ciertos tipos de infracciones de seguridad, el cliente y el servidor usan las funciones de [*integridad*](../secgloss/i-gly.md) de mensajes [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) de la interfaz del proveedor de [compatibilidad para seguridad](sspi.md) (SSPI) para proteger los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f63ad-105">As a means of detecting certain types of security violations, the client and server use the [security support provider interface](sspi.md) (SSPI) message [*integrity*](../secgloss/i-gly.md) functions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) to protect messages.</span></span>

<span data-ttu-id="f63ad-106">Un cliente llama a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) para firmar un mensaje mediante su [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f63ad-106">A client calls the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) function to sign a message using its [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f63ad-107">El servidor utiliza la función [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) para comprobar el origen del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f63ad-107">The server uses the [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) function to verify the message's origin.</span></span> <span data-ttu-id="f63ad-108">Además de comprobar la [*firma*](../secgloss/d-gly.md) que acompaña al mensaje, la función **VerifySignature** también comprueba que el número de [*nonce*](../secgloss/n-gly.md) (especificado por la Directiva de NC) es uno mayor que el último recuento enviado para el nonce.</span><span class="sxs-lookup"><span data-stu-id="f63ad-108">In addition to verifying the [*signature*](../secgloss/d-gly.md) that accompanies the message, the **VerifySignature** function also checks that the [*nonce*](../secgloss/n-gly.md) count (specified by the nc directive) is one greater than the last count sent for the nonce.</span></span> <span data-ttu-id="f63ad-109">Si no es así, la función **VerifySignature** devuelve un \_ \_ \_ código de error seg. de secuencia.</span><span class="sxs-lookup"><span data-stu-id="f63ad-109">If this is not the case, the **VerifySignature** function returns an SEC\_OUT\_OF\_SEQUENCE error code.</span></span>

## <a name="sasl-only"></a><span data-ttu-id="f63ad-110">Solo SASL</span><span class="sxs-lookup"><span data-stu-id="f63ad-110">SASL Only</span></span>

<span data-ttu-id="f63ad-111">Las funciones [**EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) proporcionan confidencialidad para los mensajes posteriores a la autenticación intercambiados entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="f63ad-111">The [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) functions supply confidentiality for post-authentication messages exchanged between client and server.</span></span>

<span data-ttu-id="f63ad-112">Para poder usar las funciones de confidencialidad de mensajes, el servidor y el cliente deben haber establecido un [*contexto de seguridad*](../secgloss/s-gly.md) con los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="f63ad-112">In order to use the message confidentiality functions, the server and client must have established a [*security context*](../secgloss/s-gly.md) with the following attributes:</span></span>

-   <span data-ttu-id="f63ad-113">La calidad de protección, especificada por la Directiva qop, debe ser "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="f63ad-113">Quality of protection, specified by the qop directive, must be "auth-conf".</span></span>
-   <span data-ttu-id="f63ad-114">Se debe haber especificado un mecanismo de cifrado mediante la Directiva Cipher.</span><span class="sxs-lookup"><span data-stu-id="f63ad-114">An encryption mechanism must have been specified by means of the cipher directive.</span></span>

 

 

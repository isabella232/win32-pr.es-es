---
description: La calidad de protección, identificada por la Directiva qop, la especifica primero el servidor en el desafío de síntesis y, a continuación, la confirma el cliente en la respuesta de desafío.
ms.assetid: bee4236c-69e5-4281-a6b3-be316bac0a11
title: Calidad de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4643c9e2de77647a3adf2cbf0441e31bcf5be5de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083188"
---
# <a name="quality-of-protection"></a><span data-ttu-id="9533d-103">Calidad de protección</span><span class="sxs-lookup"><span data-stu-id="9533d-103">Quality of Protection</span></span>

<span data-ttu-id="9533d-104">La calidad de protección, identificada por la Directiva qop, la especifica primero el servidor en el desafío de síntesis y, a continuación, la confirma el cliente en la respuesta de desafío.</span><span class="sxs-lookup"><span data-stu-id="9533d-104">The quality of protection, identified by the qop directive, is first specified by the server in the Digest challenge, and then confirmed by the client in the challenge response.</span></span> <span data-ttu-id="9533d-105">Si el cliente requiere una calidad de protección que el servidor no admite, el cliente debe finalizar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="9533d-105">If the client requires a quality of protection that the server does not support, the client must terminate the authentication.</span></span>

<span data-ttu-id="9533d-106">Los valores posibles de la Directiva qop se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9533d-106">The possible values for the qop directive are described in the following table.</span></span>



| <span data-ttu-id="9533d-107">Value</span><span class="sxs-lookup"><span data-stu-id="9533d-107">Value</span></span>                   | <span data-ttu-id="9533d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9533d-108">Description</span></span>                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9533d-109">autenticación</span><span class="sxs-lookup"><span data-stu-id="9533d-109">"auth"</span></span>                  | <span data-ttu-id="9533d-110">Sólo autenticación.</span><span class="sxs-lookup"><span data-stu-id="9533d-110">Authentication only.</span></span>                                                                                                                         |
| <span data-ttu-id="9533d-111">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="9533d-111">"auth-int"</span></span>              | <span data-ttu-id="9533d-112">Autenticación y comprobación de la [*integridad*](../secgloss/i-gly.md) mediante firmas.</span><span class="sxs-lookup"><span data-stu-id="9533d-112">Authentication and [*integrity*](../secgloss/i-gly.md) checking using signatures.</span></span>                  |
| <span data-ttu-id="9533d-113">(Solo SASL) "auth-conf"</span><span class="sxs-lookup"><span data-stu-id="9533d-113">(SASL only) "auth-conf"</span></span> | <span data-ttu-id="9533d-114">Autenticación, integridad y comprobación de confidencialidad mediante firmas y cifrado.</span><span class="sxs-lookup"><span data-stu-id="9533d-114">Authentication, integrity and confidentiality checking by using signatures and encryption.</span></span> <span data-ttu-id="9533d-115">Para obtener más información, vea [cifrado](ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="9533d-115">For more information, see [Ciphers](ciphers.md).</span></span> |



 

<span data-ttu-id="9533d-116">La calidad de la protección viene determinada por las marcas de requisitos de contexto que se pasan al Microsoft Digest SSP.</span><span class="sxs-lookup"><span data-stu-id="9533d-116">Quality of protection is determined by context requirement flags passed to the Microsoft Digest SSP.</span></span> <span data-ttu-id="9533d-117">En la tabla siguiente se enumeran las marcas relacionadas con la calidad de la protección y el valor resultante de la Directiva qop.</span><span class="sxs-lookup"><span data-stu-id="9533d-117">The following table lists the flags related to quality of protection, and the resulting value of the qop directive.</span></span>



| <span data-ttu-id="9533d-118">Marca</span><span class="sxs-lookup"><span data-stu-id="9533d-118">Flag</span></span>                         | <span data-ttu-id="9533d-119">valor qop</span><span class="sxs-lookup"><span data-stu-id="9533d-119">qop value</span></span>               |
|------------------------------|-------------------------|
| <span data-ttu-id="9533d-120">*XXX* \_ \_confidencialidad de REQ</span><span class="sxs-lookup"><span data-stu-id="9533d-120">*XXX*\_REQ\_CONFIDENTIALITY</span></span>  | <span data-ttu-id="9533d-121">"auth-conf" (solo SASL)</span><span class="sxs-lookup"><span data-stu-id="9533d-121">"auth-conf" (SASL only)</span></span> |
| <span data-ttu-id="9533d-122">*XXX* \_ detección de la reproducción de REQ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9533d-122">*XXX*\_REQ\_REPLAY\_DETECT</span></span>   | <span data-ttu-id="9533d-123">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="9533d-123">"auth-int"</span></span>              |
| <span data-ttu-id="9533d-124">*XXX* \_ \_detección de secuencia de REQ \_</span><span class="sxs-lookup"><span data-stu-id="9533d-124">*XXX*\_REQ\_SEQUENCE\_DETECT</span></span> | <span data-ttu-id="9533d-125">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="9533d-125">"auth-int"</span></span>              |
| <span data-ttu-id="9533d-126">*XXX* \_ integridad de REQ \_</span><span class="sxs-lookup"><span data-stu-id="9533d-126">*XXX*\_REQ\_INTEGRITY</span></span>        | <span data-ttu-id="9533d-127">"auth-int"</span><span class="sxs-lookup"><span data-stu-id="9533d-127">"auth-int"</span></span>              |
| <span data-ttu-id="9533d-128">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="9533d-128">(none)</span></span>                       | <span data-ttu-id="9533d-129">autenticación</span><span class="sxs-lookup"><span data-stu-id="9533d-129">"auth"</span></span>                  |



 

> [!Note]  
> <span data-ttu-id="9533d-130">Las marcas de requisitos de contexto especificadas por las aplicaciones de servidor tienen un prefijo de ASC y las especificadas por los clientes tienen el prefijo ISC.</span><span class="sxs-lookup"><span data-stu-id="9533d-130">Context requirement flags specified by server applications have a prefix of ASC, and those specified by clients are prefixed with ISC.</span></span> <span data-ttu-id="9533d-131">Para determinar los valores de marca usados por la aplicación, sustituya uno de estos prefijos por *XXX*.</span><span class="sxs-lookup"><span data-stu-id="9533d-131">To determine the flag values used by your application, substitute one of these prefixes for *XXX*.</span></span>

 

<span data-ttu-id="9533d-132">Para obtener información adicional relacionada con el servidor, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="9533d-132">For additional server-related information, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

<span data-ttu-id="9533d-133">Para obtener información adicional relacionada con el cliente, consulte [generación de la respuesta de desafío de síntesis](generating-the-digest-challenge-response.md).</span><span class="sxs-lookup"><span data-stu-id="9533d-133">For additional client-related information, see [Generating the Digest Challenge Response](generating-the-digest-challenge-response.md).</span></span>

 

 

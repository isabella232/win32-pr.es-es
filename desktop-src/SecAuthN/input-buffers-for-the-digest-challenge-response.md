---
description: La autenticación HTTP mediante Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío. En la tabla siguiente se resumen estos búferes.
ms.assetid: 0df02be2-f42e-46d0-a206-765adf3d7a72
title: Búferes de entrada para la respuesta de desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982923782b13e37a5e3531717dabf47016c60932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153840"
---
# <a name="input-buffers-for-the-digest-challenge-response"></a><span data-ttu-id="f27ac-104">Búferes de entrada para la respuesta de desafío de síntesis</span><span class="sxs-lookup"><span data-stu-id="f27ac-104">Input Buffers for the Digest Challenge Response</span></span>

<span data-ttu-id="f27ac-105">La autenticación HTTP mediante Microsoft Digest requiere tres búferes de entrada para generar una respuesta de desafío.</span><span class="sxs-lookup"><span data-stu-id="f27ac-105">HTTP authentication using Microsoft Digest requires three input buffers to generate a challenge response.</span></span> <span data-ttu-id="f27ac-106">En la tabla siguiente se resumen estos búferes.</span><span class="sxs-lookup"><span data-stu-id="f27ac-106">The following table summarizes these buffers.</span></span>



| <span data-ttu-id="f27ac-107">Número de búfer</span><span class="sxs-lookup"><span data-stu-id="f27ac-107">Buffer number</span></span> | <span data-ttu-id="f27ac-108">Contiene</span><span class="sxs-lookup"><span data-stu-id="f27ac-108">Contains</span></span>                                                                                                                                             | <span data-ttu-id="f27ac-109">Tipo de búfer</span><span class="sxs-lookup"><span data-stu-id="f27ac-109">Buffer type</span></span>                                                 |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f27ac-110">0</span><span class="sxs-lookup"><span data-stu-id="f27ac-110">0</span></span>             | <span data-ttu-id="f27ac-111">Desafío recibido del servidor</span><span class="sxs-lookup"><span data-stu-id="f27ac-111">Challenge received from the Server</span></span>                                                                                                                   | <span data-ttu-id="f27ac-112">\_token SECBUFFER</span><span class="sxs-lookup"><span data-stu-id="f27ac-112">SECBUFFER\_TOKEN</span></span>                                            |
| <span data-ttu-id="f27ac-113">1</span><span class="sxs-lookup"><span data-stu-id="f27ac-113">1</span></span>             | <span data-ttu-id="f27ac-114">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="f27ac-114">HTTP Method</span></span>                                                                                                                                          | <span data-ttu-id="f27ac-115">PARÁMETROS de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="f27ac-115">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="f27ac-116">2</span><span class="sxs-lookup"><span data-stu-id="f27ac-116">2</span></span>             | <span data-ttu-id="f27ac-117">H (entidad)</span><span class="sxs-lookup"><span data-stu-id="f27ac-117">H(Entity)</span></span>                                                                                                                                            | <span data-ttu-id="f27ac-118">PARÁMETROS de SECBUFFER \_</span><span class="sxs-lookup"><span data-stu-id="f27ac-118">SECBUFFER\_PARAMS</span></span>                                           |
| <span data-ttu-id="f27ac-119">3</span><span class="sxs-lookup"><span data-stu-id="f27ac-119">3</span></span>             | <span data-ttu-id="f27ac-120">El [*nombre de entidad*](../secgloss/s-gly.md) de seguridad de servicio (SPN) del servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="f27ac-120">The [*service principal name*](../secgloss/s-gly.md) (SPN) of the target server.</span></span> | <span data-ttu-id="f27ac-121">**SECBUFFER \_ \_host de destino** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f27ac-121">**SECBUFFER\_TARGET\_HOST** \| **SECBUFFER\_READONLY**</span></span>      |
| <span data-ttu-id="f27ac-122">4</span><span class="sxs-lookup"><span data-stu-id="f27ac-122">4</span></span>             | <span data-ttu-id="f27ac-123">Valores de token de enlaces de canal</span><span class="sxs-lookup"><span data-stu-id="f27ac-123">Channel bindings token values</span></span>                                                                                                                        | <span data-ttu-id="f27ac-124">**SECBUFFER \_ \_enlaces de canal** \| **SECBUFFER \_ ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="f27ac-124">**SECBUFFER\_CHANNEL\_BINDINGS** \| **SECBUFFER\_READONLY**</span></span> |



 

<span data-ttu-id="f27ac-125">El búfer cero contiene el desafío de síntesis recibido del servidor en respuesta a la solicitud inicial de un recurso protegido de acceso.</span><span class="sxs-lookup"><span data-stu-id="f27ac-125">Buffer zero contains the Digest challenge received from the server in response to the initial request for an access-protected resource.</span></span>

<span data-ttu-id="f27ac-126">El búfer 1 contiene la representación de cadena del método, como "GET" o "POST".</span><span class="sxs-lookup"><span data-stu-id="f27ac-126">Buffer 1 contains the string representation of the method, such as "GET" or "POST".</span></span> <span data-ttu-id="f27ac-127">El método se usa en el cálculo de a2, tal como se describe en [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span><span class="sxs-lookup"><span data-stu-id="f27ac-127">The method is used in the calculation of A2, as described in [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt).</span></span>

<span data-ttu-id="f27ac-128">Buffer 2 es el hash [*MD5*](../secgloss/m-gly.md) del cuerpo de entidad del mensaje, tal y como se describe en RFC 2617.</span><span class="sxs-lookup"><span data-stu-id="f27ac-128">Buffer 2 is the [*MD5*](../secgloss/m-gly.md) hash of the message's entity-body as described in RFC 2617.</span></span>

<span data-ttu-id="f27ac-129">El búfer 3 contiene el SPN del servidor de destino en formato UTF-8 cuando se utiliza el compendio con enlaces de canal.</span><span class="sxs-lookup"><span data-stu-id="f27ac-129">Buffer 3 contains the SPN of the target server in UTF-8 formatting when Digest is used with channel bindings.</span></span>

<span data-ttu-id="f27ac-130">El búfer 4 contiene el valor del token de enlace del canal cuando se utiliza el compendio con enlaces de canal.</span><span class="sxs-lookup"><span data-stu-id="f27ac-130">Buffer 4 contains the channel binding token value when Digest is used with channel bindings.</span></span>

## <a name="input-buffers-for-sasl"></a><span data-ttu-id="f27ac-131">Búferes de entrada para SASL</span><span class="sxs-lookup"><span data-stu-id="f27ac-131">Input Buffers for SASL</span></span>

<span data-ttu-id="f27ac-132">Proporcione solo el cero en el búfer.</span><span class="sxs-lookup"><span data-stu-id="f27ac-132">Supply buffer zero only.</span></span> <span data-ttu-id="f27ac-133">Por compatibilidad con otros SSP, puede llamar a [**InitializeSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) sin un desafío de servidor válido.</span><span class="sxs-lookup"><span data-stu-id="f27ac-133">For compatibility with other SSPs, you may call [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) without a valid server challenge.</span></span> <span data-ttu-id="f27ac-134">En este caso, el parámetro *pInput* debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="f27ac-134">In this case the *pInput* parameter should be set to **NULL**.</span></span>

 

 

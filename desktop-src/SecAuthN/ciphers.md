---
description: El material siguiente solo es válido cuando se usa Digest como mecanismo SASL. Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.
ms.assetid: 3836b064-241f-4276-af08-557bdc53bb36
title: Ciphers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9637fee72e6f9521968eed432dcd83947a5ddd01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276165"
---
# <a name="ciphers"></a><span data-ttu-id="16857-104">Ciphers</span><span class="sxs-lookup"><span data-stu-id="16857-104">Ciphers</span></span>

<span data-ttu-id="16857-105">El material siguiente solo es válido cuando se usa Digest como mecanismo SASL.</span><span class="sxs-lookup"><span data-stu-id="16857-105">The following material is valid only when Digest is used as a SASL mechanism.</span></span> <span data-ttu-id="16857-106">Los cifrados y el cifrado no están disponibles para la autenticación HTTP mediante Microsoft Digest.</span><span class="sxs-lookup"><span data-stu-id="16857-106">Ciphers and encryption are not available for HTTP authentication using Microsoft Digest.</span></span>

<span data-ttu-id="16857-107">Una directiva de cifrado de un desafío SASL de síntesis contiene una lista de los cifrados admitidos por un servidor que requiere comunicaciones confidenciales.</span><span class="sxs-lookup"><span data-stu-id="16857-107">A Digest SASL challenge's cipher directive contains a list of the ciphers supported by a server that requires confidential communications.</span></span> <span data-ttu-id="16857-108">La Directiva Cipher solo se puede incluir si la Directiva qop se establece en "auth-conf".</span><span class="sxs-lookup"><span data-stu-id="16857-108">The cipher directive can only be included if the qop directive is set to "auth-conf".</span></span> <span data-ttu-id="16857-109">Los cifrados reconocidos por Microsoft Digest se muestran en la siguiente tabla, en orden de mayor a menor.</span><span class="sxs-lookup"><span data-stu-id="16857-109">The ciphers recognized by Microsoft Digest are listed in the following table, in order from strongest to weakest.</span></span>



| <span data-ttu-id="16857-110">Valor de cifrado</span><span class="sxs-lookup"><span data-stu-id="16857-110">Cipher value</span></span> | <span data-ttu-id="16857-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="16857-111">Description</span></span>                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16857-112">RC4</span><span class="sxs-lookup"><span data-stu-id="16857-112">"rc4"</span></span>        | <span data-ttu-id="16857-113">El cifrado RC4 con una clave de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="16857-113">The RC4 cipher with a 128-bit key.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="16857-114">dicha</span><span class="sxs-lookup"><span data-stu-id="16857-114">"3des"</span></span>       | <span data-ttu-id="16857-115">El cifrado [*triple des*](/windows/desktop/SecGloss/t-gly) en el modo [*CBC*](/windows/desktop/SecGloss/c-gly) con Ede con la misma clave para cada fase E (modo de dos claves).</span><span class="sxs-lookup"><span data-stu-id="16857-115">The [*triple DES*](/windows/desktop/SecGloss/t-gly) cipher in [*CBC*](/windows/desktop/SecGloss/c-gly) mode with EDE with the same key for each E stage (two keys mode).</span></span> <span data-ttu-id="16857-116">La longitud total de la clave es de 112 bits.</span><span class="sxs-lookup"><span data-stu-id="16857-116">Total key length is 112 bits.</span></span> |
| <span data-ttu-id="16857-117">"RC4-56"</span><span class="sxs-lookup"><span data-stu-id="16857-117">"rc4-56"</span></span>     | <span data-ttu-id="16857-118">El cifrado RC4 con una clave de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="16857-118">The RC4 cipher with a 56-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="16857-119">"RC4-40"</span><span class="sxs-lookup"><span data-stu-id="16857-119">"rc4-40"</span></span>     | <span data-ttu-id="16857-120">El cifrado RC4 con una clave de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="16857-120">The RC4 cipher with a 40-bit key.</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="16857-121">des</span><span class="sxs-lookup"><span data-stu-id="16857-121">"des"</span></span>        | <span data-ttu-id="16857-122">El cifrado del [*estándar de cifrado de datos*](/windows/desktop/SecGloss/d-gly) (des) en el modo de [*encadenamiento de bloques de cifrado*](/windows/desktop/SecGloss/c-gly) (CBC) con una clave de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="16857-122">The [*Data Encryption Standard*](/windows/desktop/SecGloss/d-gly) (DES) cipher in [*cipher block chaining*](/windows/desktop/SecGloss/c-gly) (CBC) mode with a 56-bit key.</span></span> |



 

<span data-ttu-id="16857-123">Cuando una aplicación de servidor solicita confidencialidad (qop = "auth-conf") Microsoft Digest generará un desafío que ofrece al cliente todos los cifrados instalados en el servidor y que es compatible con el resumen.</span><span class="sxs-lookup"><span data-stu-id="16857-123">When a server application requests confidentiality (qop="auth-conf") Microsoft Digest will generate a challenge that offers the client all of the ciphers installed on the server and supported by Digest.</span></span> <span data-ttu-id="16857-124">El cliente de síntesis seleccionará el cifrado más seguro disponible.</span><span class="sxs-lookup"><span data-stu-id="16857-124">The Digest client will select the strongest available cipher.</span></span> <span data-ttu-id="16857-125">Para obtener más información sobre cómo especificar la confidencialidad, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="16857-125">For details on specifying confidentiality, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 

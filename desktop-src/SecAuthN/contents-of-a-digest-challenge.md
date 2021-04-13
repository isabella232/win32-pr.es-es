---
description: El tamaño de un desafío de acceso implícita debe ser inferior a 2048 bytes.
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: Contenido de un desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153845"
---
# <a name="contents-of-a-digest-challenge"></a><span data-ttu-id="d65bd-103">Contenido de un desafío de síntesis</span><span class="sxs-lookup"><span data-stu-id="d65bd-103">Contents of a Digest Challenge</span></span>

<span data-ttu-id="d65bd-104">El tamaño de un desafío de acceso implícita debe ser inferior a 2048 bytes.</span><span class="sxs-lookup"><span data-stu-id="d65bd-104">The size of a Digest Access challenge must be less than 2048 bytes.</span></span> <span data-ttu-id="d65bd-105">En el ejemplo siguiente se muestra un desafío asignado a la cadena de caracteres szChallenge.</span><span class="sxs-lookup"><span data-stu-id="d65bd-105">The following example shows a challenge assigned to the character string szChallenge.</span></span>


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> <span data-ttu-id="d65bd-106">La cadena de desafío está entre comillas dobles y contiene comillas dobles incrustadas.</span><span class="sxs-lookup"><span data-stu-id="d65bd-106">The challenge string is enclosed in double quotes and contains embedded double quotes.</span></span> <span data-ttu-id="d65bd-107">Las comillas dobles incrustadas deben ir precedidas de una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="d65bd-107">Embedded double quotes must be preceded (escaped) with a backslash (\\).</span></span>

 

<span data-ttu-id="d65bd-108">Un desafío de síntesis puede contener las siguientes directivas.</span><span class="sxs-lookup"><span data-stu-id="d65bd-108">A Digest challenge can contain the following directives.</span></span>



| <span data-ttu-id="d65bd-109">Directiva</span><span class="sxs-lookup"><span data-stu-id="d65bd-109">Directive</span></span>         | <span data-ttu-id="d65bd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d65bd-110">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d65bd-111">realm</span><span class="sxs-lookup"><span data-stu-id="d65bd-111">realm</span></span>             | <span data-ttu-id="d65bd-112">Una sugerencia definida por la implementación al cliente sobre qué [*credenciales*](/windows/desktop/SecGloss/c-gly) se requieren.</span><span class="sxs-lookup"><span data-stu-id="d65bd-112">An implementation-defined hint to the client about which [*credentials*](/windows/desktop/SecGloss/c-gly) are required.</span></span> <span data-ttu-id="d65bd-113">El cliente debe mostrar esta información al usuario si solicita las credenciales.</span><span class="sxs-lookup"><span data-stu-id="d65bd-113">The client should display this information to the user if it is prompting for credentials.</span></span>                                                  |
| <span data-ttu-id="d65bd-114">algoritmo</span><span class="sxs-lookup"><span data-stu-id="d65bd-114">algorithm</span></span>         | <span data-ttu-id="d65bd-115">Microsoft Digest admite MD5 y MD5-SESS.</span><span class="sxs-lookup"><span data-stu-id="d65bd-115">Microsoft Digest supports MD5 and MD5-Sess.</span></span> <span data-ttu-id="d65bd-116">Para obtener un rendimiento óptimo, use MD5-SESS.</span><span class="sxs-lookup"><span data-stu-id="d65bd-116">For optimal performance, use MD5-Sess.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="d65bd-117">qop</span><span class="sxs-lookup"><span data-stu-id="d65bd-117">qop</span></span>               | <span data-ttu-id="d65bd-118">Esta Directiva se puede establecer en auth, auth-int o auth-conf.</span><span class="sxs-lookup"><span data-stu-id="d65bd-118">This directive can be set to auth, auth-int, or auth-conf.</span></span> <span data-ttu-id="d65bd-119">Para obtener más información, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="d65bd-119">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="d65bd-120">valor de seguridad</span><span class="sxs-lookup"><span data-stu-id="d65bd-120">nonce</span></span>             | <span data-ttu-id="d65bd-121">Valor codificado único generado por el servidor para cada desafío.</span><span class="sxs-lookup"><span data-stu-id="d65bd-121">A unique encoded value generated by the server for each challenge.</span></span> <span data-ttu-id="d65bd-122">El cliente no debe modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="d65bd-122">This value must not be altered by the client.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d65bd-123">opaco</span><span class="sxs-lookup"><span data-stu-id="d65bd-123">opaque</span></span>            | <span data-ttu-id="d65bd-124">Contiene una referencia para el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) que se está estableciendo.</span><span class="sxs-lookup"><span data-stu-id="d65bd-124">Contains a reference for the [*security context*](/windows/desktop/SecGloss/s-gly) that is being established.</span></span> <span data-ttu-id="d65bd-125">Para obtener más información, vea [mantener el contexto de seguridad entre conexiones](maintaining-the-security-context-between-connections.md).</span><span class="sxs-lookup"><span data-stu-id="d65bd-125">For more information, see [Maintaining the Security Context Between Connections](maintaining-the-security-context-between-connections.md).</span></span> |
| <span data-ttu-id="d65bd-126">Cipher (solo SASL)</span><span class="sxs-lookup"><span data-stu-id="d65bd-126">cipher(SASL only)</span></span> | <span data-ttu-id="d65bd-127">La lista de cifrados que admite el servidor.</span><span class="sxs-lookup"><span data-stu-id="d65bd-127">The list of ciphers that the server supports.</span></span> <span data-ttu-id="d65bd-128">Este elemento puede estar presente en un desafío de SASL implícito solo si la Directiva qop especifica auth-conf.</span><span class="sxs-lookup"><span data-stu-id="d65bd-128">This element can be present in a Digest SASL challenge only if the qop directive specifies auth-conf.</span></span> <span data-ttu-id="d65bd-129">Para obtener más información, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).</span><span class="sxs-lookup"><span data-stu-id="d65bd-129">For more information, see [Quality of Protection and Ciphers](quality-of-protection-and-ciphers.md).</span></span>                                              |
| <span data-ttu-id="d65bd-130">charset</span><span class="sxs-lookup"><span data-stu-id="d65bd-130">charset</span></span>           | <span data-ttu-id="d65bd-131">Esta Directiva se puede establecer en UTF-8 Si el servidor puede procesar nombres de usuario y territorios codificados en UTF-8.</span><span class="sxs-lookup"><span data-stu-id="d65bd-131">This directive can be set to utf-8 if the server can process UTF-8–encoded user names and realms.</span></span> <span data-ttu-id="d65bd-132">Si el cliente entiende la Directiva charset, puede responder mediante valores con codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="d65bd-132">If the client understands the charset directive, it can respond by using UTF-8–encoded values.</span></span>                                                                                                       |



 

<span data-ttu-id="d65bd-133">Microsoft Digest genera la cadena de desafío de síntesis para las aplicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="d65bd-133">Microsoft Digest generates the Digest challenge string for server applications.</span></span> <span data-ttu-id="d65bd-134">Para obtener más información, consulte [generación del desafío de síntesis](generating-the-digest-challenge.md).</span><span class="sxs-lookup"><span data-stu-id="d65bd-134">For details, see [Generating the Digest Challenge](generating-the-digest-challenge.md).</span></span>

 

 

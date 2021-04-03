---
description: Admite tanto firmas digitales como cifrado de datos. Se considera un proveedor de servicios criptográficos (CSP) de uso general.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083080"
---
# <a name="prov_rsa_aes"></a><span data-ttu-id="7ae7a-104">\_AES de RSA \_</span><span class="sxs-lookup"><span data-stu-id="7ae7a-104">PROV\_RSA\_AES</span></span>

<span data-ttu-id="7ae7a-105">El \_ tipo de proveedor de RSA AES de Prov \_ es compatible con las [firmas digitales](digital-signatures.md) y el cifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-105">The PROV\_RSA\_AES provider type supports both [digital signatures](digital-signatures.md) and data encryption.</span></span> <span data-ttu-id="7ae7a-106">Se considera un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de uso general.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-106">It is considered a general purpose [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="7ae7a-107">El [*algoritmo de clave pública*](../secgloss/p-gly.md) RSA se utiliza para todas las operaciones de [*clave pública*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="7ae7a-107">The RSA [*public key algorithm*](../secgloss/p-gly.md) is used for all [*public key*](../secgloss/p-gly.md) operations.</span></span>

## <a name="algorithms-supported"></a><span data-ttu-id="7ae7a-108">Algoritmos admitidos</span><span class="sxs-lookup"><span data-stu-id="7ae7a-108">Algorithms Supported</span></span>

<span data-ttu-id="7ae7a-109">Para obtener descripciones de cada uno de estos algoritmos, vea el glosario.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-109">For descriptions of each of these algorithms, see the glossary.</span></span>



| <span data-ttu-id="7ae7a-110">Propósito</span><span class="sxs-lookup"><span data-stu-id="7ae7a-110">Purpose</span></span>      | <span data-ttu-id="7ae7a-111">Algoritmos admitidos</span><span class="sxs-lookup"><span data-stu-id="7ae7a-111">Supported algorithms</span></span>                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae7a-112">Intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="7ae7a-112">Key Exchange</span></span> | [<span data-ttu-id="7ae7a-113">*RSA*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-113">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="7ae7a-114">Firma</span><span class="sxs-lookup"><span data-stu-id="7ae7a-114">Signature</span></span>    | [<span data-ttu-id="7ae7a-115">*RSA*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-115">*RSA*</span></span>](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="7ae7a-116">Cifrado</span><span class="sxs-lookup"><span data-stu-id="7ae7a-116">Encryption</span></span>   | [<span data-ttu-id="7ae7a-117">*RC2*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-117">*RC2*</span></span>](../secgloss/r-gly.md)<br/> [<span data-ttu-id="7ae7a-118">*RC4*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-118">*RC4*</span></span>](../secgloss/r-gly.md)<br/> <span data-ttu-id="7ae7a-119">[*Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES)</span><span class="sxs-lookup"><span data-stu-id="7ae7a-119">[*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES)</span></span> <br/>                                                       |
| <span data-ttu-id="7ae7a-120">Aplicación de algoritmo hash</span><span class="sxs-lookup"><span data-stu-id="7ae7a-120">Hashing</span></span>      | [<span data-ttu-id="7ae7a-121">*MD2*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-121">*MD2*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="7ae7a-122">*MD4*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-122">*MD4*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="7ae7a-123">*MD5*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-123">*MD5*</span></span>](../secgloss/m-gly.md)<br/> [<span data-ttu-id="7ae7a-124">*SHA-1*</span><span class="sxs-lookup"><span data-stu-id="7ae7a-124">*SHA-1*</span></span>](../secgloss/s-gly.md)<br/> <span data-ttu-id="7ae7a-125">SHA-2 (SHA-256, SHA-384 y SHA-512)</span><span class="sxs-lookup"><span data-stu-id="7ae7a-125">SHA-2 (SHA-256, SHA-384, and SHA-512)</span></span><br/> |



 

## <a name="related-documentation"></a><span data-ttu-id="7ae7a-126">Documentación relacionada</span><span class="sxs-lookup"><span data-stu-id="7ae7a-126">Related Documentation</span></span>

<span data-ttu-id="7ae7a-127">Este tipo de proveedor está definido por Microsoft y RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-127">This provider type is defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="7ae7a-128">Se describe en los siguientes documentos:</span><span class="sxs-lookup"><span data-stu-id="7ae7a-128">It is described in the following documents:</span></span>

-   <span data-ttu-id="7ae7a-129">*Guía del programador del proveedor de servicios criptográficos de Microsoft*, microsoft, 1996.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-129">*Microsoft Cryptographic Service Provider Programmer's Guide*, Microsoft, 1996.</span></span>
-   <span data-ttu-id="7ae7a-130">RSA Laboratories, estándares de criptografía de clave pública, RSA Data Security, noviembre de 1993.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-130">RSA Laboratories, Public Key Cryptography Standards, RSA Data Security, November 1993.</span></span>

> [!Note]  
> <span data-ttu-id="7ae7a-131">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="7ae7a-131">These resources may not be available in some languages and countries or regions.</span></span>

 

 

 

---
description: Los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios. Los proveedores se pueden implementar en hardware, software o ambos.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Descripción de los proveedores de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002524"
---
# <a name="understanding-cryptographic-providers"></a><span data-ttu-id="cbd6b-104">Descripción de los proveedores de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="cbd6b-104">Understanding Cryptographic Providers</span></span>

<span data-ttu-id="cbd6b-105">El concepto de proveedor de servicios criptográficos que se presentó en Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) y que evolucionó en cierto modo en [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) es fundamental para la implementación segura de la funcionalidad criptográfica en los sistemas operativos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-105">The cryptographic provider concept that was introduced in Cryptography API ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) and which evolved somewhat in [*Cryptography API: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) is central to the secure implementation of cryptographic functionality on Microsoft operating systems.</span></span> <span data-ttu-id="cbd6b-106">Estos dos SDK se han usado para crear muchas aplicaciones y otros SDK las llaman internamente.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-106">These two SDKs have been used to create many applications and are called internally by other SDKs.</span></span> <span data-ttu-id="cbd6b-107">Por ejemplo, Active Directory servicios de Certificate Server y la API de inscripción de certificados se basan en CryptoAPI y CNG.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-107">For example, Active Directory Certificate Services and the Certificate Enrollment API rely on CryptoAPI and CNG.</span></span>

<span data-ttu-id="cbd6b-108">En general, los proveedores implementan algoritmos criptográficos, generan claves, proporcionan almacenamiento de claves y autentican a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-108">In general, providers implement cryptographic algorithms, generate keys, provide key storage, and authenticate users.</span></span> <span data-ttu-id="cbd6b-109">Los proveedores se pueden implementar en hardware, software o ambos.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-109">Providers can be implemented in hardware, software, or both.</span></span> <span data-ttu-id="cbd6b-110">Las aplicaciones compiladas con CryptoAPI o CNG no pueden modificar las claves creadas por los proveedores y no pueden modificar la implementación de algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-110">Applications built by using CryptoAPI or CNG cannot alter the keys created by providers, and they cannot alter cryptographic algorithm implementation.</span></span> <span data-ttu-id="cbd6b-111">Los diversos proveedores creados por Microsoft se distribuyen con los sistemas operativos.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-111">The multiple providers created by Microsoft are distributed with the operating systems.</span></span> <span data-ttu-id="cbd6b-112">Otros proveedores se han creado y distribuido por terceros.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-112">Other providers have been created and distributed by third parties.</span></span>

<span data-ttu-id="cbd6b-113">En los temas siguientes se resaltan las diferencias entre los proveedores asociados con CryptoAPI y los asociados a CNG.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-113">The following topics highlight the differences between providers associated with CryptoAPI and those associated with CNG.</span></span> <span data-ttu-id="cbd6b-114">Normalmente, esta documentación hace referencia a los proveedores sin referencia al SDK con el que están asociados, anotando la Asociación solo cuando es relevante.</span><span class="sxs-lookup"><span data-stu-id="cbd6b-114">Typically, this documentation refers to providers without reference to the SDK with which they are associated, noting the association only when it is relevant.</span></span>

-   [<span data-ttu-id="cbd6b-115">Proveedores de servicios criptográficos de CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="cbd6b-115">CryptoAPI Cryptographic Service Providers</span></span>](cryptoapi-cryptographic-service-providers.md)
-   [<span data-ttu-id="cbd6b-116">Proveedores de algoritmos criptográficos CNG</span><span class="sxs-lookup"><span data-stu-id="cbd6b-116">CNG Cryptographic Algorithm Providers</span></span>](cng-cryptographic-algorithm-providers.md)
-   [<span data-ttu-id="cbd6b-117">Proveedores de almacenamiento de claves CNG</span><span class="sxs-lookup"><span data-stu-id="cbd6b-117">CNG Key Storage Providers</span></span>](cng-key-storage-providers.md)
-   [<span data-ttu-id="cbd6b-118">Enumerar los proveedores instalados</span><span class="sxs-lookup"><span data-stu-id="cbd6b-118">Enumerating Installed Providers</span></span>](enumerating-installed-providers.md)

## <a name="related-topics"></a><span data-ttu-id="cbd6b-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbd6b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd6b-120">Uso de la API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="cbd6b-120">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 

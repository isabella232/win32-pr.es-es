---
description: Devuelve la colección EKU para el certificado.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: ExtendedKeyUsage. EKU (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670349"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="94973-103">ExtendedKeyUsage. EKU (propiedad)</span><span class="sxs-lookup"><span data-stu-id="94973-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="94973-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="94973-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="94973-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="94973-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="94973-106">La propiedad **EKU** devuelve la colección [**EKU**](ekus.md) para el certificado.</span><span class="sxs-lookup"><span data-stu-id="94973-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="94973-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94973-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="94973-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="94973-108">Property value</span></span>

<span data-ttu-id="94973-109">La colección [**EKU**](ekus.md) que contiene los objetos [**EKU**](eku.md) para el certificado.</span><span class="sxs-lookup"><span data-stu-id="94973-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="94973-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94973-110">Requirements</span></span>



| <span data-ttu-id="94973-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="94973-111">Requirement</span></span> | <span data-ttu-id="94973-112">Value</span><span class="sxs-lookup"><span data-stu-id="94973-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94973-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="94973-113">End of client support</span></span><br/> | <span data-ttu-id="94973-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94973-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="94973-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="94973-115">End of server support</span></span><br/> | <span data-ttu-id="94973-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94973-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="94973-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="94973-117">Redistributable</span></span><br/>       | <span data-ttu-id="94973-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="94973-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="94973-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94973-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="94973-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94973-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94973-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="94973-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94973-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="94973-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 

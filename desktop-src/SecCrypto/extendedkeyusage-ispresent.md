---
description: Devuelve un valor booleano que indica si la extensión EKU está presente. Esta es la propiedad predeterminada.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: Propiedad ExtendedKeyUsage. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671199"
---
# <a name="extendedkeyusageispresent-property"></a><span data-ttu-id="22607-104">Propiedad ExtendedKeyUsage. IsPresent</span><span class="sxs-lookup"><span data-stu-id="22607-104">ExtendedKeyUsage.IsPresent property</span></span>

<span data-ttu-id="22607-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22607-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="22607-106">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="22607-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="22607-107">La propiedad **IsPresent** devuelve un valor booleano que indica si la extensión EKU está presente.</span><span class="sxs-lookup"><span data-stu-id="22607-107">The **IsPresent** property returns a Boolean value that indicates whether the EKU extension is present.</span></span> <span data-ttu-id="22607-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="22607-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="22607-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22607-109">Syntax</span></span>


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="22607-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="22607-110">Property value</span></span>

<span data-ttu-id="22607-111">Si es **true**, la extensión EKU está presente.</span><span class="sxs-lookup"><span data-stu-id="22607-111">If **true**, the EKU extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="22607-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22607-112">Requirements</span></span>



| <span data-ttu-id="22607-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="22607-113">Requirement</span></span> | <span data-ttu-id="22607-114">Value</span><span class="sxs-lookup"><span data-stu-id="22607-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22607-115">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="22607-115">End of client support</span></span><br/> | <span data-ttu-id="22607-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22607-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="22607-117">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="22607-117">End of server support</span></span><br/> | <span data-ttu-id="22607-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22607-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="22607-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="22607-119">Redistributable</span></span><br/>       | <span data-ttu-id="22607-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="22607-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="22607-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22607-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="22607-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22607-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22607-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="22607-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22607-124">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="22607-124">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 

---
description: Devuelve un valor booleano que indica si la extensión EKU está marcada como crítica.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Propiedad ExtendedKeyUsage. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649693"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="a2982-103">Propiedad ExtendedKeyUsage. IsCritical</span><span class="sxs-lookup"><span data-stu-id="a2982-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="a2982-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a2982-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a2982-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a2982-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a2982-106">La propiedad **IsCritical** devuelve un valor booleano que indica si la extensión EKU está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="a2982-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2982-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2982-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a2982-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2982-108">Property value</span></span>

<span data-ttu-id="a2982-109">Si es **true**, la extensión EKU se marca como crítica.</span><span class="sxs-lookup"><span data-stu-id="a2982-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2982-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2982-110">Requirements</span></span>



| <span data-ttu-id="a2982-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2982-111">Requirement</span></span> | <span data-ttu-id="a2982-112">Value</span><span class="sxs-lookup"><span data-stu-id="a2982-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2982-113">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a2982-113">End of client support</span></span><br/> | <span data-ttu-id="a2982-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2982-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a2982-115">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a2982-115">End of server support</span></span><br/> | <span data-ttu-id="a2982-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2982-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a2982-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a2982-117">Redistributable</span></span><br/>       | <span data-ttu-id="a2982-118">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2982-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a2982-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2982-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a2982-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2982-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2982-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2982-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2982-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="a2982-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 

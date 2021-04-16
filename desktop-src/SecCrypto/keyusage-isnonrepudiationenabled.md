---
description: Recupera un valor booleano que indica si se ha establecido el bit nonRepudiationEnabled.
ms.assetid: d9bcf0fc-8b2d-408c-b587-71903ef5f5f6
title: Propiedad KeyUsage. IsNonRepudiationEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsNonRepudiationEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 30e0a532cd39f2150591a3eb74ed9bbba83a7080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670290"
---
# <a name="keyusageisnonrepudiationenabled-property"></a><span data-ttu-id="bb6ba-103">Propiedad KeyUsage. IsNonRepudiationEnabled</span><span class="sxs-lookup"><span data-stu-id="bb6ba-103">KeyUsage.IsNonRepudiationEnabled property</span></span>

<span data-ttu-id="bb6ba-104">\[La propiedad **IsNonRepudiationEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bb6ba-104">\[The **IsNonRepudiationEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb6ba-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bb6ba-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bb6ba-106">La propiedad **IsNonRepudiationEnabled** recupera un valor booleano que indica si se ha establecido el bit nonRepudiationEnabled.</span><span class="sxs-lookup"><span data-stu-id="bb6ba-106">The **IsNonRepudiationEnabled** property retrieves a Boolean value that indicates whether the nonRepudiationEnabled bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6ba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb6ba-107">Syntax</span></span>


```VB
KeyUsage.IsNonRepudiationEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bb6ba-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bb6ba-108">Property value</span></span>

<span data-ttu-id="bb6ba-109">Si es **true**, se establece el bit nonRepudiationEnabled.</span><span class="sxs-lookup"><span data-stu-id="bb6ba-109">If **true**, the nonRepudiationEnabled bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6ba-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb6ba-110">Requirements</span></span>



| <span data-ttu-id="bb6ba-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb6ba-111">Requirement</span></span> | <span data-ttu-id="bb6ba-112">Value</span><span class="sxs-lookup"><span data-stu-id="bb6ba-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6ba-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bb6ba-113">Redistributable</span></span><br/> | <span data-ttu-id="bb6ba-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb6ba-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb6ba-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb6ba-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bb6ba-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6ba-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb6ba-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb6ba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6ba-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="bb6ba-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

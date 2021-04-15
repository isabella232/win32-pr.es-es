---
description: Recupera un valor booleano que indica si se ha establecido el bit encipherOnly.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: Propiedad KeyUsage. IsEncipherOnlyEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689919"
---
# <a name="keyusageisencipheronlyenabled-property"></a><span data-ttu-id="e8b25-103">Propiedad KeyUsage. IsEncipherOnlyEnabled</span><span class="sxs-lookup"><span data-stu-id="e8b25-103">KeyUsage.IsEncipherOnlyEnabled property</span></span>

<span data-ttu-id="e8b25-104">\[La propiedad **IsEncipherOnlyEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e8b25-104">\[The **IsEncipherOnlyEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e8b25-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e8b25-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e8b25-106">La propiedad **IsEncipherOnlyEnabled** recupera un valor booleano que indica si se ha establecido el bit encipherOnly.</span><span class="sxs-lookup"><span data-stu-id="e8b25-106">The **IsEncipherOnlyEnabled** property retrieves a Boolean value that indicates whether the encipherOnly bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b25-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8b25-107">Syntax</span></span>


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e8b25-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8b25-108">Property value</span></span>

<span data-ttu-id="e8b25-109">Si es **true**, se establece el bit encipherOnly.</span><span class="sxs-lookup"><span data-stu-id="e8b25-109">If **true**, the encipherOnly bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b25-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8b25-110">Requirements</span></span>



| <span data-ttu-id="e8b25-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b25-111">Requirement</span></span> | <span data-ttu-id="e8b25-112">Value</span><span class="sxs-lookup"><span data-stu-id="e8b25-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b25-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="e8b25-113">Redistributable</span></span><br/> | <span data-ttu-id="e8b25-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8b25-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e8b25-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8b25-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e8b25-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8b25-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b25-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8b25-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b25-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="e8b25-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

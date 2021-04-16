---
description: Recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.
ms.assetid: f7d53570-2b89-40a9-ab56-fcae4e4cb70c
title: Propiedad KeyUsage. IsCritical
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b1829da9c9ddbcf5261f4cc595b72b8596193078
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689922"
---
# <a name="keyusageiscritical-property"></a><span data-ttu-id="f8907-103">Propiedad KeyUsage. IsCritical</span><span class="sxs-lookup"><span data-stu-id="f8907-103">KeyUsage.IsCritical property</span></span>

<span data-ttu-id="f8907-104">\[La propiedad **IsCritical** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f8907-104">\[The **IsCritical** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f8907-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f8907-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f8907-106">La propiedad **IsCritical** recupera un valor booleano que indica si la extensión KeyUsage está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="f8907-106">The **IsCritical** property retrieves a Boolean value that indicates whether the KeyUsage extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8907-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8907-107">Syntax</span></span>


```VB
KeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f8907-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f8907-108">Property value</span></span>

<span data-ttu-id="f8907-109">Si es **true**, la extensión KeyUsage se marca como crítica.</span><span class="sxs-lookup"><span data-stu-id="f8907-109">If **true**, the KeyUsage extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8907-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8907-110">Requirements</span></span>



| <span data-ttu-id="f8907-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8907-111">Requirement</span></span> | <span data-ttu-id="f8907-112">Value</span><span class="sxs-lookup"><span data-stu-id="f8907-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8907-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f8907-113">Redistributable</span></span><br/> | <span data-ttu-id="f8907-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8907-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f8907-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8907-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="f8907-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8907-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8907-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8907-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8907-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="f8907-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

---
description: Recupera un valor booleano que indica si se ha establecido el bit dataEncipherment.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Propiedad KeyUsage. IsDataEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689921"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="301fb-103">Propiedad KeyUsage. IsDataEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="301fb-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="301fb-104">\[La propiedad **IsDataEnciphermentEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="301fb-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="301fb-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="301fb-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="301fb-106">La propiedad **IsDataEnciphermentEnabled** recupera un valor booleano que indica si se ha establecido el bit dataEncipherment.</span><span class="sxs-lookup"><span data-stu-id="301fb-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="301fb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="301fb-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="301fb-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="301fb-108">Property value</span></span>

<span data-ttu-id="301fb-109">Si es **true**, se establece el bit dataEncipherment.</span><span class="sxs-lookup"><span data-stu-id="301fb-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="301fb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="301fb-110">Requirements</span></span>



| <span data-ttu-id="301fb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="301fb-111">Requirement</span></span> | <span data-ttu-id="301fb-112">Value</span><span class="sxs-lookup"><span data-stu-id="301fb-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="301fb-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="301fb-113">Redistributable</span></span><br/> | <span data-ttu-id="301fb-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="301fb-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="301fb-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="301fb-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="301fb-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="301fb-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="301fb-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="301fb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301fb-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="301fb-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

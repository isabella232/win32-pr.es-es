---
description: Recupera un valor booleano que indica si se ha establecido el bit bit keycertsign.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Propiedad KeyUsage. IsKeyCertSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689911"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="f3eff-103">Propiedad KeyUsage. IsKeyCertSignEnabled</span><span class="sxs-lookup"><span data-stu-id="f3eff-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="f3eff-104">\[La propiedad **IsKeyCertSignEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f3eff-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3eff-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f3eff-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f3eff-106">La propiedad **IsKeyCertSignEnabled** recupera un valor booleano que indica si se ha establecido el bit bit keycertsign.</span><span class="sxs-lookup"><span data-stu-id="f3eff-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3eff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3eff-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f3eff-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f3eff-108">Property value</span></span>

<span data-ttu-id="f3eff-109">Si es **true**, se establece el bit bit keycertsign.</span><span class="sxs-lookup"><span data-stu-id="f3eff-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eff-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eff-110">Requirements</span></span>



| <span data-ttu-id="f3eff-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eff-111">Requirement</span></span> | <span data-ttu-id="f3eff-112">Value</span><span class="sxs-lookup"><span data-stu-id="f3eff-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eff-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f3eff-113">Redistributable</span></span><br/> | <span data-ttu-id="f3eff-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3eff-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f3eff-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3eff-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="f3eff-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3eff-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3eff-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3eff-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eff-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="f3eff-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

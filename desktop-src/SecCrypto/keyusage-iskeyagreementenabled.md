---
description: Recupera un valor booleano que indica si se ha establecido el bit keyAgreement.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: Propiedad KeyUsage. IsKeyAgreementEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689917"
---
# <a name="keyusageiskeyagreementenabled-property"></a><span data-ttu-id="b0b5b-103">Propiedad KeyUsage. IsKeyAgreementEnabled</span><span class="sxs-lookup"><span data-stu-id="b0b5b-103">KeyUsage.IsKeyAgreementEnabled property</span></span>

<span data-ttu-id="b0b5b-104">\[La propiedad **IsKeyAgreementEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-104">\[The **IsKeyAgreementEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b0b5b-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b0b5b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b0b5b-106">La propiedad **IsKeyAgreementEnabled** recupera un valor booleano que indica si se ha establecido el bit keyAgreement.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-106">The **IsKeyAgreementEnabled** property retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b5b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0b5b-107">Syntax</span></span>


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b0b5b-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b0b5b-108">Property value</span></span>

<span data-ttu-id="b0b5b-109">Si es **true**, se establece el bit keyAgreement.</span><span class="sxs-lookup"><span data-stu-id="b0b5b-109">If **true**, the keyAgreement bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b5b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b5b-110">Requirements</span></span>



| <span data-ttu-id="b0b5b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b5b-111">Requirement</span></span> | <span data-ttu-id="b0b5b-112">Value</span><span class="sxs-lookup"><span data-stu-id="b0b5b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b5b-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b0b5b-113">Redistributable</span></span><br/> | <span data-ttu-id="b0b5b-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b0b5b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b0b5b-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0b5b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="b0b5b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0b5b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b5b-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0b5b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b5b-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="b0b5b-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

---
description: Recupera un valor booleano que indica si se ha establecido el bit digitalSignature.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: Propiedad KeyUsage. IsDigitalSignatureEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689920"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="9f84d-103">Propiedad KeyUsage. IsDigitalSignatureEnabled</span><span class="sxs-lookup"><span data-stu-id="9f84d-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="9f84d-104">\[La propiedad **IsDigitalSignatureEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="9f84d-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9f84d-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9f84d-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9f84d-106">La propiedad **IsDigitalSignatureEnabled** recupera un valor booleano que indica si se ha establecido el bit digitalSignature.</span><span class="sxs-lookup"><span data-stu-id="9f84d-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f84d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f84d-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="9f84d-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9f84d-108">Property value</span></span>

<span data-ttu-id="9f84d-109">Si es **true**, se establece el bit digitalSignature.</span><span class="sxs-lookup"><span data-stu-id="9f84d-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f84d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f84d-110">Requirements</span></span>



| <span data-ttu-id="9f84d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f84d-111">Requirement</span></span> | <span data-ttu-id="9f84d-112">Value</span><span class="sxs-lookup"><span data-stu-id="9f84d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f84d-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9f84d-113">Redistributable</span></span><br/> | <span data-ttu-id="9f84d-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f84d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9f84d-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f84d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="9f84d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f84d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f84d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f84d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f84d-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="9f84d-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

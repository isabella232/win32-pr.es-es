---
description: Recupera un valor booleano que indica si se ha establecido el bit bit crlsign.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: Propiedad KeyUsage. IsCRLSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39bd8509ebc89719e5d06e5e60a300ec2cd9949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670296"
---
# <a name="keyusageiscrlsignenabled-property"></a><span data-ttu-id="3c004-103">Propiedad KeyUsage. IsCRLSignEnabled</span><span class="sxs-lookup"><span data-stu-id="3c004-103">KeyUsage.IsCRLSignEnabled property</span></span>

<span data-ttu-id="3c004-104">\[La propiedad **IsCRLSignEnabled** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3c004-104">\[The **IsCRLSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3c004-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3c004-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3c004-106">La propiedad **IsCRLSignEnabled** recupera un valor booleano que indica si se ha establecido el bit bit crlsign.</span><span class="sxs-lookup"><span data-stu-id="3c004-106">The **IsCRLSignEnabled** property retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c004-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c004-107">Syntax</span></span>


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="3c004-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c004-108">Property value</span></span>

<span data-ttu-id="3c004-109">Si es **true**, se establece el bit bit crlsign.</span><span class="sxs-lookup"><span data-stu-id="3c004-109">If **true**, the CRLSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c004-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c004-110">Requirements</span></span>



| <span data-ttu-id="3c004-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c004-111">Requirement</span></span> | <span data-ttu-id="3c004-112">Value</span><span class="sxs-lookup"><span data-stu-id="3c004-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c004-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3c004-113">Redistributable</span></span><br/> | <span data-ttu-id="3c004-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c004-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3c004-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c004-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="3c004-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c004-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c004-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c004-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c004-118">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="3c004-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 

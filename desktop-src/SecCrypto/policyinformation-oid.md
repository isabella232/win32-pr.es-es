---
description: Recupera el OID de la Directiva. Esta es la propiedad predeterminada.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: Propiedad PolicyInformation. OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690025"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="6d4ba-104">Propiedad PolicyInformation. OID</span><span class="sxs-lookup"><span data-stu-id="6d4ba-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="6d4ba-105">\[La propiedad **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6d4ba-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d4ba-106">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="6d4ba-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="6d4ba-107">La propiedad **OID** recupera el OID de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="6d4ba-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="6d4ba-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6d4ba-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4ba-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d4ba-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="6d4ba-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6d4ba-110">Property value</span></span>

<span data-ttu-id="6d4ba-111">Identificador de objeto de la Directiva como un objeto [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="6d4ba-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4ba-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d4ba-112">Requirements</span></span>



| <span data-ttu-id="6d4ba-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d4ba-113">Requirement</span></span> | <span data-ttu-id="6d4ba-114">Value</span><span class="sxs-lookup"><span data-stu-id="6d4ba-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4ba-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="6d4ba-115">Redistributable</span></span><br/> | <span data-ttu-id="6d4ba-116">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="6d4ba-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d4ba-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d4ba-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="6d4ba-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d4ba-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d4ba-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d4ba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4ba-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="6d4ba-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 

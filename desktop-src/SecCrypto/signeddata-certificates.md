---
description: Recupera la colección de certificados asociada al objeto SignedData. Después de recuperarse, se pueden enumerar los objetos de certificado individuales de la colección.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Propiedad SignedData. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670817"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="5ed62-104">Propiedad SignedData. Certificates</span><span class="sxs-lookup"><span data-stu-id="5ed62-104">SignedData.Certificates property</span></span>

<span data-ttu-id="5ed62-105">\[La propiedad **certificados** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="5ed62-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5ed62-106">En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="5ed62-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5ed62-107">La propiedad **Certificates** recupera la colección de [**certificados**](certificates.md) asociada al objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed62-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="5ed62-108">Después de recuperarse, se pueden enumerar los objetos de [**certificado**](certificate.md) individuales de la colección.</span><span class="sxs-lookup"><span data-stu-id="5ed62-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed62-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ed62-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="5ed62-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ed62-110">Property value</span></span>

<span data-ttu-id="5ed62-111">Colección de [**certificados**](certificates.md) que está asociada al objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="5ed62-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed62-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ed62-112">Requirements</span></span>



| <span data-ttu-id="5ed62-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed62-113">Requirement</span></span> | <span data-ttu-id="5ed62-114">Value</span><span class="sxs-lookup"><span data-stu-id="5ed62-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed62-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5ed62-115">Redistributable</span></span><br/> | <span data-ttu-id="5ed62-116">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5ed62-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5ed62-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ed62-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="5ed62-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ed62-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed62-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ed62-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed62-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="5ed62-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 

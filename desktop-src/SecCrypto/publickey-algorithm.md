---
description: La propiedad Algorithm recupera el objeto OID que identifica el algoritmo utilizado por la clave pública. Esta es la propiedad predeterminada.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. algorithm (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671054"
---
# <a name="publickeyalgorithm-property"></a><span data-ttu-id="bed55-104">PublicKey. algorithm (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bed55-104">PublicKey.Algorithm property</span></span>

<span data-ttu-id="bed55-105">\[La propiedad **algorithm** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="bed55-105">\[The **Algorithm** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bed55-106">En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bed55-106">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bed55-107">La propiedad **algorithm** recupera el objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública.</span><span class="sxs-lookup"><span data-stu-id="bed55-107">The **Algorithm** property retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="bed55-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bed55-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed55-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bed55-109">Syntax</span></span>


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a><span data-ttu-id="bed55-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bed55-110">Property value</span></span>

<span data-ttu-id="bed55-111">Objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública.</span><span class="sxs-lookup"><span data-stu-id="bed55-111">The [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed55-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bed55-112">Requirements</span></span>



| <span data-ttu-id="bed55-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bed55-113">Requirement</span></span> | <span data-ttu-id="bed55-114">Value</span><span class="sxs-lookup"><span data-stu-id="bed55-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bed55-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bed55-115">Redistributable</span></span><br/> | <span data-ttu-id="bed55-116">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="bed55-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bed55-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bed55-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="bed55-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bed55-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed55-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bed55-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed55-120">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="bed55-120">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 

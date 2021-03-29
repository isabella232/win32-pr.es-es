---
description: El objeto PublicKey representa una clave pública en un objeto de certificado.
title: PublicKey (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650185"
---
# <a name="publickey-object"></a><span data-ttu-id="f3712-103">PublicKey (objeto)</span><span class="sxs-lookup"><span data-stu-id="f3712-103">PublicKey object</span></span>

<span data-ttu-id="f3712-104">\[El objeto **publicKey** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f3712-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3712-105">En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f3712-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f3712-106">El objeto **publicKey** representa una clave pública en un objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="f3712-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f3712-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="f3712-107">When to use</span></span>

<span data-ttu-id="f3712-108">El objeto **publicKey** se utiliza para recuperar datos sobre la clave pública.</span><span class="sxs-lookup"><span data-stu-id="f3712-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="f3712-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f3712-109">Members</span></span>

<span data-ttu-id="f3712-110">El objeto **publicKey** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f3712-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="f3712-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3712-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3712-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3712-112">Properties</span></span>

<span data-ttu-id="f3712-113">El objeto **publicKey** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f3712-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="f3712-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3712-114">Property</span></span>                                                            | <span data-ttu-id="f3712-115">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f3712-115">Access type</span></span>          | <span data-ttu-id="f3712-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3712-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3712-117">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="f3712-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="f3712-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3712-118">Read-only</span></span><br/> | <span data-ttu-id="f3712-119">Recupera el objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública.</span><span class="sxs-lookup"><span data-stu-id="f3712-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="f3712-120">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f3712-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="f3712-121">**EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="f3712-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="f3712-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3712-122">Read-only</span></span><br/> | <span data-ttu-id="f3712-123">Recupera un objeto [**EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="f3712-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="f3712-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="f3712-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="f3712-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3712-125">Read-only</span></span><br/> | <span data-ttu-id="f3712-126">Recupera un objeto [**EncodedData**](encodeddata.md) que proporciona acceso a los parámetros del algoritmo de clave pública.</span><span class="sxs-lookup"><span data-stu-id="f3712-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="f3712-127">**Length**</span><span class="sxs-lookup"><span data-stu-id="f3712-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="f3712-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f3712-128">Read-only</span></span><br/> | <span data-ttu-id="f3712-129">Recupera la longitud de la clave pública en bits.</span><span class="sxs-lookup"><span data-stu-id="f3712-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="f3712-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3712-130">Remarks</span></span>

<span data-ttu-id="f3712-131">No se puede crear el objeto **publicKey** .</span><span class="sxs-lookup"><span data-stu-id="f3712-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="f3712-132">El método [**Certificate. publickey**](certificate-publickey.md) utiliza el objeto **publicKey** .</span><span class="sxs-lookup"><span data-stu-id="f3712-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3712-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3712-133">Requirements</span></span>



| <span data-ttu-id="f3712-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3712-134">Requirement</span></span> | <span data-ttu-id="f3712-135">Value</span><span class="sxs-lookup"><span data-stu-id="f3712-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3712-136">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f3712-136">Redistributable</span></span><br/> | <span data-ttu-id="f3712-137">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3712-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f3712-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3712-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="f3712-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3712-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

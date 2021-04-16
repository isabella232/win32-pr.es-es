---
description: Elimina el almacén de certificados representado por el objeto de almacén actual.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650209"
---
# <a name="storedelete-method"></a><span data-ttu-id="cffe5-103">Store. Delete (método)</span><span class="sxs-lookup"><span data-stu-id="cffe5-103">Store.Delete method</span></span>

<span data-ttu-id="cffe5-104">\[El método **Delete** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="cffe5-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cffe5-105">En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cffe5-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cffe5-106">El método **Delete** elimina el [*almacén de certificados*](../secgloss/c-gly.md) representado por el objeto de [**almacén**](certificate.md) actual.</span><span class="sxs-lookup"><span data-stu-id="cffe5-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="cffe5-107">Este método elimina solo almacenes que no son del sistema.</span><span class="sxs-lookup"><span data-stu-id="cffe5-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="cffe5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cffe5-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="cffe5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cffe5-109">Parameters</span></span>

<span data-ttu-id="cffe5-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cffe5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cffe5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cffe5-111">Return value</span></span>

<span data-ttu-id="cffe5-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cffe5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cffe5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cffe5-113">Remarks</span></span>

<span data-ttu-id="cffe5-114">Los siguientes almacenes son almacenes del sistema y no se pueden eliminar:</span><span class="sxs-lookup"><span data-stu-id="cffe5-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="cffe5-115">My</span><span class="sxs-lookup"><span data-stu-id="cffe5-115">My</span></span>
-   <span data-ttu-id="cffe5-116">Root</span><span class="sxs-lookup"><span data-stu-id="cffe5-116">Root</span></span>
-   <span data-ttu-id="cffe5-117">Confianza</span><span class="sxs-lookup"><span data-stu-id="cffe5-117">Trust</span></span>
-   <span data-ttu-id="cffe5-118">CA</span><span class="sxs-lookup"><span data-stu-id="cffe5-118">CA</span></span>
-   <span data-ttu-id="cffe5-119">UserDS</span><span class="sxs-lookup"><span data-stu-id="cffe5-119">UserDS</span></span>
-   <span data-ttu-id="cffe5-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="cffe5-120">TrustedPublisher</span></span>
-   <span data-ttu-id="cffe5-121">No permitida.</span><span class="sxs-lookup"><span data-stu-id="cffe5-121">Disallowed</span></span>
-   <span data-ttu-id="cffe5-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="cffe5-122">AuthRoot</span></span>
-   <span data-ttu-id="cffe5-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="cffe5-123">TrustedPeople</span></span>

<span data-ttu-id="cffe5-124">El método **Delete** devuelve un error si se llama desde un script Web.</span><span class="sxs-lookup"><span data-stu-id="cffe5-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="cffe5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cffe5-125">Requirements</span></span>



| <span data-ttu-id="cffe5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cffe5-126">Requirement</span></span> | <span data-ttu-id="cffe5-127">Value</span><span class="sxs-lookup"><span data-stu-id="cffe5-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cffe5-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cffe5-128">Redistributable</span></span><br/> | <span data-ttu-id="cffe5-129">CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="cffe5-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cffe5-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cffe5-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="cffe5-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cffe5-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cffe5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="cffe5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cffe5-133">**Store**</span><span class="sxs-lookup"><span data-stu-id="cffe5-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="cffe5-134">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="cffe5-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

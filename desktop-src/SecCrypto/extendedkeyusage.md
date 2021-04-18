---
description: Proporciona acceso de solo lectura a las propiedades de uso mejorado de clave (EKU) de un certificado.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objeto ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649954"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="40841-103">Objeto ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="40841-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="40841-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40841-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="40841-105">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="40841-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="40841-106">El objeto **ExtendedKeyUsage** proporciona acceso de solo lectura a las propiedades de uso mejorado de clave (EKU) de un certificado.</span><span class="sxs-lookup"><span data-stu-id="40841-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="40841-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="40841-107">Members</span></span>

<span data-ttu-id="40841-108">El objeto **ExtendedKeyUsage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40841-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="40841-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40841-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40841-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40841-110">Properties</span></span>

<span data-ttu-id="40841-111">El objeto **ExtendedKeyUsage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="40841-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="40841-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40841-112">Property</span></span>                                                     | <span data-ttu-id="40841-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="40841-113">Access type</span></span>          | <span data-ttu-id="40841-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="40841-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40841-115">**EKU**</span><span class="sxs-lookup"><span data-stu-id="40841-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="40841-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="40841-116">Read-only</span></span><br/> | <span data-ttu-id="40841-117">Colección [**EKU**](ekus.md) que contiene los objetos [**EKU**](eku.md) para el certificado.</span><span class="sxs-lookup"><span data-stu-id="40841-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="40841-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="40841-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="40841-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="40841-119">Read-only</span></span><br/> | <span data-ttu-id="40841-120">Recupera un valor **booleano** que indica si la extensión EKU está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="40841-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="40841-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="40841-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="40841-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="40841-122">Read-only</span></span><br/> | <span data-ttu-id="40841-123">Recupera un valor **booleano** que indica si la extensión EKU está presente.</span><span class="sxs-lookup"><span data-stu-id="40841-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="40841-124">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="40841-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="40841-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40841-125">Remarks</span></span>

<span data-ttu-id="40841-126">No se puede crear el objeto **ExtendedKeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="40841-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="40841-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40841-127">Requirements</span></span>



| <span data-ttu-id="40841-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="40841-128">Requirement</span></span> | <span data-ttu-id="40841-129">Value</span><span class="sxs-lookup"><span data-stu-id="40841-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40841-130">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="40841-130">End of client support</span></span><br/> | <span data-ttu-id="40841-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40841-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40841-132">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="40841-132">End of server support</span></span><br/> | <span data-ttu-id="40841-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40841-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40841-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="40841-134">Redistributable</span></span><br/>       | <span data-ttu-id="40841-135">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="40841-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="40841-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40841-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="40841-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40841-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40841-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="40841-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40841-139">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="40841-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

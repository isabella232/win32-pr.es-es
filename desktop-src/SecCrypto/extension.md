---
description: Representa una única extensión de certificado.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensión (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690212"
---
# <a name="extension-object"></a><span data-ttu-id="19f86-103">Objeto de extensión</span><span class="sxs-lookup"><span data-stu-id="19f86-103">Extension object</span></span>

<span data-ttu-id="19f86-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19f86-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="19f86-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="19f86-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="19f86-106">El objeto de **extensión** representa una única extensión de certificado.</span><span class="sxs-lookup"><span data-stu-id="19f86-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="19f86-107">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="19f86-107">When to use</span></span>

<span data-ttu-id="19f86-108">El objeto de **extensión** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="19f86-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="19f86-109">Recupere el OID de la extensión de certificado.</span><span class="sxs-lookup"><span data-stu-id="19f86-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="19f86-110">Recupera los datos de la extensión de certificado representados por un objeto [**EncodedData**](encodeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="19f86-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="19f86-111">Determine si la extensión de certificado está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="19f86-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="19f86-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="19f86-112">Members</span></span>

<span data-ttu-id="19f86-113">El objeto de **extensión** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19f86-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="19f86-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19f86-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19f86-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19f86-115">Properties</span></span>

<span data-ttu-id="19f86-116">El objeto de **extensión** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="19f86-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="19f86-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19f86-117">Property</span></span>                                                | <span data-ttu-id="19f86-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="19f86-118">Access type</span></span>          | <span data-ttu-id="19f86-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f86-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19f86-120">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="19f86-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="19f86-121">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="19f86-121">Read-only</span></span><br/> | <span data-ttu-id="19f86-122">Recupera los datos codificados para la extensión.</span><span class="sxs-lookup"><span data-stu-id="19f86-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="19f86-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="19f86-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="19f86-124">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="19f86-124">Read-only</span></span><br/> | <span data-ttu-id="19f86-125">Recupera un valor booleano que indica si la extensión está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="19f86-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="19f86-126">**OID**</span><span class="sxs-lookup"><span data-stu-id="19f86-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="19f86-127">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="19f86-127">Read-only</span></span><br/> | <span data-ttu-id="19f86-128">Recupera el identificador de objeto de la extensión.</span><span class="sxs-lookup"><span data-stu-id="19f86-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="19f86-129">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="19f86-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="19f86-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19f86-130">Remarks</span></span>

<span data-ttu-id="19f86-131">No se puede crear el objeto de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="19f86-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="19f86-132">El objeto de la colección de [**extensiones**](extensions.md) utiliza el objeto de **extensión** .</span><span class="sxs-lookup"><span data-stu-id="19f86-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f86-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f86-133">Requirements</span></span>



| <span data-ttu-id="19f86-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f86-134">Requirement</span></span> | <span data-ttu-id="19f86-135">Value</span><span class="sxs-lookup"><span data-stu-id="19f86-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19f86-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="19f86-136">End of client support</span></span><br/> | <span data-ttu-id="19f86-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19f86-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="19f86-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="19f86-138">End of server support</span></span><br/> | <span data-ttu-id="19f86-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19f86-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="19f86-140">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="19f86-140">Redistributable</span></span><br/>       | <span data-ttu-id="19f86-141">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="19f86-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19f86-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19f86-142">Header</span></span><br/>                | <dl> <span data-ttu-id="19f86-143"><dt>Mmcobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f86-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="19f86-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19f86-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="19f86-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19f86-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

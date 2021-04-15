---
description: Representa una colección de objetos OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objeto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690060"
---
# <a name="oids-object"></a><span data-ttu-id="4c385-103">Objeto OID</span><span class="sxs-lookup"><span data-stu-id="4c385-103">OIDs object</span></span>

<span data-ttu-id="4c385-104">\[El objeto **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4c385-104">\[The **OIDs** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c385-105">En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="4c385-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="4c385-106">El objeto **OID** representa una colección de objetos [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="4c385-106">The **OIDs** object represents a collection of [**OID**](oid.md) objects.</span></span> <span data-ttu-id="4c385-107">Cada objeto [**OID**](oid.md) representa un único identificador de objeto.</span><span class="sxs-lookup"><span data-stu-id="4c385-107">Each [**OID**](oid.md) object represents a single object identifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="4c385-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="4c385-108">When to use</span></span>

<span data-ttu-id="4c385-109">El objeto **OID** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="4c385-109">The **OIDs** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="4c385-110">Agregue o quite un objeto [**OID**](oid.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-110">Add or remove an [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="4c385-111">Borre todos los objetos [**OID**](oid.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-111">Clear all the [**OID**](oid.md) objects from the collection.</span></span>
-   <span data-ttu-id="4c385-112">Recupere el número de identificadores de objeto de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-112">Retrieve the number of object identifiers in the collection.</span></span>
-   <span data-ttu-id="4c385-113">Recupera un objeto [**OID**](oid.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-113">Retrieve a specific [**OID**](oid.md) object from the collection.</span></span>
-   <span data-ttu-id="4c385-114">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="4c385-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="4c385-115">Members</span></span>

<span data-ttu-id="4c385-116">El objeto **OID** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4c385-116">The **OIDs** object has these types of members:</span></span>

-   [<span data-ttu-id="4c385-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c385-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c385-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c385-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c385-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="4c385-119">Methods</span></span>

<span data-ttu-id="4c385-120">El objeto **OID** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4c385-120">The **OIDs** object has these methods.</span></span>



| <span data-ttu-id="4c385-121">Método</span><span class="sxs-lookup"><span data-stu-id="4c385-121">Method</span></span>                        | <span data-ttu-id="4c385-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c385-122">Description</span></span>                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="4c385-123">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="4c385-123">**Add**</span></span>](oids-add.md)       | <span data-ttu-id="4c385-124">Agrega un objeto [**OID**](oid.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-124">Adds an [**OID**](oid.md) object to the collection.</span></span><br/>              |
| [<span data-ttu-id="4c385-125">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="4c385-125">**Clear**</span></span>](oids-clear.md)   | <span data-ttu-id="4c385-126">Borra todos los objetos [**OID**](oid.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-126">Clears all [**OID**](oid.md) objects from the collection.</span></span><br/>        |
| [<span data-ttu-id="4c385-127">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="4c385-127">**Remove**</span></span>](oids-remove.md) | <span data-ttu-id="4c385-128">Quita un objeto [**OID**](oid.md) indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-128">Removes an indexed [**OID**](oid.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4c385-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4c385-129">Properties</span></span>

<span data-ttu-id="4c385-130">El objeto **OID** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4c385-130">The **OIDs** object has these properties.</span></span>



| <span data-ttu-id="4c385-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c385-131">Property</span></span>                                     | <span data-ttu-id="4c385-132">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4c385-132">Access type</span></span>          | <span data-ttu-id="4c385-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c385-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c385-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="4c385-134">**\_NewEnum**</span></span>](oids-newenum.md)<br/> | <span data-ttu-id="4c385-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c385-135">Read-only</span></span><br/> | <span data-ttu-id="4c385-136">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="4c385-137">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="4c385-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="4c385-138">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="4c385-138">**Count**</span></span>](oids-count.md)<br/>       | <span data-ttu-id="4c385-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c385-139">Read-only</span></span><br/> | <span data-ttu-id="4c385-140">Recupera el número de objetos [**OID**](oid.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-140">Retrieves the number of [**OID**](oid.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="4c385-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c385-141">**Item**</span></span>](oids-item.md)<br/>         | <span data-ttu-id="4c385-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4c385-142">Read-only</span></span><br/> | <span data-ttu-id="4c385-143">Recupera un objeto [**OID**](oid.md) indizado de la colección.</span><span class="sxs-lookup"><span data-stu-id="4c385-143">Retrieves an indexed [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="4c385-144">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4c385-144">This is the default property.</span></span><br/>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="4c385-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c385-145">Remarks</span></span>

<span data-ttu-id="4c385-146">No se puede crear el objeto **OID** .</span><span class="sxs-lookup"><span data-stu-id="4c385-146">The **OIDs** object cannot be created.</span></span>

<span data-ttu-id="4c385-147">Las siguientes propiedades utilizan el objeto **OID** :</span><span class="sxs-lookup"><span data-stu-id="4c385-147">The **OIDs** object is used by the following properties:</span></span>

-   [<span data-ttu-id="4c385-148">**CertificateStatus.ApplicationPolicies**</span><span class="sxs-lookup"><span data-stu-id="4c385-148">**CertificateStatus.ApplicationPolicies**</span></span>](certificatestatus-applicationpolicies.md)
-   [<span data-ttu-id="4c385-149">**CertificateStatus.CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="4c385-149">**CertificateStatus.CertificatePolicies**</span></span>](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a><span data-ttu-id="4c385-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c385-150">Requirements</span></span>



| <span data-ttu-id="4c385-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c385-151">Requirement</span></span> | <span data-ttu-id="4c385-152">Value</span><span class="sxs-lookup"><span data-stu-id="4c385-152">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c385-153">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4c385-153">Redistributable</span></span><br/> | <span data-ttu-id="4c385-154">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c385-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4c385-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c385-155">DLL</span></span><br/>             | <dl> <span data-ttu-id="4c385-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c385-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

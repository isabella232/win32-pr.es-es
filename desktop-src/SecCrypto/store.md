---
description: Proporciona propiedades y métodos que puede usar para elegir, administrar y usar almacenes de certificados y certificados en esos almacenes.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Objeto Store
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649945"
---
# <a name="store-object"></a><span data-ttu-id="d6173-103">Objeto Store</span><span class="sxs-lookup"><span data-stu-id="d6173-103">Store object</span></span>

<span data-ttu-id="d6173-104">\[El objeto de **almacenamiento** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d6173-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d6173-105">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d6173-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d6173-106">El objeto de **almacén** proporciona propiedades y métodos que puede usar para elegir, administrar y usar [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de esas tiendas.</span><span class="sxs-lookup"><span data-stu-id="d6173-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="d6173-107">CAPICOM puede utilizar el usuario actual, el equipo local, la memoria y los almacenes de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d6173-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="d6173-108">Además, los almacenes admiten almacenes de certificados basados en tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="d6173-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="d6173-109">Los desarrolladores deben tener en cuenta que pueden producirse errores en algunos métodos con algunos almacenes si se intentan realizar operaciones para las que el usuario no tiene derechos.</span><span class="sxs-lookup"><span data-stu-id="d6173-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="d6173-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6173-110">Members</span></span>

<span data-ttu-id="d6173-111">El objeto **Store** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6173-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="d6173-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d6173-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d6173-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6173-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d6173-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d6173-114">Methods</span></span>

<span data-ttu-id="d6173-115">El objeto **Store** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d6173-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="d6173-116">Método</span><span class="sxs-lookup"><span data-stu-id="d6173-116">Method</span></span>                         | <span data-ttu-id="d6173-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6173-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6173-118">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="d6173-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="d6173-119">Agrega un objeto de [**certificado**](certificate.md) al almacén de certificados abierto.</span><span class="sxs-lookup"><span data-stu-id="d6173-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="d6173-120">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="d6173-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="d6173-121">Cierra un almacén de certificados abierto.</span><span class="sxs-lookup"><span data-stu-id="d6173-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="d6173-122">**CAPICOM 2.0.0.3 y versiones anteriores:** No se admite el método [**Close**](store-close.md) .</span><span class="sxs-lookup"><span data-stu-id="d6173-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="d6173-123">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="d6173-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="d6173-124">Elimina el almacén de certificados representado por el objeto de [**almacén**](certificate.md) actual.</span><span class="sxs-lookup"><span data-stu-id="d6173-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="d6173-125">**CAPICOM 2.0.0.3 y versiones anteriores:** No se admite el método [**Delete**](store-delete.md) .</span><span class="sxs-lookup"><span data-stu-id="d6173-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="d6173-126">**Exportación**</span><span class="sxs-lookup"><span data-stu-id="d6173-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="d6173-127">Exporta el almacén de un [*BLOB*](../secgloss/b-gly.md)codificado.</span><span class="sxs-lookup"><span data-stu-id="d6173-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="d6173-128">**Importar**</span><span class="sxs-lookup"><span data-stu-id="d6173-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="d6173-129">Importa un almacén exportado previamente.</span><span class="sxs-lookup"><span data-stu-id="d6173-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="d6173-130">**Cargar**</span><span class="sxs-lookup"><span data-stu-id="d6173-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="d6173-131">Importa los objetos de [**certificado**](certificate.md) de un archivo en el almacén.</span><span class="sxs-lookup"><span data-stu-id="d6173-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="d6173-132">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="d6173-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="d6173-133">Abre un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="d6173-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="d6173-134">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="d6173-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="d6173-135">Quita un objeto de [**certificado**](certificate.md) de un almacén abierto.</span><span class="sxs-lookup"><span data-stu-id="d6173-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="d6173-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6173-136">Properties</span></span>

<span data-ttu-id="d6173-137">El objeto **Store** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d6173-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="d6173-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6173-138">Property</span></span>                                              | <span data-ttu-id="d6173-139">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d6173-139">Access type</span></span>          | <span data-ttu-id="d6173-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6173-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6173-141">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="d6173-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="d6173-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6173-142">Read-only</span></span><br/> | <span data-ttu-id="d6173-143">Recupera la colección de [**certificados**](certificates.md) del almacén.</span><span class="sxs-lookup"><span data-stu-id="d6173-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="d6173-144">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="d6173-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d6173-145">**Location**</span><span class="sxs-lookup"><span data-stu-id="d6173-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="d6173-146">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6173-146">Read-only</span></span><br/> | <span data-ttu-id="d6173-147">Recupera la ubicación del almacén de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="d6173-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="d6173-148">**CAPICOM 2.0.0.3 y versiones anteriores:** No se admite la propiedad [**Location**](store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="d6173-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="d6173-149">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6173-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="d6173-150">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6173-150">Read-only</span></span><br/> | <span data-ttu-id="d6173-151">Recupera el nombre del almacén de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="d6173-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="d6173-152">**CAPICOM 2.0.0.3 y versiones anteriores:** No se admite la propiedad [**Name**](store-name.md) .</span><span class="sxs-lookup"><span data-stu-id="d6173-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d6173-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6173-153">Remarks</span></span>

<span data-ttu-id="d6173-154">Se puede crear el objeto de **almacén** y es seguro para el scripting.</span><span class="sxs-lookup"><span data-stu-id="d6173-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="d6173-155">El ProgID del objeto **Store** es CAPICOM. Almacén. 2.</span><span class="sxs-lookup"><span data-stu-id="d6173-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="d6173-156">**CAPICOM 1. *x*:** el identificador de programa (ProgID) del objeto **Store** es CAPICOM. Almacén. 1.</span><span class="sxs-lookup"><span data-stu-id="d6173-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6173-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6173-157">Requirements</span></span>



| <span data-ttu-id="d6173-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6173-158">Requirement</span></span> | <span data-ttu-id="d6173-159">Value</span><span class="sxs-lookup"><span data-stu-id="d6173-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6173-160">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d6173-160">Redistributable</span></span><br/> | <span data-ttu-id="d6173-161">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6173-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d6173-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6173-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="d6173-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6173-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6173-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6173-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6173-165">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="d6173-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

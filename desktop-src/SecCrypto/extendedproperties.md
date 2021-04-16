---
description: Representa una colección de objetos ExtendedProperty.
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 512c29e43b9099d9ef577cce61bbcc3a38d68ac6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649907"
---
# <a name="extendedproperties-object"></a><span data-ttu-id="27061-103">ExtendedProperties (objeto)</span><span class="sxs-lookup"><span data-stu-id="27061-103">ExtendedProperties object</span></span>

<span data-ttu-id="27061-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27061-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="27061-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades.</span><span class="sxs-lookup"><span data-stu-id="27061-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="27061-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="27061-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="27061-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="27061-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="27061-108">El objeto **ExtendedProperties** representa una colección de objetos [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="27061-108">The **ExtendedProperties** object represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span> <span data-ttu-id="27061-109">Cada objeto representa una única propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="27061-109">Each object represents a single extended property.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="27061-110">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="27061-110">When to use</span></span>

<span data-ttu-id="27061-111">El objeto **ExtendedProperties** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="27061-111">The **ExtendedProperties** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="27061-112">Agregue o quite un objeto [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-112">Add or remove an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="27061-113">Recupere el número de propiedades extendidas de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-113">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="27061-114">Recupera un objeto [**ExtendedProperty**](extendedproperty.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-114">Retrieve a specific [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span>
-   <span data-ttu-id="27061-115">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-115">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="27061-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="27061-116">Members</span></span>

<span data-ttu-id="27061-117">El objeto **ExtendedProperties** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="27061-117">The **ExtendedProperties** object has these types of members:</span></span>

-   [<span data-ttu-id="27061-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="27061-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="27061-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27061-119">Properties</span></span>](#extendedproperties-object)

### <a name="methods"></a><span data-ttu-id="27061-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="27061-120">Methods</span></span>

<span data-ttu-id="27061-121">El objeto **ExtendedProperties** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="27061-121">The **ExtendedProperties** object has these methods.</span></span>



| <span data-ttu-id="27061-122">Método</span><span class="sxs-lookup"><span data-stu-id="27061-122">Method</span></span>                                      | <span data-ttu-id="27061-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="27061-123">Description</span></span>                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27061-124">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="27061-124">**Add**</span></span>](extendedproperties-add.md)       | <span data-ttu-id="27061-125">Agrega un objeto [**ExtendedProperty**](extendedproperty.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-125">Adds an [**ExtendedProperty**](extendedproperty.md) object to the collection.</span></span><br/>      |
| [<span data-ttu-id="27061-126">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="27061-126">**Remove**</span></span>](extendedproperties-remove.md) | <span data-ttu-id="27061-127">Quita un objeto [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-127">Removes an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="27061-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27061-128">Properties</span></span>

<span data-ttu-id="27061-129">El objeto **ExtendedProperties** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="27061-129">The **ExtendedProperties** object has these properties.</span></span>



| <span data-ttu-id="27061-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27061-130">Property</span></span>                                                   | <span data-ttu-id="27061-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="27061-131">Access type</span></span>          | <span data-ttu-id="27061-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="27061-132">Description</span></span>                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27061-133">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="27061-133">**\_NewEnum**</span></span>](extendedproperties-newenum.md)<br/> | <span data-ttu-id="27061-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="27061-134">Read-only</span></span><br/> | <span data-ttu-id="27061-135">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-135">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="27061-136">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="27061-136">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="27061-137">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="27061-137">**Count**</span></span>](extendedproperties-count.md)<br/>       | <span data-ttu-id="27061-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="27061-138">Read-only</span></span><br/> | <span data-ttu-id="27061-139">Recupera el número de objetos [**ExtendedProperty**](extendedproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-139">Retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="27061-140">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="27061-140">**Item**</span></span>](extendedproperties-item.md)<br/>         | <span data-ttu-id="27061-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="27061-141">Read-only</span></span><br/> | <span data-ttu-id="27061-142">Recupera un objeto [**ExtendedProperty**](extendedproperty.md) que representa la propiedad extendida indizada de la colección.</span><span class="sxs-lookup"><span data-stu-id="27061-142">Retrieves an [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span> <span data-ttu-id="27061-143">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="27061-143">This is the default property.</span></span><br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="27061-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27061-144">Remarks</span></span>

<span data-ttu-id="27061-145">No se puede crear el objeto **ExtendedProperties** .</span><span class="sxs-lookup"><span data-stu-id="27061-145">The **ExtendedProperties** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="27061-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27061-146">Requirements</span></span>



| <span data-ttu-id="27061-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="27061-147">Requirement</span></span> | <span data-ttu-id="27061-148">Value</span><span class="sxs-lookup"><span data-stu-id="27061-148">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27061-149">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="27061-149">End of client support</span></span><br/> | <span data-ttu-id="27061-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27061-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="27061-151">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="27061-151">End of server support</span></span><br/> | <span data-ttu-id="27061-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27061-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="27061-153">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="27061-153">Redistributable</span></span><br/>       | <span data-ttu-id="27061-154">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="27061-154">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="27061-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27061-155">DLL</span></span><br/>                   | <dl> <span data-ttu-id="27061-156"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27061-156"><dt>Capicom.dll</dt></span></span> </dl> |



 

 

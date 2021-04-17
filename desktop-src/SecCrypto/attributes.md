---
description: Representa una colección de objetos de atributo.
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributes (objeto)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2493d4e1bbcbeb2dc7e7b335513beb84c3f28d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670682"
---
# <a name="attributes-object"></a><span data-ttu-id="370bb-103">Attributes (objeto)</span><span class="sxs-lookup"><span data-stu-id="370bb-103">Attributes object</span></span>

<span data-ttu-id="370bb-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="370bb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="370bb-105">En su lugar, use la [**clase CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="370bb-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="370bb-106">El objeto **attributes** representa una colección de objetos de [**atributo**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="370bb-106">The **Attributes** object represents a collection of [**Attribute**](attribute.md) objects.</span></span> <span data-ttu-id="370bb-107">Cada objeto de [**atributo**](attribute.md) representa un atributo único de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="370bb-107">Each [**Attribute**](attribute.md) object represents a single attribute of a message.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="370bb-108">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="370bb-108">When to use</span></span>

<span data-ttu-id="370bb-109">El objeto **attributes** se usa para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="370bb-109">The **Attributes** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="370bb-110">Agregue o quite un objeto de [**atributo**](attribute.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-110">Add or remove a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="370bb-111">Borre la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-111">Clear the collection.</span></span>
-   <span data-ttu-id="370bb-112">Recupere el número de atributos de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-112">Retrieve the number of attributes in the collection.</span></span>
-   <span data-ttu-id="370bb-113">Recupera un objeto de [**atributo**](attribute.md) específico de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-113">Retrieve a specific [**Attribute**](attribute.md) object from the collection.</span></span>
-   <span data-ttu-id="370bb-114">Recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-114">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="370bb-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="370bb-115">Members</span></span>

<span data-ttu-id="370bb-116">El objeto **attributes** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="370bb-116">The **Attributes** object has these types of members:</span></span>

-   [<span data-ttu-id="370bb-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="370bb-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="370bb-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="370bb-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="370bb-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="370bb-119">Methods</span></span>

<span data-ttu-id="370bb-120">El objeto **attributes** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="370bb-120">The **Attributes** object has these methods.</span></span>



| <span data-ttu-id="370bb-121">Método</span><span class="sxs-lookup"><span data-stu-id="370bb-121">Method</span></span>                              | <span data-ttu-id="370bb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="370bb-122">Description</span></span>                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="370bb-123">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="370bb-123">**Add**</span></span>](attributes-add.md)       | <span data-ttu-id="370bb-124">Agrega un objeto de [**atributo**](attribute.md) a la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-124">Adds an [**Attribute**](attribute.md) object to the collection.</span></span><br/>       |
| [<span data-ttu-id="370bb-125">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="370bb-125">**Clear**</span></span>](attributes-clear.md)   | <span data-ttu-id="370bb-126">Borra todos los objetos de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-126">Clears all [**Attribute**](attribute.md) objects from the collection.</span></span><br/> |
| [<span data-ttu-id="370bb-127">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="370bb-127">**Remove**</span></span>](attributes-remove.md) | <span data-ttu-id="370bb-128">Quita un objeto de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-128">Removes an [**Attribute**](attribute.md) object from the collection.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="370bb-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="370bb-129">Properties</span></span>

<span data-ttu-id="370bb-130">El objeto **attributes** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="370bb-130">The **Attributes** object has these properties.</span></span>



| <span data-ttu-id="370bb-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="370bb-131">Property</span></span>                                           | <span data-ttu-id="370bb-132">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="370bb-132">Access type</span></span>          | <span data-ttu-id="370bb-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="370bb-133">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="370bb-134">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="370bb-134">**\_NewEnum**</span></span>](attributes-newenum.md)<br/> | <span data-ttu-id="370bb-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="370bb-135">Read-only</span></span><br/> | <span data-ttu-id="370bb-136">Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-136">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="370bb-137">Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="370bb-137">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="370bb-138">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="370bb-138">**Count**</span></span>](attributes-count.md)<br/>       | <span data-ttu-id="370bb-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="370bb-139">Read-only</span></span><br/> | <span data-ttu-id="370bb-140">Recupera el número de objetos de [**atributo**](attribute.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="370bb-140">Retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="370bb-141">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="370bb-141">**Item**</span></span>](attributes-item.md)<br/>         | <span data-ttu-id="370bb-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="370bb-142">Read-only</span></span><br/> | <span data-ttu-id="370bb-143">Recupera el objeto de [**atributo**](attribute.md) que representa el atributo indizado.</span><span class="sxs-lookup"><span data-stu-id="370bb-143">Retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="370bb-144">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="370bb-144">This is the default property.</span></span><br/>                                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="370bb-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="370bb-145">Remarks</span></span>

<span data-ttu-id="370bb-146">No se puede crear el objeto **attributes** .</span><span class="sxs-lookup"><span data-stu-id="370bb-146">The **Attributes** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="370bb-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="370bb-147">Requirements</span></span>



| <span data-ttu-id="370bb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="370bb-148">Requirement</span></span> | <span data-ttu-id="370bb-149">Value</span><span class="sxs-lookup"><span data-stu-id="370bb-149">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="370bb-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="370bb-150">End of client support</span></span><br/> | <span data-ttu-id="370bb-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="370bb-151">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="370bb-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="370bb-152">End of server support</span></span><br/> | <span data-ttu-id="370bb-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="370bb-153">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="370bb-154">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="370bb-154">Redistributable</span></span><br/>       | <span data-ttu-id="370bb-155">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="370bb-155">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="370bb-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="370bb-156">DLL</span></span><br/>                   | <dl> <span data-ttu-id="370bb-157"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="370bb-157"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="370bb-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="370bb-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370bb-159">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="370bb-159">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

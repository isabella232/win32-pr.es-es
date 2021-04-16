---
description: Proporciona métodos estándar COM para administrar elementos de datos de almacenamiento protegido.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interfaz IPStore (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649512"
---
# <a name="ipstore-interface"></a><span data-ttu-id="418b0-103">Interfaz IPStore</span><span class="sxs-lookup"><span data-stu-id="418b0-103">IPStore interface</span></span>

<span data-ttu-id="418b0-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="418b0-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="418b0-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="418b0-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="418b0-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="418b0-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="418b0-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="418b0-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="418b0-108">\[Es posible que esta interfaz se modifique o no esté disponible en versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="418b0-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="418b0-109">Proporciona métodos estándar COM para administrar elementos de datos de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="418b0-110">El método [**PStoreCreateInstance**](pstorecreateinstance.md) devuelve un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="418b0-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="418b0-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="418b0-111">Members</span></span>

<span data-ttu-id="418b0-112">La interfaz **IPStore** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="418b0-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="418b0-113">**IPStore** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="418b0-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="418b0-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="418b0-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="418b0-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="418b0-115">Methods</span></span>

<span data-ttu-id="418b0-116">La interfaz **IPStore** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="418b0-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="418b0-117">Método</span><span class="sxs-lookup"><span data-stu-id="418b0-117">Method</span></span>                                                   | <span data-ttu-id="418b0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="418b0-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="418b0-119">**CloseItem**</span><span class="sxs-lookup"><span data-stu-id="418b0-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="418b0-120">Cierra un elemento de datos especificado de un almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="418b0-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="418b0-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="418b0-122">Crea el subtipo especificado en el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="418b0-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="418b0-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="418b0-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="418b0-124">Crea el tipo especificado con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="418b0-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="418b0-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="418b0-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="418b0-126">Elimina el elemento especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="418b0-127">**DeleteSubtype**</span><span class="sxs-lookup"><span data-stu-id="418b0-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="418b0-128">Elimina el subtipo de elemento especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="418b0-129">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="418b0-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="418b0-130">Elimina el tipo especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="418b0-131">**EnumItems**</span><span class="sxs-lookup"><span data-stu-id="418b0-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="418b0-132">Devuelve el puntero de interfaz de un subtipo para enumerar los elementos de la base de datos de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="418b0-133">**EnumSubtypes**</span><span class="sxs-lookup"><span data-stu-id="418b0-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="418b0-134">Devuelve una interfaz para enumerar los subtipos de los tipos registrados actualmente en la base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="418b0-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="418b0-135">**EnumTypes**</span><span class="sxs-lookup"><span data-stu-id="418b0-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="418b0-136">Devuelve una interfaz para enumerar los tipos registrados actualmente en la base de datos protegida.</span><span class="sxs-lookup"><span data-stu-id="418b0-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="418b0-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="418b0-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="418b0-138">Recupera información sobre el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="418b0-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="418b0-139">**GetProvParam**</span><span class="sxs-lookup"><span data-stu-id="418b0-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="418b0-140">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="418b0-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="418b0-141">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="418b0-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="418b0-142">Recupera información asociada a un subtipo.</span><span class="sxs-lookup"><span data-stu-id="418b0-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="418b0-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="418b0-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="418b0-144">Recupera información asociada a un tipo.</span><span class="sxs-lookup"><span data-stu-id="418b0-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="418b0-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="418b0-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="418b0-146">Abre un elemento para varios accesos.</span><span class="sxs-lookup"><span data-stu-id="418b0-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="418b0-147">**ReadAccessRuleSet**</span><span class="sxs-lookup"><span data-stu-id="418b0-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="418b0-148">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="418b0-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="418b0-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="418b0-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="418b0-150">Lee el elemento de datos especificado del almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="418b0-151">**SetProvParam**</span><span class="sxs-lookup"><span data-stu-id="418b0-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="418b0-152">Establece la información de parámetros especificada.</span><span class="sxs-lookup"><span data-stu-id="418b0-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="418b0-153">**WriteAccessRuleset**</span><span class="sxs-lookup"><span data-stu-id="418b0-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="418b0-154">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="418b0-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="418b0-155">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="418b0-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="418b0-156">Escribe un elemento de datos en el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="418b0-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="418b0-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="418b0-157">Requirements</span></span>



| <span data-ttu-id="418b0-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="418b0-158">Requirement</span></span> | <span data-ttu-id="418b0-159">Value</span><span class="sxs-lookup"><span data-stu-id="418b0-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="418b0-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="418b0-160">Header</span></span><br/> | <dl> <span data-ttu-id="418b0-161"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="418b0-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="418b0-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="418b0-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="418b0-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="418b0-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 

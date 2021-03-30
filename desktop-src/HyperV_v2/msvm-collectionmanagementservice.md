---
description: Administra las colecciones en el host de Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Msvm_CollectionManagementService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819019"
---
# <a name="msvm_collectionmanagementservice-class"></a><span data-ttu-id="9b9f8-103">MSVM \_ CollectionManagementService (clase)</span><span class="sxs-lookup"><span data-stu-id="9b9f8-103">Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="9b9f8-104">Administra las colecciones en el host de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-104">Manages the collections on the Hyper-V host.</span></span>

<span data-ttu-id="9b9f8-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9f8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b9f8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="9b9f8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b9f8-107">Members</span></span>

<span data-ttu-id="9b9f8-108">La clase **MSVM \_ CollectionManagementService** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b9f8-108">The **Msvm\_CollectionManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="9b9f8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b9f8-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9b9f8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b9f8-110">Methods</span></span>

<span data-ttu-id="9b9f8-111">La clase **MSVM \_ CollectionManagementService** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-111">The **Msvm\_CollectionManagementService** class has these methods.</span></span>



| <span data-ttu-id="9b9f8-112">Método</span><span class="sxs-lookup"><span data-stu-id="9b9f8-112">Method</span></span>                                                                          | <span data-ttu-id="9b9f8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b9f8-113">Description</span></span>                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b9f8-114">**AddMember**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-114">**AddMember**</span></span>](msvm-collectionmanagementservice-addmember.md)                 | <span data-ttu-id="9b9f8-115">Agrega el elemento ManagedElement especificado como miembro del objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-115">Adds the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                           |
| [<span data-ttu-id="9b9f8-116">**DefineCollection**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-116">**DefineCollection**</span></span>](msvm-collectionmanagementservice-definecollection.md)   | <span data-ttu-id="9b9f8-117">Crea un nuevo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="9b9f8-117">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="9b9f8-118">**DestroyCollection**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-118">**DestroyCollection**</span></span>](msvm-collectionmanagementservice-destroycollection.md) | <span data-ttu-id="9b9f8-119">Elimina el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-119">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="9b9f8-120">**RemoveMember**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-120">**RemoveMember**</span></span>](msvm-collectionmanagementservice-removemember.md)           | <span data-ttu-id="9b9f8-121">Quita el elemento ManagedElement especificado como miembro del objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-121">Removes the specified ManagedElement as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="9b9f8-122">**RemoveMemberById**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-122">**RemoveMemberById**</span></span>](msvm-collectionmanagementservice-removememberbyid.md)   | <span data-ttu-id="9b9f8-123">Quita el elemento ManagedElement especificado como miembro de [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-123">Removes the specified ManagedElement as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="9b9f8-124">Esto se realizará correctamente incluso si el objeto con ese identificador no está presente.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-124">This will succeed even if the object with that identifier is not present.</span></span><br/> |
| [<span data-ttu-id="9b9f8-125">**RenameCollection**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-125">**RenameCollection**</span></span>](msvm-collectionmanagementservice-renamecollection.md)   | <span data-ttu-id="9b9f8-126">Actualiza ElementName el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-126">Updates the ElementName the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="9b9f8-127">**StartService**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-127">**StartService**</span></span>](msvm-collectionmanagementservice-startservice.md)           | <span data-ttu-id="9b9f8-128">inicia el servicio.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-128">Starts the service.</span></span><br/>                                                                                                                                                                                                |
| [<span data-ttu-id="9b9f8-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-129">**StopService**</span></span>](msvm-collectionmanagementservice-stopservice.md)             | <span data-ttu-id="9b9f8-130">detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="9b9f8-130">Stops the service.</span></span><br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="9b9f8-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b9f8-131">Requirements</span></span>



| <span data-ttu-id="9b9f8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b9f8-132">Requirement</span></span> | <span data-ttu-id="9b9f8-133">Value</span><span class="sxs-lookup"><span data-stu-id="9b9f8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9f8-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b9f8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9b9f8-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b9f8-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9b9f8-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b9f8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9b9f8-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9b9f8-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9b9f8-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b9f8-138">Namespace</span></span><br/>                | <span data-ttu-id="9b9f8-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9b9f8-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9b9f8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="9b9f8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b9f8-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b9f8-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b9f8-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b9f8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b9f8-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b9f8-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9b9f8-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b9f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9f8-145">**\_Servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="9b9f8-145">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 





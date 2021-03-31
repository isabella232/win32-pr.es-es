---
description: Representa una colección de instantáneas del sistema virtual.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Msvm_SnapshotCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155540"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="46e87-103">MSVM \_ SnapshotCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="46e87-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="46e87-104">Representa una colección de instantáneas del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="46e87-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="46e87-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="46e87-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e87-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46e87-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="46e87-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="46e87-107">Members</span></span>

<span data-ttu-id="46e87-108">La clase **MSVM \_ SnapshotCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="46e87-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="46e87-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46e87-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46e87-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46e87-110">Properties</span></span>

<span data-ttu-id="46e87-111">La clase **MSVM \_ SnapshotCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46e87-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46e87-112">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="46e87-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e87-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="46e87-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e87-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46e87-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e87-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="46e87-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="46e87-116">Identificación única del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="46e87-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="46e87-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="46e87-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46e87-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="46e87-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46e87-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46e87-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46e87-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="46e87-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="46e87-121">Nombre definido por el usuario para la colección.</span><span class="sxs-lookup"><span data-stu-id="46e87-121">An user-defined name for the collection.</span></span> <span data-ttu-id="46e87-122">Tenga en cuenta que no se garantiza que sea único.</span><span class="sxs-lookup"><span data-stu-id="46e87-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46e87-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e87-123">Requirements</span></span>



| <span data-ttu-id="46e87-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e87-124">Requirement</span></span> | <span data-ttu-id="46e87-125">Value</span><span class="sxs-lookup"><span data-stu-id="46e87-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e87-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46e87-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="46e87-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="46e87-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46e87-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="46e87-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="46e87-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46e87-130">Namespace</span></span><br/>                | <span data-ttu-id="46e87-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="46e87-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46e87-132">MOF</span><span class="sxs-lookup"><span data-stu-id="46e87-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46e87-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46e87-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46e87-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46e87-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e87-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46e87-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46e87-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="46e87-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e87-137">**\_Colección CIM**</span><span class="sxs-lookup"><span data-stu-id="46e87-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 


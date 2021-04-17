---
description: Asocia el \_ SnapshotCollection MSVM a los objetos MSVM \_ VirtualSystemSettingData incluidos.
ms.assetid: 21005e8a-0bc6-4ea7-8f6f-d79803b43bc0
title: Msvm_CollectedSnapshots (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedSnapshots
- Msvm_CollectedSnapshots.Collection
- Msvm_CollectedSnapshots.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9c89e7c7390cc1f2cc0c3217fca93e3f2d2d01ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666757"
---
# <a name="msvm_collectedsnapshots-class"></a><span data-ttu-id="ad3c1-103">MSVM \_ CollectedSnapshots (clase)</span><span class="sxs-lookup"><span data-stu-id="ad3c1-103">Msvm\_CollectedSnapshots class</span></span>

<span data-ttu-id="ad3c1-104">Asocia el [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) a los objetos [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) incluidos.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the contained [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) objects.</span></span>

<span data-ttu-id="ad3c1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3c1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad3c1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedSnapshots : CIM_CollectedMSEs
{
  Msvm_SnapshotCollection       REF Collection;
  Msvm_VirtualSystemSettingData REF Member;
};
```

## <a name="members"></a><span data-ttu-id="ad3c1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad3c1-107">Members</span></span>

<span data-ttu-id="ad3c1-108">La clase **MSVM \_ CollectedSnapshots** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ad3c1-108">The **Msvm\_CollectedSnapshots** class has these types of members:</span></span>

-   [<span data-ttu-id="ad3c1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad3c1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad3c1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad3c1-110">Properties</span></span>

<span data-ttu-id="ad3c1-111">La clase **MSVM \_ CollectedSnapshots** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-111">The **Msvm\_CollectedSnapshots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad3c1-112">**Colección**</span><span class="sxs-lookup"><span data-stu-id="ad3c1-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad3c1-113">Tipo de datos: **MSVM \_ SnapshotCollection**</span><span class="sxs-lookup"><span data-stu-id="ad3c1-113">Data type: **Msvm\_SnapshotCollection**</span></span>
</dt> <dt>

<span data-ttu-id="ad3c1-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad3c1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad3c1-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span><span class="sxs-lookup"><span data-stu-id="ad3c1-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="ad3c1-116">Objeto de agrupación o contenedor de [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md) que representa la colección.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-116">An [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ad3c1-117">**Member**</span><span class="sxs-lookup"><span data-stu-id="ad3c1-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad3c1-118">Tipo de datos: **MSVM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="ad3c1-118">Data type: **Msvm\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="ad3c1-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad3c1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad3c1-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("miembro")</span><span class="sxs-lookup"><span data-stu-id="ad3c1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="ad3c1-121">[**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que contiene los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-121">An [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad3c1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad3c1-122">Requirements</span></span>



| <span data-ttu-id="ad3c1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad3c1-123">Requirement</span></span> | <span data-ttu-id="ad3c1-124">Value</span><span class="sxs-lookup"><span data-stu-id="ad3c1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3c1-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad3c1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad3c1-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad3c1-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ad3c1-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad3c1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad3c1-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ad3c1-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ad3c1-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad3c1-129">Namespace</span></span><br/>                | <span data-ttu-id="ad3c1-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ad3c1-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ad3c1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ad3c1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad3c1-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad3c1-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad3c1-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ad3c1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad3c1-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ad3c1-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ad3c1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad3c1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3c1-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="ad3c1-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 


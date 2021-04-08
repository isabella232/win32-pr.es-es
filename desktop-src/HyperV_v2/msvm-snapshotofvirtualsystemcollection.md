---
description: Asocia el \_ SnapshotCollection MSVM a los objetos MSVM \_ VirtualSystemCollection correspondientes.
ms.assetid: 4dbfe21f-e700-4266-aedb-236c57c424f6
title: Msvm_SnapshotOfVirtualSystemCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystemCollection
- Msvm_SnapshotOfVirtualSystemCollection.Antecedent
- Msvm_SnapshotOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae3c9c146cea8a8af98f4d3071ee7339d53eb6b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908446"
---
# <a name="msvm_snapshotofvirtualsystemcollection-class"></a><span data-ttu-id="3c24a-103">MSVM \_ SnapshotOfVirtualSystemCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="3c24a-103">Msvm\_SnapshotOfVirtualSystemCollection class</span></span>

<span data-ttu-id="3c24a-104">Asocia el [**\_ SnapshotCollection MSVM**](msvm-snapshotcollection.md) a los objetos [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="3c24a-104">Associates the [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="3c24a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3c24a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c24a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c24a-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3c24a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c24a-107">Members</span></span>

<span data-ttu-id="3c24a-108">La clase **MSVM \_ SnapshotOfVirtualSystemCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3c24a-108">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="3c24a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c24a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c24a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c24a-110">Properties</span></span>

<span data-ttu-id="3c24a-111">La clase **MSVM \_ SnapshotOfVirtualSystemCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3c24a-111">The **Msvm\_SnapshotOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c24a-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3c24a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c24a-113">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="3c24a-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="3c24a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3c24a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c24a-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3c24a-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3c24a-116">Un objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) que representa el objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="3c24a-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3c24a-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3c24a-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c24a-118">Tipo de datos **: \_ colección CIM**</span><span class="sxs-lookup"><span data-stu-id="3c24a-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="3c24a-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3c24a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c24a-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="3c24a-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3c24a-121">[**\_ Colección CIM**](cim-collection.md) que representa el objeto que depende del **antecedente.**</span><span class="sxs-lookup"><span data-stu-id="3c24a-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent.**</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c24a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c24a-122">Requirements</span></span>



| <span data-ttu-id="3c24a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c24a-123">Requirement</span></span> | <span data-ttu-id="3c24a-124">Value</span><span class="sxs-lookup"><span data-stu-id="3c24a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c24a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c24a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3c24a-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c24a-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c24a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c24a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3c24a-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c24a-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3c24a-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3c24a-129">Namespace</span></span><br/>                | <span data-ttu-id="3c24a-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3c24a-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c24a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3c24a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c24a-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c24a-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c24a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c24a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c24a-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c24a-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c24a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c24a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c24a-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3c24a-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


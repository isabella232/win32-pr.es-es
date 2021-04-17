---
description: Asocia el \_ ReferencePointCollection MSVM a los objetos MSVM \_ VirtualSystemCollection correspondientes.
ms.assetid: 847f1f46-364f-4c91-b9e8-4740d3da1947
title: Msvm_ReferencePointOfVirtualSystemCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointOfVirtualSystemCollection
- Msvm_ReferencePointOfVirtualSystemCollection.Antecedent
- Msvm_ReferencePointOfVirtualSystemCollection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0919b8666915817d8475908b0305e90ea39e60f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652714"
---
# <a name="msvm_referencepointofvirtualsystemcollection-class"></a><span data-ttu-id="95c17-103">MSVM \_ ReferencePointOfVirtualSystemCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="95c17-103">Msvm\_ReferencePointOfVirtualSystemCollection class</span></span>

<span data-ttu-id="95c17-104">Asocia el [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) a los objetos [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) correspondientes.</span><span class="sxs-lookup"><span data-stu-id="95c17-104">Associates the [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) to the corresponding [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) objects.</span></span>

<span data-ttu-id="95c17-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="95c17-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c17-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95c17-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointOfVirtualSystemCollection : CIM_Dependency
{
  CIM_CollectionOfMSEs REF Antecedent;
  CIM_Collection       REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="95c17-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95c17-107">Members</span></span>

<span data-ttu-id="95c17-108">La clase **MSVM \_ ReferencePointOfVirtualSystemCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95c17-108">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="95c17-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95c17-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95c17-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95c17-110">Properties</span></span>

<span data-ttu-id="95c17-111">La clase **MSVM \_ ReferencePointOfVirtualSystemCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95c17-111">The **Msvm\_ReferencePointOfVirtualSystemCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95c17-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="95c17-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95c17-113">Tipo de datos: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="95c17-113">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="95c17-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95c17-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95c17-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="95c17-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="95c17-116">Un objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) que representa el objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="95c17-116">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) that represents the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="95c17-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="95c17-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95c17-118">Tipo de datos **: \_ colección CIM**</span><span class="sxs-lookup"><span data-stu-id="95c17-118">Data type: **CIM\_Collection**</span></span>
</dt> <dt>

<span data-ttu-id="95c17-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95c17-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95c17-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="95c17-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="95c17-121">[**\_ Colección CIM**](cim-collection.md) que representa el objeto que depende del **antecedente**.</span><span class="sxs-lookup"><span data-stu-id="95c17-121">A [**CIM\_Collection**](cim-collection.md) that represents the object that is dependent on the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95c17-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c17-122">Requirements</span></span>



| <span data-ttu-id="95c17-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="95c17-123">Requirement</span></span> | <span data-ttu-id="95c17-124">Value</span><span class="sxs-lookup"><span data-stu-id="95c17-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c17-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95c17-125">Minimum supported client</span></span><br/> | <span data-ttu-id="95c17-126">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="95c17-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="95c17-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95c17-127">Minimum supported server</span></span><br/> | <span data-ttu-id="95c17-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="95c17-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="95c17-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95c17-129">Namespace</span></span><br/>                | <span data-ttu-id="95c17-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="95c17-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="95c17-131">MOF</span><span class="sxs-lookup"><span data-stu-id="95c17-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95c17-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95c17-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="95c17-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95c17-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95c17-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="95c17-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="95c17-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="95c17-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c17-136">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="95c17-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 


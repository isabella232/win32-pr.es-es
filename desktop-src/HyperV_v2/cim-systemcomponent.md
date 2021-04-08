---
description: Representa una asociación entre un sistema y uno de los elementos que lo componen.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: CIM_SystemComponent (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 79bb7d3807a93b2d29157a3377d6e6a9079bfe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908737"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a><span data-ttu-id="eeadc-103">CIM_SystemComponent (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="eeadc-103">CIM_SystemComponent class (Hyper-V management)</span></span>

<span data-ttu-id="eeadc-104">Representa una asociación entre un sistema y uno de los elementos que lo componen.</span><span class="sxs-lookup"><span data-stu-id="eeadc-104">Represents an association between a system and one of the elements that compose it.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeadc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeadc-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="eeadc-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="eeadc-106">Members</span></span>

<span data-ttu-id="eeadc-107">La clase **CIM \_ SystemComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eeadc-107">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="eeadc-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeadc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eeadc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eeadc-109">Properties</span></span>

<span data-ttu-id="eeadc-110">La clase **CIM \_ SystemComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eeadc-110">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eeadc-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="eeadc-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeadc-112">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="eeadc-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="eeadc-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eeadc-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeadc-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="eeadc-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="eeadc-115">[**\_ Sistema CIM**](cim-system.md) que contiene el **PartComponent**.</span><span class="sxs-lookup"><span data-stu-id="eeadc-115">The [**CIM\_System**](cim-system.md) that contains the **PartComponent**.</span></span>

</dd> <dt>

<span data-ttu-id="eeadc-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="eeadc-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eeadc-117">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="eeadc-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="eeadc-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eeadc-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eeadc-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="eeadc-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="eeadc-120">El [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) secundario que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="eeadc-120">The child [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eeadc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeadc-121">Requirements</span></span>



| <span data-ttu-id="eeadc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeadc-122">Requirement</span></span> | <span data-ttu-id="eeadc-123">Value</span><span class="sxs-lookup"><span data-stu-id="eeadc-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeadc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeadc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eeadc-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eeadc-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="eeadc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eeadc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eeadc-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eeadc-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="eeadc-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eeadc-128">Namespace</span></span><br/>                | <span data-ttu-id="eeadc-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="eeadc-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eeadc-130">MOF</span><span class="sxs-lookup"><span data-stu-id="eeadc-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeadc-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeadc-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeadc-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeadc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeadc-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eeadc-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eeadc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeadc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeadc-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="eeadc-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 


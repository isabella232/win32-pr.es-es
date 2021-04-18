---
description: Asocia un sistema a un dispositivo lógico que es un componente del sistema.
ms.assetid: d5a36f71-5ebe-46e2-aaa9-5d99fa075d31
title: CIM_SystemDevice (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.GroupComponent
- CIM_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b02921e4be0f8aa0cddc194a2ed430e10e115eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687351"
---
# <a name="cim_systemdevice-class-hyper-v-management"></a><span data-ttu-id="d705d-103">CIM_SystemDevice (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="d705d-103">CIM_SystemDevice class (Hyper-V management)</span></span>

<span data-ttu-id="d705d-104">Asocia un sistema a un dispositivo lógico que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="d705d-104">Associates a system with a logical device that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d705d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d705d-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d705d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d705d-106">Members</span></span>

<span data-ttu-id="d705d-107">La clase **CIM \_ SystemDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d705d-107">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="d705d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d705d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d705d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d705d-109">Properties</span></span>

<span data-ttu-id="d705d-110">La clase **CIM \_ SystemDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d705d-110">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d705d-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d705d-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d705d-112">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="d705d-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="d705d-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d705d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d705d-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d705d-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d705d-115">Referencia [**\_ del sistema CIM**](cim-system.md) al sistema principal de la asociación.</span><span class="sxs-lookup"><span data-stu-id="d705d-115">A [**CIM\_System**](cim-system.md) reference to the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d705d-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d705d-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d705d-117">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="d705d-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d705d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d705d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d705d-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d705d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d705d-120">Una referencia de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) al dispositivo lógico que es un componente del sistema.</span><span class="sxs-lookup"><span data-stu-id="d705d-120">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) reference to the logical device that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d705d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d705d-121">Requirements</span></span>



| <span data-ttu-id="d705d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d705d-122">Requirement</span></span> | <span data-ttu-id="d705d-123">Value</span><span class="sxs-lookup"><span data-stu-id="d705d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d705d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d705d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d705d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d705d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d705d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d705d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d705d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d705d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d705d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d705d-128">Namespace</span></span><br/>                | <span data-ttu-id="d705d-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d705d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d705d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d705d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d705d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d705d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d705d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d705d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d705d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d705d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d705d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d705d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d705d-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d705d-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 


---
description: Asocia un dispositivo lógico al sistema primario.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652373"
---
# <a name="msvm_systemdevice-class"></a><span data-ttu-id="3fa52-103">MSVM \_ SystemDevice (clase)</span><span class="sxs-lookup"><span data-stu-id="3fa52-103">Msvm\_SystemDevice class</span></span>

<span data-ttu-id="3fa52-104">Un sistema puede agregar dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="3fa52-104">Logical devices can be aggregated by a system.</span></span> <span data-ttu-id="3fa52-105">Esta relación se hace explícita mediante la Asociación de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fa52-105">This relationship is made explicit by the system device association.</span></span>

<span data-ttu-id="3fa52-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3fa52-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa52-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fa52-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="3fa52-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fa52-108">Members</span></span>

<span data-ttu-id="3fa52-109">La clase **MSVM \_ SystemDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3fa52-109">The **Msvm\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3fa52-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fa52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fa52-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fa52-111">Properties</span></span>

<span data-ttu-id="3fa52-112">La clase **MSVM \_ SystemDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3fa52-112">The **Msvm\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fa52-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3fa52-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa52-114">Tipo de datos: **[ **\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="3fa52-114">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="3fa52-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa52-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa52-116">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3fa52-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 ), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="3fa52-117">Sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="3fa52-117">The parent system in the association.</span></span> <span data-ttu-id="3fa52-118">Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="3fa52-118">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="3fa52-119">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3fa52-119">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa52-120">Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="3fa52-120">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="3fa52-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3fa52-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fa52-122">Dispositivo lógico que es un elemento de un sistema.</span><span class="sxs-lookup"><span data-stu-id="3fa52-122">The logical device that is an element of a system.</span></span> <span data-ttu-id="3fa52-123">Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="3fa52-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fa52-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fa52-124">Remarks</span></span>

<span data-ttu-id="3fa52-125">El acceso a la clase **MSVM \_ SystemDevice** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3fa52-125">Access to the **Msvm\_SystemDevice** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3fa52-126">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3fa52-126">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa52-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa52-127">Requirements</span></span>



| <span data-ttu-id="3fa52-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa52-128">Requirement</span></span> | <span data-ttu-id="3fa52-129">Value</span><span class="sxs-lookup"><span data-stu-id="3fa52-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa52-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fa52-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa52-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fa52-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fa52-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fa52-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa52-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fa52-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fa52-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3fa52-134">Namespace</span></span><br/>                | <span data-ttu-id="3fa52-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3fa52-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fa52-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3fa52-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fa52-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fa52-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fa52-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3fa52-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa52-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fa52-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fa52-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fa52-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa52-141">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fa52-141">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dt>

[<span data-ttu-id="3fa52-142">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fa52-142">**CIM\_SystemDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[<span data-ttu-id="3fa52-143">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="3fa52-143">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


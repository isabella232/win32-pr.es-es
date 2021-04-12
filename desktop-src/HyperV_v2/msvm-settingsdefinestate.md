---
description: Asocia una máquina virtual y sus dispositivos con instancias del \_ objeto SettingData de CIM que representan la configuración actual que se aplica a estos objetos.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277570"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="94c36-103">MSVM \_ SettingsDefineState (clase)</span><span class="sxs-lookup"><span data-stu-id="94c36-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="94c36-104">Asocia una máquina virtual y sus dispositivos con instancias del [**objeto \_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) que representan la configuración actual que se aplica a estos objetos.</span><span class="sxs-lookup"><span data-stu-id="94c36-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="94c36-105">Más específicamente, asocia [**MSVM \_ ComputerSystem**](msvm-computersystem.md) con instancias de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)y asocia \**MSVM \_ \** _ derivados de _ el [*\_ LogicalDevice* \* de CIM](/windows/desktop/CIMWin32Prov/cim-logicaldevice) con \**MSVM \_ \** _ derivados de [_ *CIM \_ ResourceAllocationSettingData*. \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)</span><span class="sxs-lookup"><span data-stu-id="94c36-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="94c36-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="94c36-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="94c36-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94c36-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="94c36-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="94c36-108">Members</span></span>

<span data-ttu-id="94c36-109">La clase **MSVM \_ SettingsDefineState** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94c36-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="94c36-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94c36-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94c36-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94c36-111">Properties</span></span>

<span data-ttu-id="94c36-112">La clase **MSVM \_ SettingsDefineState** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94c36-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94c36-113">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="94c36-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94c36-114">Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="94c36-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="94c36-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94c36-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94c36-116">Referencia a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="94c36-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="94c36-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="94c36-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94c36-118">Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="94c36-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="94c36-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="94c36-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94c36-120">Referencia a la configuración actual de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="94c36-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94c36-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94c36-121">Remarks</span></span>

<span data-ttu-id="94c36-122">El acceso a la clase **MSVM \_ SettingsDefineState** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="94c36-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="94c36-123">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="94c36-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="94c36-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94c36-124">Requirements</span></span>



| <span data-ttu-id="94c36-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="94c36-125">Requirement</span></span> | <span data-ttu-id="94c36-126">Value</span><span class="sxs-lookup"><span data-stu-id="94c36-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94c36-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c36-127">Minimum supported client</span></span><br/> | <span data-ttu-id="94c36-128">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="94c36-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="94c36-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94c36-129">Minimum supported server</span></span><br/> | <span data-ttu-id="94c36-130">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="94c36-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="94c36-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94c36-131">Namespace</span></span><br/>                | <span data-ttu-id="94c36-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="94c36-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="94c36-133">MOF</span><span class="sxs-lookup"><span data-stu-id="94c36-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="94c36-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="94c36-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="94c36-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94c36-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94c36-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="94c36-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="94c36-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="94c36-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c36-138">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="94c36-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="94c36-139">**\_SETTINGSDEFINESTATE CIM**</span><span class="sxs-lookup"><span data-stu-id="94c36-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="94c36-140">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="94c36-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


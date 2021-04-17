---
description: Una asociación entre una instancia de MSVM \_ VirtualSystemSettingData y la instancia de MSVM \_ VirtualSystemSettingData que representa la instantánea más reciente en la que se basa este objeto.
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Msvm_ParentChildSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669763"
---
# <a name="msvm_parentchildsettingdata-class"></a><span data-ttu-id="39b35-103">MSVM \_ ParentChildSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="39b35-103">Msvm\_ParentChildSettingData class</span></span>

<span data-ttu-id="39b35-104">Una asociación entre una instancia de [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) y la instancia de **MSVM \_ VirtualSystemSettingData** que representa la instantánea más reciente en la que se basa este objeto.</span><span class="sxs-lookup"><span data-stu-id="39b35-104">An association between an instance of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) and the **Msvm\_VirtualSystemSettingData** instance that represents the most recent snapshot upon which this object is based.</span></span>

<span data-ttu-id="39b35-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="39b35-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b35-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39b35-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="39b35-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="39b35-107">Members</span></span>

<span data-ttu-id="39b35-108">La clase **MSVM \_ ParentChildSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39b35-108">The **Msvm\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="39b35-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39b35-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39b35-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39b35-110">Properties</span></span>

<span data-ttu-id="39b35-111">La clase **MSVM \_ ParentChildSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="39b35-111">The **Msvm\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39b35-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="39b35-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39b35-113">Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="39b35-113">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="39b35-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39b35-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39b35-115">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. antecedente")</span><span class="sxs-lookup"><span data-stu-id="39b35-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="39b35-116">Los datos de configuración de instantáneas en los que se basan los datos de configuración secundarios.</span><span class="sxs-lookup"><span data-stu-id="39b35-116">The snapshot setting data upon which the child setting data is based.</span></span>

</dd> <dt>

<span data-ttu-id="39b35-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="39b35-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39b35-118">Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="39b35-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="39b35-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39b35-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39b35-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency. Dependent")</span><span class="sxs-lookup"><span data-stu-id="39b35-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="39b35-121">Los datos de configuración de la máquina virtual que representa el elemento secundario del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="39b35-121">The setting data for the virtual machine that represents the child of the parent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39b35-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39b35-122">Remarks</span></span>

<span data-ttu-id="39b35-123">El acceso a la clase **MSVM \_ ParentChildSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="39b35-123">Access to the **Msvm\_ParentChildSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="39b35-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="39b35-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="39b35-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39b35-125">Requirements</span></span>



| <span data-ttu-id="39b35-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="39b35-126">Requirement</span></span> | <span data-ttu-id="39b35-127">Value</span><span class="sxs-lookup"><span data-stu-id="39b35-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39b35-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39b35-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39b35-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="39b35-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39b35-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39b35-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39b35-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="39b35-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39b35-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39b35-132">Namespace</span></span><br/>                | <span data-ttu-id="39b35-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="39b35-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39b35-134">MOF</span><span class="sxs-lookup"><span data-stu-id="39b35-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39b35-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39b35-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39b35-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39b35-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b35-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39b35-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39b35-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="39b35-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b35-139">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="39b35-139">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="39b35-140">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="39b35-140">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[<span data-ttu-id="39b35-141">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="39b35-141">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 


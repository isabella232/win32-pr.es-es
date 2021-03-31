---
description: Se usa para asociar una máquina virtual a su BIOS.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153898"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="2f8c9-103">MSVM \_ SystemBIOS (clase)</span><span class="sxs-lookup"><span data-stu-id="2f8c9-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="2f8c9-104">Se usa para asociar una máquina virtual a su BIOS.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="2f8c9-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f8c9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f8c9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2f8c9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f8c9-107">Members</span></span>

<span data-ttu-id="2f8c9-108">La clase **MSVM \_ SystemBIOS** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2f8c9-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="2f8c9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f8c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f8c9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f8c9-110">Properties</span></span>

<span data-ttu-id="2f8c9-111">La clase **MSVM \_ SystemBIOS** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f8c9-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2f8c9-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8c9-113">Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="2f8c9-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2f8c9-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f8c9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8c9-115">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2f8c9-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2f8c9-116">La máquina virtual que se inicia desde el BIOS.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="2f8c9-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2f8c9-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f8c9-118">Tipo de datos: **[ **MSVM \_ BIOSElement**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="2f8c9-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2f8c9-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2f8c9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f8c9-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2f8c9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2f8c9-121">BIOS asociado a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f8c9-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f8c9-122">Remarks</span></span>

<span data-ttu-id="2f8c9-123">El acceso a la clase **MSVM \_ SystemBIOS** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2f8c9-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2f8c9-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2f8c9-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8c9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f8c9-125">Requirements</span></span>



| <span data-ttu-id="2f8c9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f8c9-126">Requirement</span></span> | <span data-ttu-id="2f8c9-127">Value</span><span class="sxs-lookup"><span data-stu-id="2f8c9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8c9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f8c9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8c9-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f8c9-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f8c9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f8c9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8c9-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2f8c9-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f8c9-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f8c9-132">Namespace</span></span><br/>                | <span data-ttu-id="2f8c9-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2f8c9-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f8c9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2f8c9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f8c9-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f8c9-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f8c9-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f8c9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f8c9-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f8c9-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f8c9-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f8c9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8c9-139">**\_SYSTEMBIOS CIM**</span><span class="sxs-lookup"><span data-stu-id="2f8c9-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="2f8c9-140">Clases de BIOS</span><span class="sxs-lookup"><span data-stu-id="2f8c9-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 


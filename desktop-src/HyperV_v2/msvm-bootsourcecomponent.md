---
description: Asocia el BootSourceSettingData de MSVM \_ al MSVM general \_ VirtualSystemSettingData.
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Msvm_BootSourceComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666691"
---
# <a name="msvm_bootsourcecomponent-class"></a><span data-ttu-id="8e334-103">MSVM \_ BootSourceComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="8e334-103">Msvm\_BootSourceComponent class</span></span>

<span data-ttu-id="8e334-104">Asocia el [**\_ BootSourceSettingData de MSVM**](msvm-bootsourcesettingdata.md) al [**MSVM general \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="8e334-104">Associates the [**Msvm\_BootSourceSettingData**](msvm-bootsourcesettingdata.md) to the overall [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md).</span></span> <span data-ttu-id="8e334-105">Esta clase se deriva del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="8e334-105">This class derives from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

<span data-ttu-id="8e334-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8e334-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e334-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e334-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="8e334-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e334-108">Members</span></span>

<span data-ttu-id="8e334-109">La clase **MSVM \_ BootSourceComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8e334-109">The **Msvm\_BootSourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8e334-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e334-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e334-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e334-111">Properties</span></span>

<span data-ttu-id="8e334-112">La clase **MSVM \_ BootSourceComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8e334-112">The **Msvm\_BootSourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e334-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="8e334-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e334-114">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="8e334-114">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="8e334-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e334-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e334-116">Referencia al elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="8e334-116">Reference to the parent element in the association.</span></span> <span data-ttu-id="8e334-117">Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="8e334-117">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e334-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="8e334-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e334-119">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="8e334-119">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="8e334-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e334-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e334-121">Referencia al elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="8e334-121">Reference to the child element in the association.</span></span> <span data-ttu-id="8e334-122">Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="8e334-122">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e334-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e334-123">Requirements</span></span>



| <span data-ttu-id="8e334-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e334-124">Requirement</span></span> | <span data-ttu-id="8e334-125">Value</span><span class="sxs-lookup"><span data-stu-id="8e334-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e334-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e334-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8e334-127">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="8e334-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8e334-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e334-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8e334-129">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e334-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8e334-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e334-130">Namespace</span></span><br/>                | <span data-ttu-id="8e334-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8e334-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8e334-132">MOF</span><span class="sxs-lookup"><span data-stu-id="8e334-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e334-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e334-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e334-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e334-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e334-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e334-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e334-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e334-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e334-137">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="8e334-137">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="8e334-138">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="8e334-138">**CIM\_Component**</span></span>](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[<span data-ttu-id="8e334-139">**MSVM \_ BootSourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="8e334-139">**Msvm\_BootSourceSettingData**</span></span>](msvm-bootsourcesettingdata.md)
</dt> <dt>

[<span data-ttu-id="8e334-140">**MSVM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="8e334-140">**Msvm\_VirtualSystemSettingData**</span></span>](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 


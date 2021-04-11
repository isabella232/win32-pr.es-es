---
description: Representa la configuración para el servicio 3D sintético presente en un sistema host único.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Msvm_Synthetic3DServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155920"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="e7a41-103">MSVM \_ Synthetic3DServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="e7a41-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="e7a41-104">Representa la configuración para el servicio 3D sintético presente en un sistema host único.</span><span class="sxs-lookup"><span data-stu-id="e7a41-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="e7a41-105">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="e7a41-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="e7a41-106">El cliente debe llamar al método [**MSVM \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7a41-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="e7a41-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e7a41-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7a41-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="e7a41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7a41-109">Members</span></span>

<span data-ttu-id="e7a41-110">La clase **MSVM \_ Synthetic3DServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e7a41-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e7a41-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7a41-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7a41-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7a41-112">Properties</span></span>

<span data-ttu-id="e7a41-113">La clase **MSVM \_ Synthetic3DServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7a41-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7a41-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e7a41-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7a41-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7a41-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7a41-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7a41-117">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7a41-117">A short description of the object.</span></span> <span data-ttu-id="e7a41-118">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e7a41-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e7a41-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7a41-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7a41-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7a41-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7a41-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7a41-122">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7a41-122">A description of the object.</span></span> <span data-ttu-id="e7a41-123">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e7a41-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e7a41-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e7a41-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7a41-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7a41-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7a41-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7a41-127">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7a41-127">A display name for the object.</span></span> <span data-ttu-id="e7a41-128">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e7a41-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e7a41-129">**GPUOvercommitEnabled**</span><span class="sxs-lookup"><span data-stu-id="e7a41-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7a41-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e7a41-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7a41-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7a41-132">Controla si la asignación de máquina virtual tiene en cuenta las limitaciones de memoria de la GPU.</span><span class="sxs-lookup"><span data-stu-id="e7a41-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="e7a41-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e7a41-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7a41-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7a41-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7a41-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7a41-136">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e7a41-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e7a41-137">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e7a41-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e7a41-138">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e7a41-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7a41-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7a41-139">Requirements</span></span>



| <span data-ttu-id="e7a41-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a41-140">Requirement</span></span> | <span data-ttu-id="e7a41-141">Value</span><span class="sxs-lookup"><span data-stu-id="e7a41-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a41-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7a41-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a41-143">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7a41-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7a41-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7a41-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a41-145">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7a41-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7a41-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7a41-146">Namespace</span></span><br/>                | <span data-ttu-id="e7a41-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7a41-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7a41-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e7a41-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7a41-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7a41-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7a41-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7a41-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7a41-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7a41-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


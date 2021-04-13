---
description: Representa el estado configurado del dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543582"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="08a56-103">MSVM \_ TPMSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="08a56-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="08a56-104">Representa el estado configurado del dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="08a56-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="08a56-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="08a56-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a56-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08a56-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="08a56-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="08a56-107">Members</span></span>

<span data-ttu-id="08a56-108">La clase **MSVM \_ TPMSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="08a56-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="08a56-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08a56-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08a56-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08a56-110">Properties</span></span>

<span data-ttu-id="08a56-111">La clase **MSVM \_ TPMSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="08a56-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08a56-112">**DataProtector**</span><span class="sxs-lookup"><span data-stu-id="08a56-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a56-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08a56-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08a56-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08a56-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08a56-115">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08a56-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08a56-116">**true** para establecer una directiva que proteja los datos de una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="08a56-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="08a56-117">Un TPM recién creado está deshabilitado, por lo que el estado inicial de protección de datos es **false**.</span><span class="sxs-lookup"><span data-stu-id="08a56-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="08a56-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="08a56-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a56-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08a56-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08a56-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08a56-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08a56-121">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08a56-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08a56-122">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="08a56-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="08a56-123">El valor predeterminado es **Disabled**.</span><span class="sxs-lookup"><span data-stu-id="08a56-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="08a56-124">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="08a56-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="08a56-125">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="08a56-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08a56-126">**KeyProtector**</span><span class="sxs-lookup"><span data-stu-id="08a56-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a56-127">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="08a56-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="08a56-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08a56-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08a56-129">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="08a56-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="08a56-130">El protector de clave del cliente del servicio de protección de host.</span><span class="sxs-lookup"><span data-stu-id="08a56-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="08a56-131">**LastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="08a56-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a56-132">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="08a56-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="08a56-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08a56-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08a56-134">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span><span class="sxs-lookup"><span data-stu-id="08a56-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="08a56-135">El último protector de clave válida conocida cifró correctamente el estado del dispositivo de TPM en el último arranque de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08a56-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="08a56-136">Esta propiedad es de solo lectura para el cliente WMI y solo la puede modificar el dispositivo TPM de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="08a56-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="08a56-137">**Blindada**</span><span class="sxs-lookup"><span data-stu-id="08a56-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a56-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08a56-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08a56-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08a56-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08a56-140">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08a56-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08a56-141">**true** para definir una directiva que blinda una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="08a56-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="08a56-142">Un TPM recién creado está deshabilitado, por lo que el estado de blindaje inicial es **false**.</span><span class="sxs-lookup"><span data-stu-id="08a56-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08a56-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a56-143">Requirements</span></span>



| <span data-ttu-id="08a56-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a56-144">Requirement</span></span> | <span data-ttu-id="08a56-145">Value</span><span class="sxs-lookup"><span data-stu-id="08a56-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a56-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08a56-146">Minimum supported client</span></span><br/> | <span data-ttu-id="08a56-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="08a56-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="08a56-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08a56-148">Minimum supported server</span></span><br/> | <span data-ttu-id="08a56-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="08a56-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="08a56-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="08a56-150">End of client support</span></span><br/>    | <span data-ttu-id="08a56-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="08a56-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="08a56-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="08a56-152">End of server support</span></span><br/>    | <span data-ttu-id="08a56-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="08a56-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="08a56-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08a56-154">Namespace</span></span><br/>                | <span data-ttu-id="08a56-155">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="08a56-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="08a56-156">MOF</span><span class="sxs-lookup"><span data-stu-id="08a56-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08a56-157"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08a56-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08a56-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08a56-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a56-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08a56-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08a56-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="08a56-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a56-161">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="08a56-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 


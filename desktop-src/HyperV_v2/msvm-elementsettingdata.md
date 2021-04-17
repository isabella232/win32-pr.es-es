---
description: Asocia un elemento administrado a sus datos de configuración.
ms.assetid: 4DB78E43-E387-478E-999C-770B35925721
title: Msvm_ElementSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementSettingData
- Msvm_ElementSettingData.ManagedElement
- Msvm_ElementSettingData.SettingData
- Msvm_ElementSettingData.IsDefault
- Msvm_ElementSettingData.IsCurrent
- Msvm_ElementSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9f4d2af614e3b161f49a0d37d1e4d1ee48ce0aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686964"
---
# <a name="msvm_elementsettingdata-class"></a><span data-ttu-id="abd05-103">MSVM \_ ElementSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="abd05-103">Msvm\_ElementSettingData class</span></span>

<span data-ttu-id="abd05-104">Asocia un elemento administrado a sus datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="abd05-104">Associates a managed element with its configuration data.</span></span> <span data-ttu-id="abd05-105">Algunas de las aplicaciones más importantes de esta asociación se usan en la vinculación de una máquina virtual y los dispositivos lógicos que se han asignado a ese sistema con su información de configuración de instantánea.</span><span class="sxs-lookup"><span data-stu-id="abd05-105">Some of the more notable applications of this association are its use in linking a virtual machine and the logical devices that have been assigned to that system with their snapshot configuration information.</span></span> <span data-ttu-id="abd05-106">La información de configuración actual está asociada a la máquina virtual y sus dispositivos a través de la Asociación [**MSVM \_ SettingsDefineState**](msvm-settingsdefinestate.md) .</span><span class="sxs-lookup"><span data-stu-id="abd05-106">Current configuration information is associated with the virtual machine and its devices through the [**Msvm\_SettingsDefineState**](msvm-settingsdefinestate.md) association.</span></span>

<span data-ttu-id="abd05-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="abd05-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd05-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abd05-108">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementSettingData : CIM_ElementSettingData
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
  uint16                 IsDefault = 0;
  uint16                 IsCurrent = 0;
  uint16                 IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="abd05-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="abd05-109">Members</span></span>

<span data-ttu-id="abd05-110">La clase **MSVM \_ ElementSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="abd05-110">The **Msvm\_ElementSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="abd05-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abd05-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abd05-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abd05-112">Properties</span></span>

<span data-ttu-id="abd05-113">La clase **MSVM \_ ElementSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abd05-113">The **Msvm\_ElementSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abd05-114">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="abd05-114">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd05-115">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abd05-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abd05-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abd05-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd05-117">Indica que la configuración a la que se hace referencia se está usando actualmente en el funcionamiento del elemento o que esta información es desconocida.</span><span class="sxs-lookup"><span data-stu-id="abd05-117">Indicates that the referenced setting is currently being used in the operation of the element or that this information is unknown.</span></span> <span data-ttu-id="abd05-118">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="abd05-118">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="abd05-119">El valor predeterminado es 0 (desconocido).</span><span class="sxs-lookup"><span data-stu-id="abd05-119">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="abd05-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="abd05-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Es actual** (1)</span><span class="sxs-lookup"><span data-stu-id="abd05-121"><span id="Is_Current"></span><span id="is_current"></span><span id="IS_CURRENT"></span>**Is Current** (1)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**No es actual** (2)</span><span class="sxs-lookup"><span data-stu-id="abd05-122"><span id="Is_Not_Current"></span><span id="is_not_current"></span><span id="IS_NOT_CURRENT"></span>**Is Not Current** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="abd05-123">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="abd05-123">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd05-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abd05-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abd05-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abd05-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd05-126">Indica que la configuración a la que se hace referencia es un valor predeterminado para el elemento o que esta información es desconocida.</span><span class="sxs-lookup"><span data-stu-id="abd05-126">Indicates that the referenced setting is a default setting for the element or that this information is unknown.</span></span> <span data-ttu-id="abd05-127">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="abd05-127">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="abd05-128">El valor predeterminado es 0 (desconocido).</span><span class="sxs-lookup"><span data-stu-id="abd05-128">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="abd05-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="abd05-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Es el valor predeterminado** (1)</span><span class="sxs-lookup"><span data-stu-id="abd05-130"><span id="Is_Default"></span><span id="is_default"></span><span id="IS_DEFAULT"></span>**Is Default** (1)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**No es el valor predeterminado** (2)</span><span class="sxs-lookup"><span data-stu-id="abd05-131"><span id="Is_Not_Default"></span><span id="is_not_default"></span><span id="IS_NOT_DEFAULT"></span>**Is Not Default** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="abd05-132">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="abd05-132">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd05-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abd05-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="abd05-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abd05-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd05-135">Indica si el valor al que se hace referencia es el siguiente valor que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="abd05-135">Indicates whether the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="abd05-136">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="abd05-136">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span> <span data-ttu-id="abd05-137">El valor predeterminado es 0 (desconocido).</span><span class="sxs-lookup"><span data-stu-id="abd05-137">The default value is 0 (Unknown).</span></span>

<dl> <dt>

<span data-ttu-id="abd05-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="abd05-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Es Next** (1)</span><span class="sxs-lookup"><span data-stu-id="abd05-139"><span id="Is_Next"></span><span id="is_next"></span><span id="IS_NEXT"></span>**Is Next** (1)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**No es Next** (2)</span><span class="sxs-lookup"><span data-stu-id="abd05-140"><span id="Is_Not_Next"></span><span id="is_not_next"></span><span id="IS_NOT_NEXT"></span>**Is Not Next** (2)</span></span>
</dt> <dt>

<span data-ttu-id="abd05-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Siguiente para uso único** (3)</span><span class="sxs-lookup"><span data-stu-id="abd05-141"><span id="Is_Next_For_Single_Use"></span><span id="is_next_for_single_use"></span><span id="IS_NEXT_FOR_SINGLE_USE"></span>**Is Next For Single Use** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="abd05-142">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="abd05-142">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd05-143">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="abd05-143">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="abd05-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abd05-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd05-145">Referencia a la máquina virtual o el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="abd05-145">Reference to the virtual machine or virtual device.</span></span> <span data-ttu-id="abd05-146">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="abd05-146">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="abd05-147">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="abd05-147">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd05-148">Tipo de datos: **[ **\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="abd05-148">Data type: **[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="abd05-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abd05-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd05-150">Referencia a la configuración de instantáneas para la máquina virtual o el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="abd05-150">Reference to the snapshotted settings for the virtual machine or virtual device.</span></span> <span data-ttu-id="abd05-151">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="abd05-151">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abd05-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abd05-152">Remarks</span></span>

<span data-ttu-id="abd05-153">El acceso a la clase **MSVM \_ ElementSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="abd05-153">Access to the **Msvm\_ElementSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="abd05-154">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="abd05-154">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="abd05-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="abd05-155">Examples</span></span>

<span data-ttu-id="abd05-156">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="abd05-156">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd05-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abd05-157">Requirements</span></span>



| <span data-ttu-id="abd05-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd05-158">Requirement</span></span> | <span data-ttu-id="abd05-159">Value</span><span class="sxs-lookup"><span data-stu-id="abd05-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd05-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd05-160">Minimum supported client</span></span><br/> | <span data-ttu-id="abd05-161">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="abd05-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="abd05-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd05-162">Minimum supported server</span></span><br/> | <span data-ttu-id="abd05-163">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="abd05-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abd05-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abd05-164">Namespace</span></span><br/>                | <span data-ttu-id="abd05-165">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="abd05-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="abd05-166">MOF</span><span class="sxs-lookup"><span data-stu-id="abd05-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abd05-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abd05-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abd05-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abd05-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd05-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abd05-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abd05-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="abd05-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd05-171">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="abd05-171">**CIM\_ElementSettingData**</span></span>](cim-elementsettingdata.md)
</dt> <dt>

[<span data-ttu-id="abd05-172">**\_ELEMENTSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="abd05-172">**CIM\_ElementSettingData**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata)
</dt> <dt>

[<span data-ttu-id="abd05-173">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="abd05-173">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


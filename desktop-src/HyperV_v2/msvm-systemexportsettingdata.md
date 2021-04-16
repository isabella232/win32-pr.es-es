---
description: Asocia una máquina virtual y sus datos de configuración de exportación.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Msvm_SystemExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652374"
---
# <a name="msvm_systemexportsettingdata-class"></a><span data-ttu-id="48955-103">MSVM \_ SystemExportSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="48955-103">Msvm\_SystemExportSettingData class</span></span>

<span data-ttu-id="48955-104">Asocia una máquina virtual y sus datos de configuración de exportación.</span><span class="sxs-lookup"><span data-stu-id="48955-104">Associates a virtual machine and its export setting data.</span></span> <span data-ttu-id="48955-105">Antes de llamar al método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) , se puede recuperar una instancia de [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) mediante esta asociación.</span><span class="sxs-lookup"><span data-stu-id="48955-105">Before calling the [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class, an instance of [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) can be retrieved using this association.</span></span>

<span data-ttu-id="48955-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48955-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48955-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48955-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a><span data-ttu-id="48955-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="48955-108">Members</span></span>

<span data-ttu-id="48955-109">La clase **MSVM \_ SystemExportSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48955-109">The **Msvm\_SystemExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="48955-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48955-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48955-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48955-111">Properties</span></span>

<span data-ttu-id="48955-112">La clase **MSVM \_ SystemExportSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48955-112">The **Msvm\_SystemExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48955-113">**IsCurrent**</span><span class="sxs-lookup"><span data-stu-id="48955-113">**IsCurrent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48955-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48955-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48955-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48955-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48955-116">Indica si la configuración a la que se hace referencia se está utilizando actualmente en el funcionamiento del elemento o si esta información es desconocida.</span><span class="sxs-lookup"><span data-stu-id="48955-116">Indicates if the referenced setting is currently being used in the operation of the element, or that this information is unknown.</span></span> <span data-ttu-id="48955-117">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="48955-117">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="48955-118">Value</span><span class="sxs-lookup"><span data-stu-id="48955-118">Value</span></span>                                                                        | <span data-ttu-id="48955-119">Significado</span><span class="sxs-lookup"><span data-stu-id="48955-119">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="48955-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48955-120"><dt>0</dt></span></span> </dl> | <span data-ttu-id="48955-121">Unknown</span><span class="sxs-lookup"><span data-stu-id="48955-121">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="48955-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48955-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="48955-123">Current</span><span class="sxs-lookup"><span data-stu-id="48955-123">Current</span></span><br/>     |
| <dl> <span data-ttu-id="48955-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="48955-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="48955-125">No actual</span><span class="sxs-lookup"><span data-stu-id="48955-125">Not Current</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="48955-126">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="48955-126">**IsDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48955-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48955-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48955-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48955-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48955-129">Indica si la configuración a la que se hace referencia es un valor predeterminado para el elemento o si esta información es desconocida.</span><span class="sxs-lookup"><span data-stu-id="48955-129">Indicates if the referenced setting is a default setting for the element, or that this information is unknown.</span></span> <span data-ttu-id="48955-130">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="48955-130">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="48955-131">Value</span><span class="sxs-lookup"><span data-stu-id="48955-131">Value</span></span>                                                                        | <span data-ttu-id="48955-132">Significado</span><span class="sxs-lookup"><span data-stu-id="48955-132">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="48955-133"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48955-133"><dt>0</dt></span></span> </dl> | <span data-ttu-id="48955-134">Unknown</span><span class="sxs-lookup"><span data-stu-id="48955-134">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="48955-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48955-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="48955-136">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="48955-136">Default</span></span><br/>     |
| <dl> <span data-ttu-id="48955-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="48955-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="48955-138">No es el valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="48955-138">Not Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="48955-139">**IsNext**</span><span class="sxs-lookup"><span data-stu-id="48955-139">**IsNext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48955-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48955-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48955-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48955-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48955-142">Indica si la configuración a la que se hace referencia es la opción siguiente que se va a aplicar.</span><span class="sxs-lookup"><span data-stu-id="48955-142">Indicates whether or not the referenced setting is the next setting to be applied.</span></span> <span data-ttu-id="48955-143">Por ejemplo, la aplicación puede tener lugar en una solicitud de reinicialización, restablecimiento y reconfiguración.</span><span class="sxs-lookup"><span data-stu-id="48955-143">For example, the application could take place on a re-initialization, reset, reconfiguration request.</span></span> <span data-ttu-id="48955-144">Puede ser un valor de configuración permanente o una configuración usada solo una vez, como indica la marca.</span><span class="sxs-lookup"><span data-stu-id="48955-144">This could be a permanent setting, or a setting used only one time, as indicated by the flag.</span></span> <span data-ttu-id="48955-145">Si se trata de una configuración permanente, se aplica la configuración cada vez que se reinicializa el elemento administrado, hasta que esta marca se restablece manualmente.</span><span class="sxs-lookup"><span data-stu-id="48955-145">If it is a permanent setting then the setting is applied every time the managed element reinitializes, until this flag is manually reset.</span></span> <span data-ttu-id="48955-146">Sin embargo, si es de uso único, la marca se borra automáticamente después de aplicar la configuración.</span><span class="sxs-lookup"><span data-stu-id="48955-146">However, if it is single use, then the flag is automatically cleared after the settings are applied.</span></span> <span data-ttu-id="48955-147">Además, si se especifica esta marca (es decir, se establece en un valor distinto de 0 (desconocido)), esto tiene prioridad sobre cualquier dato de configuración que se pueda haber especificado como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="48955-147">Also, if this flag is specified (i.e. set to value other than 0 (Unknown)), then this takes precedence over any setting data that may have been specified as default.</span></span> <span data-ttu-id="48955-148">Por ejemplo: Si el elemento administrado es un sistema informático y el valor de esta marca es 1 (es el siguiente), la configuración será efectiva la próxima vez que se restablezca el sistema.</span><span class="sxs-lookup"><span data-stu-id="48955-148">For example: If the managed element is a computer system, and the value of this flag is 1 (Is Next), then the setting will be effective next time the system resets.</span></span> <span data-ttu-id="48955-149">Y, a menos que se cambie esta marca, se conservará para los restablecimientos del sistema posteriores.</span><span class="sxs-lookup"><span data-stu-id="48955-149">And, unless this flag is changed, it will persist for subsequent system resets.</span></span> <span data-ttu-id="48955-150">Sin embargo, si esta marca se establece en 3 (es la siguiente para un solo uso), esta configuración solo se usará una vez y la marca se restablecerá después de la 2 (no es siguiente).</span><span class="sxs-lookup"><span data-stu-id="48955-150">However, if this flag is set to 3 (Is Next For Single Use), then this setting will only be used once and the flag would be reset after that to 2 (Is Not Next).</span></span> <span data-ttu-id="48955-151">Por lo tanto, en el ejemplo anterior, si el sistema se reinicia en una sucesión rápida, la configuración no se utilizará en el segundo reinicio.</span><span class="sxs-lookup"><span data-stu-id="48955-151">So, in the above example, if the system reboots in a quick succession, the setting will not be used at the second reboot.</span></span>

<span data-ttu-id="48955-152">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="48955-152">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>



| <span data-ttu-id="48955-153">Value</span><span class="sxs-lookup"><span data-stu-id="48955-153">Value</span></span>                                                                        | <span data-ttu-id="48955-154">Significado</span><span class="sxs-lookup"><span data-stu-id="48955-154">Meaning</span></span>                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="48955-155"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="48955-155"><dt>0</dt></span></span> </dl> | <span data-ttu-id="48955-156">Unknown</span><span class="sxs-lookup"><span data-stu-id="48955-156">Unknown</span></span><br/>                |
| <dl> <span data-ttu-id="48955-157"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="48955-157"><dt>1</dt></span></span> </dl> | <span data-ttu-id="48955-158">Siguiente</span><span class="sxs-lookup"><span data-stu-id="48955-158">Is Next</span></span><br/>                |
| <dl> <span data-ttu-id="48955-159"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="48955-159"><dt>2</dt></span></span> </dl> | <span data-ttu-id="48955-160">No es siguiente</span><span class="sxs-lookup"><span data-stu-id="48955-160">Is Not Next</span></span><br/>            |
| <dl> <span data-ttu-id="48955-161"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="48955-161"><dt>3</dt></span></span> </dl> | <span data-ttu-id="48955-162">Siguiente para uso único</span><span class="sxs-lookup"><span data-stu-id="48955-162">Is Next For Single Use</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="48955-163">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="48955-163">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48955-164">Tipo de datos: **[ **CIM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="48955-164">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="48955-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48955-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48955-166">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. ManagedElement")</span><span class="sxs-lookup"><span data-stu-id="48955-166">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="48955-167">Referencia a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48955-167">Reference to the virtual machine.</span></span> <span data-ttu-id="48955-168">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="48955-168">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="48955-169">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="48955-169">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48955-170">Tipo de datos: **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="48955-170">Data type: **[**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="48955-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48955-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48955-172">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")</span><span class="sxs-lookup"><span data-stu-id="48955-172">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ElementSettingData.SettingData")</span></span>
</dt> </dl>

<span data-ttu-id="48955-173">Referencia a los datos de configuración de exportación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48955-173">Reference to the export setting data for the virtual machine.</span></span> <span data-ttu-id="48955-174">Esta propiedad se hereda de [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span><span class="sxs-lookup"><span data-stu-id="48955-174">This property is inherited from [**CIM\_ElementSettingData**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48955-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48955-175">Remarks</span></span>

<span data-ttu-id="48955-176">El acceso a la clase **MSVM \_ SystemExportSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="48955-176">Access to the **Msvm\_SystemExportSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="48955-177">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="48955-177">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="48955-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48955-178">Requirements</span></span>



| <span data-ttu-id="48955-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="48955-179">Requirement</span></span> | <span data-ttu-id="48955-180">Value</span><span class="sxs-lookup"><span data-stu-id="48955-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48955-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48955-181">Minimum supported client</span></span><br/> | <span data-ttu-id="48955-182">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="48955-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="48955-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48955-183">Minimum supported server</span></span><br/> | <span data-ttu-id="48955-184">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="48955-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48955-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48955-185">Namespace</span></span><br/>                | <span data-ttu-id="48955-186">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="48955-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="48955-187">MOF</span><span class="sxs-lookup"><span data-stu-id="48955-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48955-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48955-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48955-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48955-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48955-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48955-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


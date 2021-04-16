---
title: Win32_TerminalSetting (clase)
description: Representa la configuración que se puede aplicar a un terminal.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Win32_TerminalSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686158"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="5086e-105">\_Clase Win32 TerminalSetting</span><span class="sxs-lookup"><span data-stu-id="5086e-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="5086e-106">La clase WMI **\_ TerminalSetting de Win32** representa la configuración que se puede aplicar a un terminal.</span><span class="sxs-lookup"><span data-stu-id="5086e-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="5086e-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="5086e-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5086e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5086e-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="5086e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5086e-109">Members</span></span>

<span data-ttu-id="5086e-110">La **clase \_ TerminalSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5086e-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="5086e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5086e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5086e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5086e-112">Properties</span></span>

<span data-ttu-id="5086e-113">La **clase \_ TerminalSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5086e-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5086e-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5086e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5086e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5086e-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5086e-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5086e-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="5086e-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5086e-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5086e-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5086e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5086e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5086e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5086e-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5086e-123">Description of the object.</span></span>

<span data-ttu-id="5086e-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5086e-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5086e-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5086e-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5086e-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5086e-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5086e-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5086e-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5086e-129">The date the object was installed.</span></span> <span data-ttu-id="5086e-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="5086e-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5086e-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5086e-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5086e-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5086e-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5086e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5086e-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="5086e-135">The name of the object.</span></span>

<span data-ttu-id="5086e-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5086e-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5086e-137">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5086e-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5086e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5086e-140">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5086e-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5086e-141">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5086e-141">Current status of the object.</span></span> <span data-ttu-id="5086e-142">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="5086e-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5086e-143">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5086e-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5086e-144">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5086e-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5086e-145">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5086e-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5086e-146">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5086e-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5086e-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5086e-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5086e-148">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="5086e-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-149">("Error")</span><span class="sxs-lookup"><span data-stu-id="5086e-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-150">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="5086e-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-151">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="5086e-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-152">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5086e-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-153">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5086e-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-154">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="5086e-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5086e-155">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="5086e-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5086e-156">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="5086e-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5086e-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5086e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5086e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5086e-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5086e-159">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="5086e-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5086e-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5086e-160">Remarks</span></span>

<span data-ttu-id="5086e-161">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5086e-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5086e-162">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5086e-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5086e-163">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5086e-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5086e-164">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5086e-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5086e-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5086e-165">Requirements</span></span>



| <span data-ttu-id="5086e-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5086e-166">Requirement</span></span> | <span data-ttu-id="5086e-167">Value</span><span class="sxs-lookup"><span data-stu-id="5086e-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5086e-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5086e-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5086e-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5086e-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5086e-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5086e-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5086e-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5086e-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5086e-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5086e-172">Namespace</span></span><br/>                | <span data-ttu-id="5086e-173">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5086e-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5086e-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5086e-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5086e-175"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5086e-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5086e-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5086e-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5086e-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5086e-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5086e-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="5086e-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5086e-179">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5086e-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="5086e-180">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="5086e-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="5086e-181">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="5086e-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


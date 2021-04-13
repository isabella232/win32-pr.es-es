---
title: Win32_TerminalServiceToSetting (clase)
description: Representa la asociación entre una instancia de la \_ clase Win32 TerminalService y el valor de una propiedad TerminalServiceSetting de Win32 determinada \_ .
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Win32_TerminalServiceToSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalServiceToSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422253"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="78eac-105">\_Clase Win32 TerminalServiceToSetting</span><span class="sxs-lookup"><span data-stu-id="78eac-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="78eac-106">La clase WMI **\_ TerminalServiceToSetting de Win32** representa la asociación entre una instancia de la clase [**\_ TerminalService de Win32**](win32-terminalservice.md) y la configuración de una propiedad [**\_ TerminalServiceSetting de Win32**](win32-terminalservicesetting.md) determinada.</span><span class="sxs-lookup"><span data-stu-id="78eac-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="78eac-107">Entre las opciones de configuración se incluyen Escritorio remoto modo de servidor host de sesión de escritorio remoto, licencias, Active Desktop, capacidad de permisos, eliminación de carpetas temporales y carpetas temporales por sesión.</span><span class="sxs-lookup"><span data-stu-id="78eac-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="78eac-108">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas.</span><span class="sxs-lookup"><span data-stu-id="78eac-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="78eac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78eac-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="78eac-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="78eac-110">Members</span></span>

<span data-ttu-id="78eac-111">La **clase \_ TerminalServiceToSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="78eac-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="78eac-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78eac-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78eac-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78eac-113">Properties</span></span>

<span data-ttu-id="78eac-114">La **clase \_ TerminalServiceToSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="78eac-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78eac-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="78eac-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78eac-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78eac-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="78eac-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="78eac-119">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="78eac-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="78eac-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78eac-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78eac-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="78eac-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78eac-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78eac-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="78eac-124">Description of the object.</span></span>

<span data-ttu-id="78eac-125">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78eac-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78eac-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="78eac-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-127">Tipo de datos: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="78eac-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78eac-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78eac-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78eac-130">Representa la instancia de [**Win32 \_ TerminalService**](win32-terminalservice.md) que se puede configurar con la propiedad de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="78eac-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="78eac-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="78eac-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-132">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="78eac-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78eac-134">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="78eac-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="78eac-135">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="78eac-135">The date the object was installed.</span></span> <span data-ttu-id="78eac-136">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="78eac-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="78eac-137">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78eac-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78eac-138">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="78eac-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78eac-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78eac-141">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="78eac-141">The name of the object.</span></span>

<span data-ttu-id="78eac-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78eac-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="78eac-143">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="78eac-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-144">Tipo de datos: **Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="78eac-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78eac-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="78eac-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="78eac-147">Representa la Servicios de Escritorio remoto valores de configuración que se pueden aplicar al servidor host de sesión de escritorio remoto asociado.</span><span class="sxs-lookup"><span data-stu-id="78eac-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="78eac-148">**Estado**</span><span class="sxs-lookup"><span data-stu-id="78eac-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78eac-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78eac-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78eac-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78eac-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78eac-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="78eac-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="78eac-152">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="78eac-152">Current status of the object.</span></span> <span data-ttu-id="78eac-153">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="78eac-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="78eac-154">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="78eac-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="78eac-155">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="78eac-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="78eac-156">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="78eac-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="78eac-157">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="78eac-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="78eac-158">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="78eac-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="78eac-159">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="78eac-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-160">("Error")</span><span class="sxs-lookup"><span data-stu-id="78eac-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-161">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="78eac-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-162">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="78eac-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-163">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="78eac-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-164">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="78eac-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-165">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="78eac-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="78eac-166">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="78eac-166">("Service")</span></span>


<span data-ttu-id="78eac-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="78eac-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="78eac-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78eac-168">Remarks</span></span>

<span data-ttu-id="78eac-169">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="78eac-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="78eac-170">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="78eac-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="78eac-171">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="78eac-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="78eac-172">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="78eac-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="78eac-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78eac-173">Requirements</span></span>



| <span data-ttu-id="78eac-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="78eac-174">Requirement</span></span> | <span data-ttu-id="78eac-175">Value</span><span class="sxs-lookup"><span data-stu-id="78eac-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78eac-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78eac-176">Minimum supported client</span></span><br/> | <span data-ttu-id="78eac-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78eac-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78eac-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78eac-178">Minimum supported server</span></span><br/> | <span data-ttu-id="78eac-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78eac-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78eac-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="78eac-180">Namespace</span></span><br/>                | <span data-ttu-id="78eac-181">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="78eac-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="78eac-182">MOF</span><span class="sxs-lookup"><span data-stu-id="78eac-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78eac-183"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78eac-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78eac-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78eac-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78eac-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78eac-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78eac-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="78eac-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78eac-187">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="78eac-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="78eac-188">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="78eac-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="78eac-189">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="78eac-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="78eac-190">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="78eac-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 


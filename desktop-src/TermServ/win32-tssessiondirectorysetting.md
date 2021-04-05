---
title: Win32_TSSessionDirectorySetting (clase)
description: Representa la asociación entre una instancia de la \_ clase Win32 TerminalService y una instancia de la \_ clase TSSessionDirectory de Win32.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionDirectorySetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSSessionDirectorySetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078960"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="63040-105">\_Clase Win32 TSSessionDirectorySetting</span><span class="sxs-lookup"><span data-stu-id="63040-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="63040-106">Representa la asociación entre una instancia de la clase [**Win32 \_ TerminalService**](win32-terminalservice.md) y una instancia de la clase [**\_ TSSessionDirectory de Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="63040-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="63040-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="63040-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63040-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63040-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="63040-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="63040-109">Members</span></span>

<span data-ttu-id="63040-110">La **clase \_ TSSessionDirectorySetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63040-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="63040-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63040-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63040-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63040-112">Properties</span></span>

<span data-ttu-id="63040-113">La **clase \_ TSSessionDirectorySetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63040-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63040-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63040-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63040-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63040-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63040-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="63040-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="63040-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="63040-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="63040-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63040-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63040-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="63040-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63040-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63040-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63040-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="63040-123">Description of the object.</span></span>

<span data-ttu-id="63040-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63040-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63040-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="63040-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-126">Tipo de datos: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="63040-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="63040-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63040-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63040-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63040-129">Representa la instancia de **Win32 \_ TerminalService** que se puede configurar con la propiedad de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="63040-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="63040-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63040-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63040-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63040-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63040-133">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="63040-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="63040-134">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="63040-134">The date the object was installed.</span></span> <span data-ttu-id="63040-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="63040-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="63040-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63040-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63040-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="63040-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63040-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63040-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63040-140">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="63040-140">The name of the object.</span></span>

<span data-ttu-id="63040-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63040-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63040-142">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="63040-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-143">Tipo de datos: **Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="63040-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="63040-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63040-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63040-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63040-146">Representa la configuración del agente de conexión a escritorio remoto que se puede aplicar al servidor host de sesión de escritorio remoto asociado.</span><span class="sxs-lookup"><span data-stu-id="63040-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="63040-147">**Estado**</span><span class="sxs-lookup"><span data-stu-id="63040-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63040-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63040-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63040-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63040-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63040-150">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="63040-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="63040-151">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="63040-151">Current status of the object.</span></span> <span data-ttu-id="63040-152">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="63040-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="63040-153">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="63040-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="63040-154">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="63040-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="63040-155">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="63040-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="63040-156">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="63040-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="63040-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63040-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="63040-158">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="63040-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-159">("Error")</span><span class="sxs-lookup"><span data-stu-id="63040-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="63040-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-161">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="63040-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-162">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="63040-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="63040-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-164">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="63040-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="63040-165">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="63040-165">("Service")</span></span>


<span data-ttu-id="63040-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63040-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="63040-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63040-167">Remarks</span></span>

<span data-ttu-id="63040-168">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="63040-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="63040-169">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="63040-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="63040-170">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="63040-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="63040-171">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="63040-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="63040-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63040-172">Requirements</span></span>



| <span data-ttu-id="63040-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="63040-173">Requirement</span></span> | <span data-ttu-id="63040-174">Value</span><span class="sxs-lookup"><span data-stu-id="63040-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63040-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63040-175">Minimum supported client</span></span><br/> | <span data-ttu-id="63040-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63040-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63040-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63040-177">Minimum supported server</span></span><br/> | <span data-ttu-id="63040-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63040-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63040-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63040-179">Namespace</span></span><br/>                | <span data-ttu-id="63040-180">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="63040-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="63040-181">MOF</span><span class="sxs-lookup"><span data-stu-id="63040-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63040-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63040-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="63040-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63040-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63040-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63040-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63040-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="63040-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63040-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="63040-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="63040-187">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="63040-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="63040-188">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="63040-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 


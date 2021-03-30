---
title: Win32_TerminalTerminalSetting (clase)
description: Representa la asociación entre un terminal y sus valores de configuración.
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Win32_TerminalTerminalSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalTerminalSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490289"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="55624-105">\_Clase Win32 TerminalTerminalSetting</span><span class="sxs-lookup"><span data-stu-id="55624-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="55624-106">La clase WMI **\_ TerminalTerminalSetting de Win32** representa la asociación entre un terminal y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="55624-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="55624-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas.</span><span class="sxs-lookup"><span data-stu-id="55624-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55624-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55624-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="55624-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="55624-109">Members</span></span>

<span data-ttu-id="55624-110">La **clase \_ TerminalTerminalSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="55624-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="55624-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55624-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55624-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55624-112">Properties</span></span>

<span data-ttu-id="55624-113">La **clase \_ TerminalTerminalSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="55624-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55624-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="55624-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55624-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55624-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55624-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="55624-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="55624-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="55624-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="55624-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55624-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55624-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55624-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55624-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55624-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55624-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="55624-123">Description of the object.</span></span>

<span data-ttu-id="55624-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55624-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55624-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="55624-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-126">Tipo de datos **: \_ terminal de Win32**</span><span class="sxs-lookup"><span data-stu-id="55624-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="55624-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55624-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55624-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55624-129">Representa el terminal que se puede configurar mediante la propiedad de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="55624-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="55624-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55624-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55624-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55624-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55624-133">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="55624-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="55624-134">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="55624-134">The date the object was installed.</span></span> <span data-ttu-id="55624-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="55624-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="55624-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55624-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55624-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="55624-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55624-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55624-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55624-140">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="55624-140">The name of the object.</span></span>

<span data-ttu-id="55624-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55624-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55624-142">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="55624-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-143">Tipo de datos: **Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="55624-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="55624-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55624-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55624-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55624-146">Representa la configuración que se puede aplicar al terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="55624-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="55624-147">**Estado**</span><span class="sxs-lookup"><span data-stu-id="55624-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55624-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55624-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55624-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55624-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55624-150">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="55624-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="55624-151">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="55624-151">Current status of the object.</span></span> <span data-ttu-id="55624-152">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="55624-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="55624-153">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="55624-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="55624-154">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="55624-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="55624-155">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="55624-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="55624-156">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="55624-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="55624-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55624-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="55624-158">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="55624-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-159">("Error")</span><span class="sxs-lookup"><span data-stu-id="55624-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="55624-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-161">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="55624-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-162">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="55624-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="55624-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-164">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="55624-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="55624-165">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="55624-165">("Service")</span></span>


<span data-ttu-id="55624-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="55624-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="55624-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55624-167">Remarks</span></span>

<span data-ttu-id="55624-168">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="55624-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55624-169">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="55624-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="55624-170">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="55624-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55624-171">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="55624-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="55624-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55624-172">Requirements</span></span>



| <span data-ttu-id="55624-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="55624-173">Requirement</span></span> | <span data-ttu-id="55624-174">Value</span><span class="sxs-lookup"><span data-stu-id="55624-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55624-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55624-175">Minimum supported client</span></span><br/> | <span data-ttu-id="55624-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55624-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55624-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55624-177">Minimum supported server</span></span><br/> | <span data-ttu-id="55624-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55624-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55624-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55624-179">Namespace</span></span><br/>                | <span data-ttu-id="55624-180">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="55624-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="55624-181">MOF</span><span class="sxs-lookup"><span data-stu-id="55624-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55624-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55624-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="55624-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55624-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55624-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55624-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55624-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="55624-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55624-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="55624-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="55624-187">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="55624-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="55624-188">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="55624-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


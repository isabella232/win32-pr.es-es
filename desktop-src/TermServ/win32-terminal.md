---
title: Win32_Terminal (clase)
description: Representa un terminal.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_Terminal de clase, se describe
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150027"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="da5c1-105">\_Clase de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="da5c1-105">Win32\_Terminal class</span></span>

<span data-ttu-id="da5c1-106">La clase WMI de **\_ terminal de Win32** representa un terminal.</span><span class="sxs-lookup"><span data-stu-id="da5c1-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="da5c1-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="da5c1-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="da5c1-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="da5c1-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5c1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da5c1-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="da5c1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="da5c1-110">Members</span></span>

<span data-ttu-id="da5c1-111">La clase de **\_ terminal Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="da5c1-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="da5c1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="da5c1-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="da5c1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da5c1-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da5c1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="da5c1-114">Methods</span></span>

<span data-ttu-id="da5c1-115">La clase de **\_ terminal Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="da5c1-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="da5c1-116">Método</span><span class="sxs-lookup"><span data-stu-id="da5c1-116">Method</span></span>                                  | <span data-ttu-id="da5c1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="da5c1-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da5c1-118">**A**</span><span class="sxs-lookup"><span data-stu-id="da5c1-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="da5c1-119">Crea un terminal con valores predeterminados que se pueden personalizar mediante las propiedades y los métodos de las clases [**\_ TerminalSetting de Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="da5c1-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="da5c1-120">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="da5c1-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="da5c1-121">Elimina el terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="da5c1-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="da5c1-122">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="da5c1-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="da5c1-123">Deshabilita o habilita el terminal.</span><span class="sxs-lookup"><span data-stu-id="da5c1-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="da5c1-124">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="da5c1-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="da5c1-125">Cambia el nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="da5c1-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="da5c1-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="da5c1-126">Properties</span></span>

<span data-ttu-id="da5c1-127">La clase de **\_ terminal Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="da5c1-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da5c1-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="da5c1-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da5c1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-131">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="da5c1-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-132">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="da5c1-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="da5c1-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da5c1-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da5c1-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da5c1-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-137">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="da5c1-137">Description of the object.</span></span>

<span data-ttu-id="da5c1-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da5c1-139">**fEnableTerminal**</span><span class="sxs-lookup"><span data-stu-id="da5c1-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5c1-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-142">Especifica si el terminal especificado está deshabilitado o habilitado.</span><span class="sxs-lookup"><span data-stu-id="da5c1-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="da5c1-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="da5c1-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="da5c1-144">El terminal está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="da5c1-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="da5c1-145"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="da5c1-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="da5c1-146">El terminal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="da5c1-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="da5c1-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da5c1-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-148">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da5c1-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-150">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="da5c1-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-151">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="da5c1-151">The date the object was installed.</span></span> <span data-ttu-id="da5c1-152">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="da5c1-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="da5c1-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da5c1-154">**LoggedOnUsers**</span><span class="sxs-lookup"><span data-stu-id="da5c1-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-155">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5c1-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-157">Número de sesiones iniciadas en el terminal.</span><span class="sxs-lookup"><span data-stu-id="da5c1-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="da5c1-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="da5c1-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da5c1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-161">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="da5c1-161">The name of the object.</span></span>

<span data-ttu-id="da5c1-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="da5c1-163">**Estado**</span><span class="sxs-lookup"><span data-stu-id="da5c1-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da5c1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-166">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="da5c1-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-167">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="da5c1-167">Current status of the object.</span></span> <span data-ttu-id="da5c1-168">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="da5c1-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="da5c1-169">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="da5c1-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="da5c1-170">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="da5c1-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="da5c1-171">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="da5c1-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="da5c1-172">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="da5c1-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="da5c1-173">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="da5c1-174">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="da5c1-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-175">("Error")</span><span class="sxs-lookup"><span data-stu-id="da5c1-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-176">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="da5c1-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-177">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="da5c1-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-178">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="da5c1-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-179">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="da5c1-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-180">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="da5c1-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="da5c1-181">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="da5c1-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="da5c1-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="da5c1-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5c1-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="da5c1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="da5c1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5c1-185">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="da5c1-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="da5c1-186">Nombre único que identifica la instancia del terminal.</span><span class="sxs-lookup"><span data-stu-id="da5c1-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da5c1-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da5c1-187">Remarks</span></span>

<span data-ttu-id="da5c1-188">**Win32 \_ Terminal** está asociado a [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) como la propiedad de **elemento** de la Asociación [**\_ TerminalTerminalSetting de Win32**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="da5c1-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="da5c1-189">Las clases siguientes son subclases de la clase de **\_ terminal Win32** : [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), [**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)y [**Win32 \_ TSAccount**](win32-tsaccount.md).</span><span class="sxs-lookup"><span data-stu-id="da5c1-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="da5c1-190">Tenga en cuenta que Winstations asociado a la sesión de consola no puede tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="da5c1-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="da5c1-191">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad **TerminalName** , los métodos de este objeto devuelven **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="da5c1-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="da5c1-192">Este código de error también se devuelve si una estación de ventana intenta llamar a métodos de este objeto para agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="da5c1-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="da5c1-193">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="da5c1-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="da5c1-194">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="da5c1-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="da5c1-195">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="da5c1-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="da5c1-196">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="da5c1-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="da5c1-197">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="da5c1-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="da5c1-198">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="da5c1-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="da5c1-199">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="da5c1-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="da5c1-200">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="da5c1-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="da5c1-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da5c1-201">Requirements</span></span>



| <span data-ttu-id="da5c1-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5c1-202">Requirement</span></span> | <span data-ttu-id="da5c1-203">Value</span><span class="sxs-lookup"><span data-stu-id="da5c1-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da5c1-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5c1-204">Minimum supported client</span></span><br/> | <span data-ttu-id="da5c1-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da5c1-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da5c1-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da5c1-206">Minimum supported server</span></span><br/> | <span data-ttu-id="da5c1-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da5c1-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da5c1-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da5c1-208">Namespace</span></span><br/>                | <span data-ttu-id="da5c1-209">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="da5c1-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="da5c1-210">MOF</span><span class="sxs-lookup"><span data-stu-id="da5c1-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da5c1-211"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da5c1-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="da5c1-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da5c1-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da5c1-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da5c1-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da5c1-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="da5c1-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5c1-215">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="da5c1-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="da5c1-216">**Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="da5c1-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="da5c1-217">**Win32 \_ TerminalTerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="da5c1-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 


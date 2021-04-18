---
title: Win32_TSPermissionsSetting (clase)
description: Incluye un método para agregar cuentas nuevas al terminal y un método para restaurar los permisos predeterminados en un terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Win32_TSPermissionsSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSPermissionsSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676913"
---
# <a name="win32_tspermissionssetting-class"></a><span data-ttu-id="0f43b-105">\_Clase Win32 TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="0f43b-105">Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="0f43b-106">La clase WMI **\_ TSPermissionsSetting de Win32** incluye un método para agregar cuentas nuevas al terminal y un método para restaurar los permisos predeterminados en un terminal.</span><span class="sxs-lookup"><span data-stu-id="0f43b-106">The **Win32\_TSPermissionsSetting** WMI class includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

<span data-ttu-id="0f43b-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="0f43b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="0f43b-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="0f43b-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f43b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f43b-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a><span data-ttu-id="0f43b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f43b-110">Members</span></span>

<span data-ttu-id="0f43b-111">La **clase \_ TSPermissionsSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0f43b-111">The **Win32\_TSPermissionsSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0f43b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f43b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f43b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f43b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f43b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f43b-114">Methods</span></span>

<span data-ttu-id="0f43b-115">La clase **Win32 \_ TSPermissionsSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0f43b-115">The **Win32\_TSPermissionsSetting** class has these methods.</span></span>



| <span data-ttu-id="0f43b-116">Método</span><span class="sxs-lookup"><span data-stu-id="0f43b-116">Method</span></span>                                                                | <span data-ttu-id="0f43b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f43b-117">Description</span></span>                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f43b-118">**AddAccount**</span><span class="sxs-lookup"><span data-stu-id="0f43b-118">**AddAccount**</span></span>](win32-tspermissionssetting-addaccount.md)           | <span data-ttu-id="0f43b-119">Agrega una cuenta al terminal con el conjunto de permisos especificado en el valor del parámetro *PermissionPreSet* .</span><span class="sxs-lookup"><span data-stu-id="0f43b-119">Adds an account to the terminal with the permission set specified in the value of the *PermissionPreSet* parameter.</span></span><br/> |
| [<span data-ttu-id="0f43b-120">**RestoreDefaults**</span><span class="sxs-lookup"><span data-stu-id="0f43b-120">**RestoreDefaults**</span></span>](win32-tspermissionssetting-restoredefaults.md) | <span data-ttu-id="0f43b-121">Restaura los valores del conjunto de permisos predeterminados para el terminal.</span><span class="sxs-lookup"><span data-stu-id="0f43b-121">Restores the default permission set values for the terminal.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="0f43b-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0f43b-122">Properties</span></span>

<span data-ttu-id="0f43b-123">La **clase \_ TSPermissionsSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0f43b-123">The **Win32\_TSPermissionsSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f43b-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0f43b-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-127">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0f43b-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-128">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="0f43b-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0f43b-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-130">**DenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="0f43b-130">**DenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f43b-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-133">Especifica si el administrador local tiene permiso para personalizar.</span><span class="sxs-lookup"><span data-stu-id="0f43b-133">Specifies whether local administrator has permission to customize.</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-134">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0f43b-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-137">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0f43b-137">Description of the object.</span></span>

<span data-ttu-id="0f43b-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0f43b-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f43b-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-142">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0f43b-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-143">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="0f43b-143">The date the object was installed.</span></span> <span data-ttu-id="0f43b-144">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="0f43b-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0f43b-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-146">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0f43b-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-149">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="0f43b-149">The name of the object.</span></span>

<span data-ttu-id="0f43b-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-151">**PolicySourceDenyAdminPermissionForCustomization**</span><span class="sxs-lookup"><span data-stu-id="0f43b-151">**PolicySourceDenyAdminPermissionForCustomization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f43b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-154">Indica si la propiedad **MinEncryptionLevel** está configurada por el servidor, la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0f43b-154">Indicates whether the **MinEncryptionLevel** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="0f43b-155">0</span><span class="sxs-lookup"><span data-stu-id="0f43b-155">0</span></span>
</dt> <dd>

<span data-ttu-id="0f43b-156">Servidor</span><span class="sxs-lookup"><span data-stu-id="0f43b-156">Server</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-157">1</span><span class="sxs-lookup"><span data-stu-id="0f43b-157">1</span></span>
</dt> <dd>

<span data-ttu-id="0f43b-158">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="0f43b-158">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f43b-159">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0f43b-159">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0f43b-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-163">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="0f43b-163">Current status of the object.</span></span> <span data-ttu-id="0f43b-164">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="0f43b-164">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0f43b-165">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="0f43b-165">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0f43b-166">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="0f43b-166">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0f43b-167">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="0f43b-167">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0f43b-168">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="0f43b-168">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0f43b-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0f43b-170">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="0f43b-170">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-171">("Error")</span><span class="sxs-lookup"><span data-stu-id="0f43b-171">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-172">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="0f43b-172">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-173">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="0f43b-173">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-174">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="0f43b-174">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-175">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0f43b-175">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-176">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="0f43b-176">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0f43b-177">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="0f43b-177">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f43b-178">**StringSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0f43b-178">**StringSecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0f43b-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-181">Descriptor de seguridad asociado con el terminal en formato de matriz de bytes binario.</span><span class="sxs-lookup"><span data-stu-id="0f43b-181">Security descriptor associated with the terminal in binary byte array format.</span></span>

</dd> <dt>

<span data-ttu-id="0f43b-182">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="0f43b-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f43b-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0f43b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f43b-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0f43b-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f43b-185">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="0f43b-185">The name of the terminal.</span></span>

<span data-ttu-id="0f43b-186">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="0f43b-186">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f43b-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f43b-187">Remarks</span></span>

<span data-ttu-id="0f43b-188">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="0f43b-188">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0f43b-189">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="0f43b-189">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0f43b-190">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="0f43b-190">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="0f43b-191">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="0f43b-191">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0f43b-192">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0f43b-192">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f43b-193">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0f43b-193">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f43b-194">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="0f43b-194">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f43b-195">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0f43b-195">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f43b-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f43b-196">Requirements</span></span>



| <span data-ttu-id="0f43b-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f43b-197">Requirement</span></span> | <span data-ttu-id="0f43b-198">Value</span><span class="sxs-lookup"><span data-stu-id="0f43b-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f43b-199">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f43b-199">Minimum supported client</span></span><br/> | <span data-ttu-id="0f43b-200">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f43b-200">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f43b-201">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f43b-201">Minimum supported server</span></span><br/> | <span data-ttu-id="0f43b-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f43b-202">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f43b-203">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0f43b-203">Namespace</span></span><br/>                | <span data-ttu-id="0f43b-204">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0f43b-204">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0f43b-205">MOF</span><span class="sxs-lookup"><span data-stu-id="0f43b-205">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f43b-206"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f43b-206"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f43b-207">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f43b-207">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f43b-208"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f43b-208"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f43b-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f43b-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f43b-210">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="0f43b-210">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


---
title: Win32_TSStartMenuApplication (clase)
description: Describe las aplicaciones que se encuentran en el menú Inicio de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 88b412b8-139f-4266-b7d8-c34f93940a72
ms.tgt_platform: multiple
keywords:
- Win32_TSStartMenuApplication clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSStartMenuApplication de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSStartMenuApplication
- Win32_TSStartMenuApplication.Caption
- Win32_TSStartMenuApplication.Description
- Win32_TSStartMenuApplication.InstallDate
- Win32_TSStartMenuApplication.Name
- Win32_TSStartMenuApplication.Status
- Win32_TSStartMenuApplication.Path
- Win32_TSStartMenuApplication.VPath
- Win32_TSStartMenuApplication.IconPath
- Win32_TSStartMenuApplication.IconIndex
- Win32_TSStartMenuApplication.CommandLineArguments
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dae7610381745f6ced2a01e76f8545b33d1205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803847"
---
# <a name="win32_tsstartmenuapplication-class"></a><span data-ttu-id="d44bb-105">\_Clase Win32 TSStartMenuApplication</span><span class="sxs-lookup"><span data-stu-id="d44bb-105">Win32\_TSStartMenuApplication class</span></span>

<span data-ttu-id="d44bb-106">Describe las aplicaciones que se encuentran en el menú Inicio de un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="d44bb-106">Describes the applications that are on the Start menu of a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="d44bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d44bb-107">Syntax</span></span>

``` syntax
class Win32_TSStartMenuApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Path;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  string   CommandLineArguments;
};
```

## <a name="members"></a><span data-ttu-id="d44bb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d44bb-108">Members</span></span>

<span data-ttu-id="d44bb-109">La **clase \_ TSStartMenuApplication de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d44bb-109">The **Win32\_TSStartMenuApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="d44bb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d44bb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d44bb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d44bb-111">Properties</span></span>

<span data-ttu-id="d44bb-112">La **clase \_ TSStartMenuApplication de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d44bb-112">The **Win32\_TSStartMenuApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d44bb-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d44bb-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d44bb-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-117">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="d44bb-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d44bb-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-119">**CommandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="d44bb-119">**CommandLineArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-122">Argumentos de la línea de comandos que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="d44bb-122">The command-line arguments to use.</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d44bb-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-126">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d44bb-126">Description of the object.</span></span>

<span data-ttu-id="d44bb-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-128">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="d44bb-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d44bb-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-131">Índice o identificador del icono.</span><span class="sxs-lookup"><span data-stu-id="d44bb-131">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="d44bb-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-135">Ruta de acceso del icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d44bb-135">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d44bb-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-137">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d44bb-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-139">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d44bb-139">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-140">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d44bb-140">The date the object was installed.</span></span> <span data-ttu-id="d44bb-141">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="d44bb-141">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d44bb-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d44bb-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-146">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="d44bb-146">The name of the object.</span></span>

<span data-ttu-id="d44bb-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-148">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="d44bb-148">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-151">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d44bb-151">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-152">Ruta de acceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d44bb-152">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="d44bb-153">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d44bb-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-156">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="d44bb-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-157">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d44bb-157">Current status of the object.</span></span> <span data-ttu-id="d44bb-158">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d44bb-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d44bb-159">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d44bb-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d44bb-160">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d44bb-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d44bb-161">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d44bb-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d44bb-162">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d44bb-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d44bb-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d44bb-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d44bb-164">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="d44bb-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-165">("Error")</span><span class="sxs-lookup"><span data-stu-id="d44bb-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-166">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="d44bb-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-167">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="d44bb-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-168">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d44bb-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-169">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d44bb-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-170">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="d44bb-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d44bb-171">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="d44bb-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d44bb-172">**VPath**</span><span class="sxs-lookup"><span data-stu-id="d44bb-172">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d44bb-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d44bb-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d44bb-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d44bb-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d44bb-175">Ruta de acceso virtual de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d44bb-175">The virtual path of the application.</span></span> <span data-ttu-id="d44bb-176">Esto incluye las variables de entorno del sistema, como% WINDIR%.</span><span class="sxs-lookup"><span data-stu-id="d44bb-176">This includes system environment variables, such as %windir%.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d44bb-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d44bb-177">Remarks</span></span>

<span data-ttu-id="d44bb-178">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d44bb-178">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="d44bb-179">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d44bb-179">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d44bb-180">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="d44bb-180">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="d44bb-181">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="d44bb-181">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d44bb-182">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d44bb-182">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d44bb-183">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d44bb-183">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d44bb-184">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d44bb-184">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d44bb-185">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d44bb-185">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d44bb-186">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d44bb-186">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d44bb-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d44bb-187">Requirements</span></span>



| <span data-ttu-id="d44bb-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="d44bb-188">Requirement</span></span> | <span data-ttu-id="d44bb-189">Value</span><span class="sxs-lookup"><span data-stu-id="d44bb-189">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d44bb-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d44bb-190">Minimum supported client</span></span><br/> | <span data-ttu-id="d44bb-191">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d44bb-191">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d44bb-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d44bb-192">Minimum supported server</span></span><br/> | <span data-ttu-id="d44bb-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d44bb-193">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d44bb-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d44bb-194">Namespace</span></span><br/>                | <span data-ttu-id="d44bb-195">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d44bb-195">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d44bb-196">MOF</span><span class="sxs-lookup"><span data-stu-id="d44bb-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d44bb-197"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d44bb-197"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="d44bb-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d44bb-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d44bb-199"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d44bb-199"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


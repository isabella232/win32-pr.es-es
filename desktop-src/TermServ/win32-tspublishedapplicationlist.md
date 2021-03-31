---
title: Win32_TSPublishedApplicationList (clase)
description: Representa la lista de programas que se encuentran en la lista Programas RemoteApp en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 3dbefe54-8c31-439f-a87a-5148214a07d5
ms.tgt_platform: multiple
keywords:
- Win32_TSPublishedApplicationList clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSPublishedApplicationList de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplicationList
- Win32_TSPublishedApplicationList.Caption
- Win32_TSPublishedApplicationList.Description
- Win32_TSPublishedApplicationList.InstallDate
- Win32_TSPublishedApplicationList.Name
- Win32_TSPublishedApplicationList.Status
- Win32_TSPublishedApplicationList.Disabled
- Win32_TSPublishedApplicationList.PolicySourceDisabled
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f87a87dc6f95bcdb33c7dbd1364ad6b3114ddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079239"
---
# <a name="win32_tspublishedapplicationlist-class"></a><span data-ttu-id="3b4cd-105">\_Clase Win32 TSPublishedApplicationList</span><span class="sxs-lookup"><span data-stu-id="3b4cd-105">Win32\_TSPublishedApplicationList class</span></span>

<span data-ttu-id="3b4cd-106">Representa la lista de programas que se encuentran en la lista Programas RemoteApp en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-106">Represents the list of programs that are in the RemoteApp Programs list on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4cd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b4cd-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplicationList : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  Disabled;
  uint32   PolicySourceDisabled;
};
```

## <a name="members"></a><span data-ttu-id="3b4cd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b4cd-108">Members</span></span>

<span data-ttu-id="3b4cd-109">La **clase \_ TSPublishedApplicationList de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b4cd-109">The **Win32\_TSPublishedApplicationList** class has these types of members:</span></span>

-   [<span data-ttu-id="3b4cd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b4cd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b4cd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b4cd-111">Properties</span></span>

<span data-ttu-id="3b4cd-112">La **clase \_ TSPublishedApplicationList de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-112">The **Win32\_TSPublishedApplicationList** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b4cd-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-116">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3b4cd-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-117">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-117">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="3b4cd-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-122">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-122">Description of the object.</span></span>

<span data-ttu-id="3b4cd-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-124">**Deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-124">**Disabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-127">Indica si el servidor host de sesión de escritorio remoto restringe los programas que un usuario puede iniciar en la conexión inicial a los programas que se encuentran en la lista Programas RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-127">Indicates whether the RD Session Host server restricts the programs that a user can start on initial connection to the programs that are in the RemoteApp Programs list.</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-129">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-131">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-131">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-132">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-132">The date the object was installed.</span></span> <span data-ttu-id="3b4cd-133">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-133">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3b4cd-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-135">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-138">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-138">The name of the object.</span></span>

<span data-ttu-id="3b4cd-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-140">**PolicySourceDisabled**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-140">**PolicySourceDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-143">Indica dónde está configurada la propiedad **Disabled** .</span><span class="sxs-lookup"><span data-stu-id="3b4cd-143">Indicates where the **Disabled** property is configured.</span></span> <span data-ttu-id="3b4cd-144">Entre los posibles valores se incluyen:</span><span class="sxs-lookup"><span data-stu-id="3b4cd-144">Possible values include:</span></span>

<dt>

<span data-ttu-id="3b4cd-145">0</span><span class="sxs-lookup"><span data-stu-id="3b4cd-145">0</span></span>
</dt> <dd>

<span data-ttu-id="3b4cd-146">La configuración se configura en el servidor a través de Administrador de RemoteApp o del proveedor de WMI de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-146">The setting is configured on the server through RemoteApp Manager or the RemoteApp WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-147">1</span><span class="sxs-lookup"><span data-stu-id="3b4cd-147">1</span></span>
</dt> <dd>

<span data-ttu-id="3b4cd-148">La configuración se configura mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-148">The setting is configured through group policy.</span></span>

</dd> <dt>

<span data-ttu-id="3b4cd-149">2</span><span class="sxs-lookup"><span data-stu-id="3b4cd-149">2</span></span>
</dt> <dd>

<span data-ttu-id="3b4cd-150">La configuración no está configurada.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-150">The setting is not configured.</span></span> <span data-ttu-id="3b4cd-151">El valor predeterminado de **false** se utiliza para la propiedad **Disabled** .</span><span class="sxs-lookup"><span data-stu-id="3b4cd-151">The default value of **FALSE** is used for the **Disabled** property.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3b4cd-152">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4cd-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b4cd-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b4cd-155">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="3b4cd-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="3b4cd-156">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-156">Current status of the object.</span></span> <span data-ttu-id="3b4cd-157">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-157">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3b4cd-158">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-158">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3b4cd-159">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="3b4cd-159">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3b4cd-160">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-160">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3b4cd-161">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-161">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3b4cd-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="3b4cd-163">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-163">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-164">("Error")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-164">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-165">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-165">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-166">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-166">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-167">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-167">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-168">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-168">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-169">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-169">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3b4cd-170">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="3b4cd-170">("Service")</span></span>


<span data-ttu-id="3b4cd-171"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="3b4cd-171"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="3b4cd-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b4cd-172">Remarks</span></span>

<span data-ttu-id="3b4cd-173">Debe ser miembro del grupo administradores para establecer las propiedades utilizando esta clase.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-173">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="3b4cd-174">La propiedad **Disabled** no impide que los usuarios inicien de forma remota programas que no están en la lista después de conectarse al servidor host de sesión de escritorio remoto mediante un programa de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-174">The **Disabled** property does not prevent users from starting unlisted programs remotely after they connect to the RD Session Host server by using a RemoteApp program.</span></span>

<span data-ttu-id="3b4cd-175">La propiedad **Disabled** se establecerá en un valor de 2 solo si falta la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="3b4cd-175">The **Disabled** property will be set to a value of 2 only if the following registry entry is missing:</span></span>

<span data-ttu-id="3b4cd-176">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WindowsNT** \\ **CurrentVersion** \\ **TerminalServer** \\ **TSAppAllowList** \\ **fDisabledAllowList**</span><span class="sxs-lookup"><span data-stu-id="3b4cd-176">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WindowsNT**\\**CurrentVersion**\\**TerminalServer**\\**TSAppAllowList**\\**fDisabledAllowList**</span></span>

<span data-ttu-id="3b4cd-177">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-177">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="3b4cd-178">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="3b4cd-178">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="3b4cd-179">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-179">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="3b4cd-180">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-180">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="3b4cd-181">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3b4cd-182">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-182">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3b4cd-183">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="3b4cd-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3b4cd-184">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3b4cd-184">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b4cd-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b4cd-185">Requirements</span></span>



| <span data-ttu-id="3b4cd-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b4cd-186">Requirement</span></span> | <span data-ttu-id="3b4cd-187">Value</span><span class="sxs-lookup"><span data-stu-id="3b4cd-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4cd-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b4cd-188">Minimum supported client</span></span><br/> | <span data-ttu-id="3b4cd-189">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b4cd-189">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3b4cd-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b4cd-190">Minimum supported server</span></span><br/> | <span data-ttu-id="3b4cd-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b4cd-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b4cd-192">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b4cd-192">Namespace</span></span><br/>                | <span data-ttu-id="3b4cd-193">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3b4cd-193">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3b4cd-194">MOF</span><span class="sxs-lookup"><span data-stu-id="3b4cd-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b4cd-195"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b4cd-195"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="3b4cd-196">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b4cd-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b4cd-197"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b4cd-197"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


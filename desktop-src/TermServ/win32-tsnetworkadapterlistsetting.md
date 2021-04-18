---
title: Win32_TSNetworkAdapterListSetting (clase)
description: Enumera la lista de adaptadores de red que se pueden configurar para un terminal Win32 \_ , según el protocolo de terminal y el método de transporte especificados.
ms.assetid: affe440a-1a7b-49be-a4aa-d792811c59ea
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterListSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSNetworkAdapterListSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterListSetting
- Win32_TSNetworkAdapterListSetting.Caption
- Win32_TSNetworkAdapterListSetting.Description
- Win32_TSNetworkAdapterListSetting.InstallDate
- Win32_TSNetworkAdapterListSetting.Name
- Win32_TSNetworkAdapterListSetting.Status
- Win32_TSNetworkAdapterListSetting.TerminalName
- Win32_TSNetworkAdapterListSetting.NetworkAdapterID
- Win32_TSNetworkAdapterListSetting.NetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e8c1ac9466d389924d0717748d7da9ec1f5b55f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686050"
---
# <a name="win32_tsnetworkadapterlistsetting-class"></a><span data-ttu-id="10ae0-105">\_Clase Win32 TSNetworkAdapterListSetting</span><span class="sxs-lookup"><span data-stu-id="10ae0-105">Win32\_TSNetworkAdapterListSetting class</span></span>

<span data-ttu-id="10ae0-106">La clase WMI **\_ TSNetworkAdapterListSetting de Win32** enumera la lista de adaptadores de red que se pueden configurar para un [**\_ terminal Win32**](win32-terminal.md), según el protocolo de terminal y el método de transporte especificados.</span><span class="sxs-lookup"><span data-stu-id="10ae0-106">The **Win32\_TSNetworkAdapterListSetting** WMI class enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

<span data-ttu-id="10ae0-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="10ae0-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ae0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10ae0-108">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TSNETWORKADAPTERLISTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterListSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   NetworkAdapterID;
  string   NetworkAdapterIP;
};
```

## <a name="members"></a><span data-ttu-id="10ae0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="10ae0-109">Members</span></span>

<span data-ttu-id="10ae0-110">La **clase \_ TSNetworkAdapterListSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="10ae0-110">The **Win32\_TSNetworkAdapterListSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="10ae0-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10ae0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10ae0-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10ae0-112">Properties</span></span>

<span data-ttu-id="10ae0-113">La **clase \_ TSNetworkAdapterListSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="10ae0-113">The **Win32\_TSNetworkAdapterListSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10ae0-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="10ae0-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="10ae0-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="10ae0-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="10ae0-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10ae0-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="10ae0-123">Description of the object.</span></span>

<span data-ttu-id="10ae0-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10ae0-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10ae0-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="10ae0-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="10ae0-129">The date the object was installed.</span></span> <span data-ttu-id="10ae0-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="10ae0-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="10ae0-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="10ae0-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="10ae0-135">The name of the object.</span></span>

<span data-ttu-id="10ae0-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-137">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="10ae0-137">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-140">GUID del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="10ae0-140">The GUID of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-141">**NetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="10ae0-141">**NetworkAdapterIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-144">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10ae0-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-145">Dirección IP del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="10ae0-145">The IP address of the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10ae0-146">**Estado**</span><span class="sxs-lookup"><span data-stu-id="10ae0-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-149">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="10ae0-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-150">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="10ae0-150">Current status of the object.</span></span> <span data-ttu-id="10ae0-151">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="10ae0-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10ae0-152">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="10ae0-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="10ae0-153">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="10ae0-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="10ae0-154">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="10ae0-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10ae0-155">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="10ae0-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="10ae0-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="10ae0-157">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="10ae0-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-158">("Error")</span><span class="sxs-lookup"><span data-stu-id="10ae0-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="10ae0-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-160">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="10ae0-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-161">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="10ae0-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="10ae0-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-163">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="10ae0-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="10ae0-164">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="10ae0-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ae0-165">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="10ae0-165">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ae0-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="10ae0-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10ae0-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10ae0-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ae0-168">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="10ae0-168">The name of the terminal.</span></span>

<span data-ttu-id="10ae0-169">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="10ae0-169">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10ae0-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10ae0-170">Remarks</span></span>

<span data-ttu-id="10ae0-171">Para conectarse al espacio de nombres "root \\ cimv2 \\ TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="10ae0-171">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="10ae0-172">En el caso de las llamadas de C/C++, esto sería un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="10ae0-172">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="10ae0-173">En el caso de las llamadas de Visual Basic y scripting, esto sería un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="10ae0-173">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="10ae0-174">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="10ae0-174">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="10ae0-175">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10ae0-175">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10ae0-176">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="10ae0-176">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10ae0-177">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="10ae0-177">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10ae0-178">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10ae0-178">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10ae0-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10ae0-179">Requirements</span></span>



| <span data-ttu-id="10ae0-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ae0-180">Requirement</span></span> | <span data-ttu-id="10ae0-181">Value</span><span class="sxs-lookup"><span data-stu-id="10ae0-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10ae0-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10ae0-182">Minimum supported client</span></span><br/> | <span data-ttu-id="10ae0-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10ae0-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10ae0-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10ae0-184">Minimum supported server</span></span><br/> | <span data-ttu-id="10ae0-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10ae0-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10ae0-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10ae0-186">Namespace</span></span><br/>                | <span data-ttu-id="10ae0-187">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="10ae0-187">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="10ae0-188">MOF</span><span class="sxs-lookup"><span data-stu-id="10ae0-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ae0-189"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10ae0-189"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ae0-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10ae0-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ae0-191"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10ae0-191"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ae0-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="10ae0-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ae0-193">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="10ae0-193">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="10ae0-194">**Win32 \_ TSNetworkAdapterSetting**</span><span class="sxs-lookup"><span data-stu-id="10ae0-194">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 


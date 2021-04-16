---
title: Win32_TSApplicationFileExtensions (clase)
description: Las extensiones de nombre de archivo que se administran mediante una aplicación en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: beefc266-5ad6-49ee-b761-98764e2905d6
ms.tgt_platform: multiple
keywords:
- Win32_TSApplicationFileExtensions clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSApplicationFileExtensions de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions.Caption
- Win32_TSApplicationFileExtensions.Description
- Win32_TSApplicationFileExtensions.InstallDate
- Win32_TSApplicationFileExtensions.Name
- Win32_TSApplicationFileExtensions.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28f84ff122b77abf1474b5686edab627177424b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686154"
---
# <a name="win32_tsapplicationfileextensions-class"></a><span data-ttu-id="95f03-105">\_Clase Win32 TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="95f03-105">Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="95f03-106">Describe las extensiones de nombre de archivo que se administran mediante una aplicación en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="95f03-106">Describes the file name extensions that are handled by an application on a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f03-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95f03-107">Syntax</span></span>

``` syntax
class Win32_TSApplicationFileExtensions : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="95f03-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="95f03-108">Members</span></span>

<span data-ttu-id="95f03-109">La **clase \_ TSApplicationFileExtensions de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95f03-109">The **Win32\_TSApplicationFileExtensions** class has these types of members:</span></span>

-   [<span data-ttu-id="95f03-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="95f03-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="95f03-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95f03-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95f03-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="95f03-112">Methods</span></span>

<span data-ttu-id="95f03-113">La clase **Win32 \_ TSApplicationFileExtensions** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="95f03-113">The **Win32\_TSApplicationFileExtensions** class has these methods.</span></span>



| <span data-ttu-id="95f03-114">Método</span><span class="sxs-lookup"><span data-stu-id="95f03-114">Method</span></span>                                                                         | <span data-ttu-id="95f03-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="95f03-115">Description</span></span>                                                                                |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95f03-116">**FileAssociations**</span><span class="sxs-lookup"><span data-stu-id="95f03-116">**FileAssociations**</span></span>](fileassociations-win32-tsapplicationfileextensions.md) | <span data-ttu-id="95f03-117">Examina el registro para obtener las asociaciones de archivo actuales para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="95f03-117">Scans the registry to get the current file associations for an application.</span></span><br/>     |
| [<span data-ttu-id="95f03-118">**FileExtensions**</span><span class="sxs-lookup"><span data-stu-id="95f03-118">**FileExtensions**</span></span>](fileextensions-win32-tsapplicationfileextensions.md)     | <span data-ttu-id="95f03-119">Proporciona una lista de las extensiones de nombre de archivo controladas por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="95f03-119">Provides a list of the file name extensions that are handled by an application.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="95f03-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95f03-120">Properties</span></span>

<span data-ttu-id="95f03-121">La **clase \_ TSApplicationFileExtensions de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95f03-121">The **Win32\_TSApplicationFileExtensions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95f03-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="95f03-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f03-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95f03-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f03-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95f03-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f03-125">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95f03-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95f03-126">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="95f03-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="95f03-127">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95f03-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95f03-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="95f03-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f03-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95f03-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f03-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95f03-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f03-131">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="95f03-131">Description of the object.</span></span>

<span data-ttu-id="95f03-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95f03-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95f03-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95f03-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f03-134">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95f03-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95f03-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95f03-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f03-136">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="95f03-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="95f03-137">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="95f03-137">The date the object was installed.</span></span> <span data-ttu-id="95f03-138">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="95f03-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="95f03-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95f03-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95f03-140">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="95f03-140">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f03-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95f03-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f03-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95f03-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95f03-143">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="95f03-143">The name of the object.</span></span>

<span data-ttu-id="95f03-144">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95f03-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95f03-145">**Estado**</span><span class="sxs-lookup"><span data-stu-id="95f03-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95f03-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="95f03-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95f03-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95f03-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95f03-148">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="95f03-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="95f03-149">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="95f03-149">Current status of the object.</span></span> <span data-ttu-id="95f03-150">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="95f03-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="95f03-151">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="95f03-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="95f03-152">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="95f03-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="95f03-153">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="95f03-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="95f03-154">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="95f03-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="95f03-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95f03-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="95f03-156">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="95f03-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-157">("Error")</span><span class="sxs-lookup"><span data-stu-id="95f03-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-158">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="95f03-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-159">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="95f03-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-160">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="95f03-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-161">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="95f03-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-162">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="95f03-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95f03-163">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="95f03-163">("Service")</span></span>


<span data-ttu-id="95f03-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="95f03-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="95f03-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95f03-165">Remarks</span></span>

<span data-ttu-id="95f03-166">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="95f03-166">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="95f03-167">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="95f03-167">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="95f03-168">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="95f03-168">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span>

<span data-ttu-id="95f03-169">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="95f03-169">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="95f03-170">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="95f03-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95f03-171">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="95f03-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="95f03-172">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="95f03-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95f03-173">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="95f03-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="95f03-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95f03-174">Requirements</span></span>



| <span data-ttu-id="95f03-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f03-175">Requirement</span></span> | <span data-ttu-id="95f03-176">Value</span><span class="sxs-lookup"><span data-stu-id="95f03-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95f03-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95f03-177">Minimum supported client</span></span><br/> | <span data-ttu-id="95f03-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95f03-178">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95f03-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95f03-179">Minimum supported server</span></span><br/> | <span data-ttu-id="95f03-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95f03-180">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95f03-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95f03-181">Namespace</span></span><br/>                | <span data-ttu-id="95f03-182">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="95f03-182">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="95f03-183">MOF</span><span class="sxs-lookup"><span data-stu-id="95f03-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95f03-184"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95f03-184"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="95f03-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95f03-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95f03-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95f03-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


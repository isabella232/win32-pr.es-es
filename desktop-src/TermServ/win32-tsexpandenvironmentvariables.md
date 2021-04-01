---
title: Win32_TSExpandEnvironmentVariables (clase)
description: Expande las variables de entorno definidas por el sistema. | Win32_TSExpandEnvironmentVariables (clase)
ms.assetid: f79d4fa2-1a6e-4a2f-a637-b62f05cfd2ad
ms.tgt_platform: multiple
keywords:
- Win32_TSExpandEnvironmentVariables clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSExpandEnvironmentVariables de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables.Caption
- Win32_TSExpandEnvironmentVariables.Description
- Win32_TSExpandEnvironmentVariables.InstallDate
- Win32_TSExpandEnvironmentVariables.Name
- Win32_TSExpandEnvironmentVariables.Status
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d6bbd1a4167de703204fcf5abe345fd1bb216c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914525"
---
# <a name="win32_tsexpandenvironmentvariables-class"></a><span data-ttu-id="a7441-106">\_Clase Win32 TSExpandEnvironmentVariables</span><span class="sxs-lookup"><span data-stu-id="a7441-106">Win32\_TSExpandEnvironmentVariables class</span></span>

<span data-ttu-id="a7441-107">Expande las variables de entorno definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a7441-107">Expands system-defined environment variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7441-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7441-108">Syntax</span></span>

``` syntax
class Win32_TSExpandEnvironmentVariables : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a7441-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a7441-109">Members</span></span>

<span data-ttu-id="a7441-110">La **clase \_ TSExpandEnvironmentVariables de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a7441-110">The **Win32\_TSExpandEnvironmentVariables** class has these types of members:</span></span>

-   [<span data-ttu-id="a7441-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a7441-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="a7441-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7441-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a7441-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a7441-113">Methods</span></span>

<span data-ttu-id="a7441-114">La clase **Win32 \_ TSExpandEnvironmentVariables** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a7441-114">The **Win32\_TSExpandEnvironmentVariables** class has these methods.</span></span>



| <span data-ttu-id="a7441-115">Método</span><span class="sxs-lookup"><span data-stu-id="a7441-115">Method</span></span>                                                                                  | <span data-ttu-id="a7441-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7441-116">Description</span></span>                                              |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="a7441-117">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="a7441-117">**EnvironmentVariables**</span></span>](environmentvariables-win32-tsexpandenvironmentvariables.md) | <span data-ttu-id="a7441-118">Expande las variables de entorno definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a7441-118">Expands system-defined environment variables.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a7441-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a7441-119">Properties</span></span>

<span data-ttu-id="a7441-120">La **clase \_ TSExpandEnvironmentVariables de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a7441-120">The **Win32\_TSExpandEnvironmentVariables** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7441-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a7441-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7441-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a7441-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7441-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7441-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7441-124">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a7441-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a7441-125">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="a7441-125">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a7441-126">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7441-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7441-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a7441-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7441-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a7441-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7441-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7441-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7441-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a7441-130">Description of the object.</span></span>

<span data-ttu-id="a7441-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7441-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7441-132">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7441-132">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7441-133">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7441-133">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7441-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7441-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7441-135">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="a7441-135">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a7441-136">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a7441-136">The date the object was installed.</span></span> <span data-ttu-id="a7441-137">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a7441-137">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a7441-138">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7441-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7441-139">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a7441-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7441-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a7441-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7441-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7441-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a7441-142">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="a7441-142">The name of the object.</span></span>

<span data-ttu-id="a7441-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7441-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7441-144">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a7441-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7441-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a7441-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7441-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a7441-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7441-147">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a7441-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a7441-148">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a7441-148">Current status of the object.</span></span> <span data-ttu-id="a7441-149">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="a7441-149">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a7441-150">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a7441-150">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a7441-151">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a7441-151">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a7441-152">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a7441-152">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a7441-153">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a7441-153">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a7441-154">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7441-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a7441-155">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="a7441-155">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-156">("Error")</span><span class="sxs-lookup"><span data-stu-id="a7441-156">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-157">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="a7441-157">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-158">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="a7441-158">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-159">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a7441-159">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-160">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a7441-160">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-161">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="a7441-161">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a7441-162">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="a7441-162">("Service")</span></span>


<span data-ttu-id="a7441-163"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a7441-163"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a7441-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7441-164">Remarks</span></span>

<span data-ttu-id="a7441-165">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a7441-165">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="a7441-166">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="a7441-166">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="a7441-167">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="a7441-167">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="a7441-168">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="a7441-168">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="a7441-169">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a7441-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a7441-170">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="a7441-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a7441-171">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a7441-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a7441-172">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a7441-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7441-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7441-173">Requirements</span></span>



| <span data-ttu-id="a7441-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7441-174">Requirement</span></span> | <span data-ttu-id="a7441-175">Value</span><span class="sxs-lookup"><span data-stu-id="a7441-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7441-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7441-176">Minimum supported client</span></span><br/> | <span data-ttu-id="a7441-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7441-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7441-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7441-178">Minimum supported server</span></span><br/> | <span data-ttu-id="a7441-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7441-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7441-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a7441-180">Namespace</span></span><br/>                | <span data-ttu-id="a7441-181">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a7441-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a7441-182">MOF</span><span class="sxs-lookup"><span data-stu-id="a7441-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7441-183"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7441-183"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="a7441-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7441-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7441-185"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7441-185"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


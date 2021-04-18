---
description: Puede usar los métodos del objeto SWbemLocator para obtener un objeto SWbemServices que representa una conexión a un espacio de nombres en un equipo local o en un equipo host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Objeto SWbemLocator (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697250"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="6c3ed-103">Objeto SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="6c3ed-103">SWbemLocator object</span></span>

<span data-ttu-id="6c3ed-104">Puede usar los métodos del objeto **SWbemLocator** para obtener un objeto [**SWbemServices**](swbemservices.md) que representa una conexión a un espacio de nombres en un equipo local o en un equipo host remoto.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="6c3ed-105">Después, puede usar los métodos del objeto **SWbemServices** para tener acceso a WMI.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="6c3ed-106">Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="6c3ed-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c3ed-107">Members</span></span>

<span data-ttu-id="6c3ed-108">El objeto **SWbemLocator** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6c3ed-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="6c3ed-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c3ed-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6c3ed-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c3ed-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6c3ed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c3ed-111">Methods</span></span>

<span data-ttu-id="6c3ed-112">El objeto **SWbemLocator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="6c3ed-113">Método</span><span class="sxs-lookup"><span data-stu-id="6c3ed-113">Method</span></span>                                              | <span data-ttu-id="6c3ed-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c3ed-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="6c3ed-115">**ConnectServer**</span><span class="sxs-lookup"><span data-stu-id="6c3ed-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="6c3ed-116">Se conecta a WMI en el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6c3ed-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c3ed-117">Properties</span></span>

<span data-ttu-id="6c3ed-118">El objeto **SWbemLocator** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="6c3ed-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c3ed-119">Property</span></span>                                                | <span data-ttu-id="6c3ed-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="6c3ed-120">Access type</span></span>          | <span data-ttu-id="6c3ed-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c3ed-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="6c3ed-122">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="6c3ed-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="6c3ed-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6c3ed-123">Read-only</span></span><br/> | <span data-ttu-id="6c3ed-124">Se usa para leer o cambiar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c3ed-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c3ed-125">Remarks</span></span>

<span data-ttu-id="6c3ed-126">En la parte superior del modelo de objetos de la biblioteca de scripting de WMI se encuentra el objeto SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="6c3ed-127">SWbemLocator se utiliza para establecer una conexión autenticada con un espacio de nombres WMI, de forma muy similar a la función GetObject de VBScript y el moniker de WMI "winmgmts:" se usa para establecer una conexión autenticada con WMI.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="6c3ed-128">Sin embargo, SWbemLocator está diseñado para abordar dos escenarios de scripting específicos que no se pueden realizar mediante GetObject y el moniker de WMI.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="6c3ed-129">Debe usar SWbemLocator si necesita:</span><span class="sxs-lookup"><span data-stu-id="6c3ed-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="6c3ed-130">Proporcione las credenciales de usuario y contraseña para conectarse a WMI en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="6c3ed-131">El moniker de WMI utilizado con la función GetObject no incluye un mecanismo para especificar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="6c3ed-132">La mayoría de las actividades de WMI (incluidas todas las que se llevan a cabo en equipos remotos) requieren derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="6c3ed-133">Si normalmente inicia sesión con una cuenta de usuario normal en lugar de una cuenta de administrador, no podrá realizar la mayoría de las tareas de WMI a menos que ejecute el script en credenciales alternativas.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="6c3ed-134">Conéctese a WMI si está ejecutando un script de WMI desde una página web.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="6c3ed-135">No se puede usar la función GetObject al ejecutar scripts insertados en una página HTML porque Internet Explorer no permite el uso de GetObject por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="6c3ed-136">Además, es posible que desee usar SWbemLocator para conectarse a WMI si encuentra la cadena de conexión WMI que se usa con GetObject confuso o difícil.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="6c3ed-137">Use CreateObject en lugar de GetObject para crear una referencia a SWbemLocator.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="6c3ed-138">Para crear la referencia, debe pasar la función CreateObject al identificador de programación de SWbemLocator (ProgID) "WbemScripting. SWbemLocator", como se muestra en la línea 2 del siguiente ejemplo de script.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="6c3ed-139">Después de obtener una referencia a un objeto SWbemLocator, llame al método ConnectServer para conectarse a WMI y obtener una referencia a un objeto SWbemServices.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="6c3ed-140">Esto se muestra en la línea 3 del script siguiente.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="6c3ed-141">Para ejecutar un script en credenciales alternativas, incluya el nombre de usuario y la contraseña como parámetros adicionales que se pasan a ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="6c3ed-142">Por ejemplo, este script se ejecuta con las credenciales de un usuario llamado kenmyer, con la contraseña homerj.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="6c3ed-143">También puede usar el formato de \\ nombre de usuario de dominio para especificar un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="6c3ed-144">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6c3ed-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="6c3ed-145">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6c3ed-145">Examples</span></span>

<span data-ttu-id="6c3ed-146">En el siguiente ejemplo de PowerShell se usa **SWbemLocator** para conectarse a un servidor.</span><span class="sxs-lookup"><span data-stu-id="6c3ed-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="6c3ed-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c3ed-147">Requirements</span></span>



| <span data-ttu-id="6c3ed-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c3ed-148">Requirement</span></span> | <span data-ttu-id="6c3ed-149">Value</span><span class="sxs-lookup"><span data-stu-id="6c3ed-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3ed-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3ed-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3ed-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c3ed-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c3ed-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c3ed-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3ed-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c3ed-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c3ed-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c3ed-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3ed-155"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ed-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c3ed-156">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6c3ed-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c3ed-157"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ed-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c3ed-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c3ed-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c3ed-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c3ed-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c3ed-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="6c3ed-160">CLSID</span></span><br/>                    | <span data-ttu-id="6c3ed-161">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="6c3ed-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="6c3ed-162">IID</span><span class="sxs-lookup"><span data-stu-id="6c3ed-162">IID</span></span><br/>                      | <span data-ttu-id="6c3ed-163">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="6c3ed-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="6c3ed-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c3ed-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3ed-165">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="6c3ed-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





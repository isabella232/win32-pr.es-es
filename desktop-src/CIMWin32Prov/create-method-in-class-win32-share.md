---
description: Inicia el uso compartido para un recurso de servidor.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Método Create de la clase Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000837"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="cc6e8-103">Método Create de la \_ clase de recurso compartido Win32</span><span class="sxs-lookup"><span data-stu-id="cc6e8-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="cc6e8-104">El método **crear**   [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) inicia el uso compartido para un recurso de servidor.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="cc6e8-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="cc6e8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cc6e8-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cc6e8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6e8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc6e8-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="cc6e8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc6e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6e8-109">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-110">Ruta de acceso local del recurso compartido de Windows.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-110">Local path of the Windows share.</span></span>

<span data-ttu-id="cc6e8-111">Ejemplo, "C: \\ archivos de programa".</span><span class="sxs-lookup"><span data-stu-id="cc6e8-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="cc6e8-112">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-113">Pasa el alias a una ruta de acceso configurada como un recurso compartido en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="cc6e8-114">Ejemplo, "Public".</span><span class="sxs-lookup"><span data-stu-id="cc6e8-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="cc6e8-115">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-116">Pasa el tipo de recurso que se comparte.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="cc6e8-117">Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="cc6e8-118">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="cc6e8-119">**Unidad de disco** (0)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="cc6e8-120">**Cola de impresión** (1)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="cc6e8-121">**Dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="cc6e8-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="cc6e8-123">**Administrador de unidad de disco** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="cc6e8-124">**Administrador** de la cola de impresión (2147483649)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="cc6e8-125">**Administrador de dispositivos** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="cc6e8-126">**Administración de IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="cc6e8-127">*MaximumAllowed* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-128">Límite en el número máximo de usuarios a los que se permite usar este recurso simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="cc6e8-129">Ejemplo: 10.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-129">Example: 10.</span></span> <span data-ttu-id="cc6e8-130">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="cc6e8-131">*Descripción* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-132">Comentario opcional para describir el recurso que se está compartiendo.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="cc6e8-133">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="cc6e8-134">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-135">Contraseña (cuando el servidor se ejecuta con seguridad de nivel de recurso compartido) para el recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="cc6e8-136">Si el servidor se ejecuta con seguridad de nivel de usuario, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="cc6e8-137">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="cc6e8-138">*Acceso a* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cc6e8-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6e8-139">Descriptor de seguridad para permisos de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="cc6e8-140">Un descriptor de seguridad contiene información sobre los permisos, el propietario y las capacidades de acceso del recurso.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="cc6e8-141">Si no se proporciona este parámetro o es **null**, todos tienen acceso de lectura al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="cc6e8-142">Para obtener más información, [**vea \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) y [cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="cc6e8-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6e8-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc6e8-143">Return value</span></span>

<span data-ttu-id="cc6e8-144">Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="cc6e8-145">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="cc6e8-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="cc6e8-146">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="cc6e8-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="cc6e8-147">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-148">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-149">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-150">**Nombre no válido** (9)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-151">**Nivel no válido** (10)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-152">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-153">**Recurso compartido duplicado** (22)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-154">**Ruta de acceso redirigida** (23)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-155">**Dispositivo o directorio desconocido** (24)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-156">**No se encontró el nombre de red** (25)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="cc6e8-157">**Otro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="cc6e8-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cc6e8-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc6e8-158">Remarks</span></span>

<span data-ttu-id="cc6e8-159">**Create** es un método estático.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-159">**Create** is a static method.</span></span>

<span data-ttu-id="cc6e8-160">Solo los miembros del grupo local Administradores o operadores de cuenta, o los que tengan la pertenencia a un grupo de operador de servidor o de comunicación pueden ejecutar **Create** correctamente.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="cc6e8-161">El operador Print solo puede Agregar colas de impresión.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="cc6e8-162">El operador de comunicación solo puede Agregar colas de dispositivos de comunicación.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="cc6e8-163">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc6e8-163">Examples</span></span>

<span data-ttu-id="cc6e8-164">El ejemplo de PowerShell [Export e import recursos compartidos](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) exporta e importa recursos compartidos de archivos y establece permisos de recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="cc6e8-165">Del mismo modo, el ejemplo de [creación de un recurso compartido y set permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) también crea un nuevo recurso compartido y establece los permisos del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="cc6e8-166">El siguiente código de PowerShell crea un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="cc6e8-167">El ejemplo de código anterior devuelve lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cc6e8-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="cc6e8-168">El siguiente \# ejemplo de código C describe cómo llamar al método Create.</span><span class="sxs-lookup"><span data-stu-id="cc6e8-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="cc6e8-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc6e8-169">Requirements</span></span>



| <span data-ttu-id="cc6e8-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6e8-170">Requirement</span></span> | <span data-ttu-id="cc6e8-171">Value</span><span class="sxs-lookup"><span data-stu-id="cc6e8-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6e8-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6e8-172">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6e8-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc6e8-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc6e8-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6e8-174">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6e8-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc6e8-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc6e8-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc6e8-176">Namespace</span></span><br/>                | <span data-ttu-id="cc6e8-177">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc6e8-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc6e8-178">MOF</span><span class="sxs-lookup"><span data-stu-id="cc6e8-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc6e8-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc6e8-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc6e8-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc6e8-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc6e8-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc6e8-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6e8-182">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc6e8-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc6e8-183">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc6e8-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cc6e8-184">**\_Recurso compartido de Win32**</span><span class="sxs-lookup"><span data-stu-id="cc6e8-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 


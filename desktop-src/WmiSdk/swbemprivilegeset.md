---
description: Un objeto SWbemPrivilegeSet es una colección de objetos SWbemPrivilege de un objeto SWbemSecurity que solicita privilegios específicos para un objeto Instrumental de administración de Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objeto SWbemPrivilegeSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360543"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="bbe14-103">Objeto SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="bbe14-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="bbe14-104">Un objeto **SWbemPrivilegeSet** es una colección de objetos [**SWbemPrivilege**](swbemprivilege.md) de un objeto [**SWbemSecurity**](swbemsecurity.md) que solicita privilegios específicos para un objeto instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bbe14-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="bbe14-105">Consulte la lista de privilegios en las [**constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bbe14-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="bbe14-106">Los elementos se agregan a la colección mediante los métodos [**Add**](swbemprivilegeset-add.md) y [**AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe14-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="bbe14-107">Los elementos se recuperan de la colección mediante el método [**Item**](swbemprivilegeset-item.md) y se quitan mediante el método [**Remove**](swbemprivilegeset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe14-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="bbe14-108">Este objeto no se puede crear mediante la llamada al método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="bbe14-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="bbe14-109">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="bbe14-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="bbe14-110">Un objeto **SWbemPrivilegeSet** es un conjunto de solicitudes de invalidación de privilegios para un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="bbe14-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="bbe14-111">Cuando se realiza una llamada API mediante este objeto, se intentan las solicitudes de invalidación de privilegios.</span><span class="sxs-lookup"><span data-stu-id="bbe14-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="bbe14-112">El objeto **SWbemPrivilegeSet** no define los privilegios disponibles para el usuario o el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="bbe14-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="bbe14-113">En otras palabras, la obtención de los privilegios de cualquier objeto WMI no identifica la configuración de privilegios que se realiza en la conexión a WMI o los privilegios en vigor cuando se entrega un objeto a un receptor.</span><span class="sxs-lookup"><span data-stu-id="bbe14-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="bbe14-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbe14-114">Members</span></span>

<span data-ttu-id="bbe14-115">El objeto **SWbemPrivilegeSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bbe14-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="bbe14-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbe14-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="bbe14-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbe14-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bbe14-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbe14-118">Methods</span></span>

<span data-ttu-id="bbe14-119">El objeto **SWbemPrivilegeSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bbe14-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="bbe14-120">Método</span><span class="sxs-lookup"><span data-stu-id="bbe14-120">Method</span></span>                                               | <span data-ttu-id="bbe14-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbe14-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbe14-122">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="bbe14-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="bbe14-123">Agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la colección **SWbemPrivilegeSet** mediante una constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="bbe14-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="bbe14-124">**AddAsString**</span><span class="sxs-lookup"><span data-stu-id="bbe14-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="bbe14-125">Agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la colección **SWbemPrivilegeSet** mediante una cadena de privilegios.</span><span class="sxs-lookup"><span data-stu-id="bbe14-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="bbe14-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="bbe14-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="bbe14-127">Elimina todos los privilegios de la colección.</span><span class="sxs-lookup"><span data-stu-id="bbe14-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="bbe14-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bbe14-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="bbe14-129">Recupera un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="bbe14-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="bbe14-130">Este es el método predeterminado de este objeto.</span><span class="sxs-lookup"><span data-stu-id="bbe14-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="bbe14-131">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="bbe14-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="bbe14-132">Quita un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="bbe14-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="bbe14-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbe14-133">Properties</span></span>

<span data-ttu-id="bbe14-134">El objeto **SWbemPrivilegeSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbe14-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="bbe14-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbe14-135">Property</span></span>                                            | <span data-ttu-id="bbe14-136">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bbe14-136">Access type</span></span>          | <span data-ttu-id="bbe14-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbe14-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="bbe14-138">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="bbe14-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="bbe14-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbe14-139">Read-only</span></span><br/> | <span data-ttu-id="bbe14-140">Número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="bbe14-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="bbe14-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bbe14-141">Examples</span></span>

<span data-ttu-id="bbe14-142">En el siguiente ejemplo de código de VBScript se obtiene un objeto SWbemPrivileges y se agregan todos los privilegios disponibles a la colección por valor de privilegio, tal y como se define en [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="bbe14-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="bbe14-143">En el ejemplo de código de VBScript siguiente se muestra cómo agregar privilegios mediante el objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="bbe14-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="bbe14-144">En el ejemplo de código Perl siguiente se muestra cómo agregar privilegios mediante el objeto **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="bbe14-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="bbe14-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbe14-145">Requirements</span></span>



| <span data-ttu-id="bbe14-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe14-146">Requirement</span></span> | <span data-ttu-id="bbe14-147">Value</span><span class="sxs-lookup"><span data-stu-id="bbe14-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe14-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbe14-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe14-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbe14-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbe14-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbe14-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe14-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbe14-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbe14-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbe14-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe14-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe14-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bbe14-154">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bbe14-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbe14-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bbe14-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bbe14-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbe14-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe14-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe14-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bbe14-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="bbe14-158">CLSID</span></span><br/>                    | <span data-ttu-id="bbe14-159">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="bbe14-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="bbe14-160">IID</span><span class="sxs-lookup"><span data-stu-id="bbe14-160">IID</span></span><br/>                      | <span data-ttu-id="bbe14-161">\_ISWBEMPRIVILEGESET IID</span><span class="sxs-lookup"><span data-stu-id="bbe14-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="bbe14-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbe14-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe14-163">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="bbe14-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="bbe14-164">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="bbe14-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="bbe14-165">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="bbe14-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="bbe14-166">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="bbe14-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="bbe14-167">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="bbe14-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 


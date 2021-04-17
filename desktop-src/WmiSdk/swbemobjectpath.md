---
description: Use los métodos y las propiedades del objeto SWbemObjectPath para construir y validar una ruta de acceso de objeto. Este objeto se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objeto SWbemObjectPath (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706045"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="602d6-104">Objeto SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="602d6-104">SWbemObjectPath object</span></span>

<span data-ttu-id="602d6-105">Use los métodos y las propiedades del objeto **SWbemObjectPath** para construir y validar una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="602d6-106">Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="602d6-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="602d6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="602d6-107">Members</span></span>

<span data-ttu-id="602d6-108">El objeto **SWbemObjectPath** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="602d6-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="602d6-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="602d6-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="602d6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="602d6-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="602d6-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="602d6-111">Methods</span></span>

<span data-ttu-id="602d6-112">El objeto **SWbemObjectPath** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="602d6-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="602d6-113">Método</span><span class="sxs-lookup"><span data-stu-id="602d6-113">Method</span></span>                                                   | <span data-ttu-id="602d6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="602d6-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="602d6-115">**SetAsClass**</span><span class="sxs-lookup"><span data-stu-id="602d6-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="602d6-116">Fuerza la ruta de acceso a una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="602d6-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="602d6-117">**SetAsSingleton**</span><span class="sxs-lookup"><span data-stu-id="602d6-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="602d6-118">Fuerza a la ruta de acceso a una instancia de WMI singleton.</span><span class="sxs-lookup"><span data-stu-id="602d6-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="602d6-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="602d6-119">Properties</span></span>

<span data-ttu-id="602d6-120">El objeto **SWbemObjectPath** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="602d6-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="602d6-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="602d6-121">Property</span></span>                                                              | <span data-ttu-id="602d6-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="602d6-122">Access type</span></span>           | <span data-ttu-id="602d6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="602d6-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="602d6-124">**Autoridad**</span><span class="sxs-lookup"><span data-stu-id="602d6-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="602d6-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-125">Read/write</span></span><br/> | <span data-ttu-id="602d6-126">Cadena que define el componente de autoridad de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="602d6-127">**Las**</span><span class="sxs-lookup"><span data-stu-id="602d6-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="602d6-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-128">Read/write</span></span><br/> | <span data-ttu-id="602d6-129">Nombre de la clase que forma parte de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="602d6-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="602d6-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="602d6-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-131">Read/write</span></span><br/> | <span data-ttu-id="602d6-132">Cadena que contiene la ruta de acceso en un formulario que se puede utilizar como nombre para mostrar del moniker.</span><span class="sxs-lookup"><span data-stu-id="602d6-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="602d6-133">Vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="602d6-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="602d6-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="602d6-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="602d6-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="602d6-135">Read-only</span></span><br/>  | <span data-ttu-id="602d6-136">Valor booleano que indica si esta ruta de acceso representa una clase.</span><span class="sxs-lookup"><span data-stu-id="602d6-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="602d6-137">Esto es análogo a la propiedad [ \_ \_ género](wmi-system-properties.md) de la API com.</span><span class="sxs-lookup"><span data-stu-id="602d6-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="602d6-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="602d6-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="602d6-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="602d6-139">Read-only</span></span><br/>  | <span data-ttu-id="602d6-140">Valor booleano que indica si esta ruta de acceso representa una instancia de singleton.</span><span class="sxs-lookup"><span data-stu-id="602d6-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="602d6-141">**Claves**</span><span class="sxs-lookup"><span data-stu-id="602d6-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="602d6-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="602d6-142">Read-only</span></span><br/>  | <span data-ttu-id="602d6-143">Un objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contiene los enlaces de valor de clave.</span><span class="sxs-lookup"><span data-stu-id="602d6-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="602d6-144">**Configuración regional**</span><span class="sxs-lookup"><span data-stu-id="602d6-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="602d6-145">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-145">Read/write</span></span><br/> | <span data-ttu-id="602d6-146">Cadena que contiene la configuración regional de esta ruta de acceso al objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="602d6-147">**System.IO**</span><span class="sxs-lookup"><span data-stu-id="602d6-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="602d6-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-148">Read/write</span></span><br/> | <span data-ttu-id="602d6-149">Nombre del espacio de nombres que forma parte de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="602d6-150">Es igual que la propiedad de [ \_ \_ espacio de nombres](wmi-system-properties.md) de la API de com.</span><span class="sxs-lookup"><span data-stu-id="602d6-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="602d6-151">**ParentNamespace**</span><span class="sxs-lookup"><span data-stu-id="602d6-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="602d6-152">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="602d6-152">Read-only</span></span><br/>  | <span data-ttu-id="602d6-153">Nombre del elemento primario del espacio de nombres que forma parte de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="602d6-154">**Ruta**</span><span class="sxs-lookup"><span data-stu-id="602d6-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="602d6-155">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-155">Read/write</span></span><br/> | <span data-ttu-id="602d6-156">Contiene la ruta de acceso absoluta.</span><span class="sxs-lookup"><span data-stu-id="602d6-156">Contains the absolute path.</span></span> <span data-ttu-id="602d6-157">Es el mismo que la propiedad del sistema [ \_ \_ path](wmi-system-properties.md) de la API com.</span><span class="sxs-lookup"><span data-stu-id="602d6-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="602d6-158">Esta es la propiedad predeterminada de este objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="602d6-159">**Relpath**</span><span class="sxs-lookup"><span data-stu-id="602d6-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="602d6-160">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-160">Read/write</span></span><br/> | <span data-ttu-id="602d6-161">Contiene la ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="602d6-161">Contains the relative path.</span></span> <span data-ttu-id="602d6-162">Es igual que la propiedad del sistema [ \_ \_ Relpath](wmi-system-properties.md) en la API de com.</span><span class="sxs-lookup"><span data-stu-id="602d6-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="602d6-163">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="602d6-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="602d6-164">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="602d6-164">Read-only</span></span><br/>  | <span data-ttu-id="602d6-165">Se usa para leer o cambiar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="602d6-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="602d6-166">**Server**</span><span class="sxs-lookup"><span data-stu-id="602d6-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="602d6-167">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="602d6-167">Read/write</span></span><br/> | <span data-ttu-id="602d6-168">Nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="602d6-168">Name of the server.</span></span> <span data-ttu-id="602d6-169">Es igual que la propiedad del sistema del [ \_ \_ servidor](wmi-system-properties.md) de la API de com.</span><span class="sxs-lookup"><span data-stu-id="602d6-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="602d6-170">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="602d6-170">Examples</span></span>

<span data-ttu-id="602d6-171">El siguiente ejemplo de código VBScript muestra cómo compilar rutas de objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="602d6-172">El siguiente ejemplo de código Perl muestra cómo compilar rutas de objeto.</span><span class="sxs-lookup"><span data-stu-id="602d6-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="602d6-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="602d6-173">Requirements</span></span>



| <span data-ttu-id="602d6-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="602d6-174">Requirement</span></span> | <span data-ttu-id="602d6-175">Value</span><span class="sxs-lookup"><span data-stu-id="602d6-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="602d6-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602d6-176">Minimum supported client</span></span><br/> | <span data-ttu-id="602d6-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="602d6-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="602d6-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="602d6-178">Minimum supported server</span></span><br/> | <span data-ttu-id="602d6-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="602d6-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="602d6-180">Encabezado</span><span class="sxs-lookup"><span data-stu-id="602d6-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="602d6-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="602d6-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="602d6-182">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="602d6-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="602d6-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="602d6-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="602d6-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="602d6-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="602d6-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="602d6-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="602d6-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="602d6-186">CLSID</span></span><br/>                    | <span data-ttu-id="602d6-187">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="602d6-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="602d6-188">IID</span><span class="sxs-lookup"><span data-stu-id="602d6-188">IID</span></span><br/>                      | <span data-ttu-id="602d6-189">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="602d6-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="602d6-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="602d6-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="602d6-191">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="602d6-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





---
description: Un objeto SWbemObjectSet es una colección de objetos SWbemObject. Para obtener más información, vea obtener acceso a una colección. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objeto SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279100"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="3015b-105">Objeto SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="3015b-105">SWbemObjectSet object</span></span>

<span data-ttu-id="3015b-106">Un objeto **SWbemObjectSet** es una colección de objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="3015b-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="3015b-107">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="3015b-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="3015b-108">Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="3015b-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="3015b-109">Puede obtener un objeto **SWbemObjectSet** llamando a cualquiera de los métodos siguientes o a sus equivalentes asincrónicos:</span><span class="sxs-lookup"><span data-stu-id="3015b-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="3015b-110">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="3015b-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="3015b-111">**SWbemObject. instances\_**</span><span class="sxs-lookup"><span data-stu-id="3015b-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="3015b-112">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="3015b-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="3015b-113">**SWbemObject. subclases\_**</span><span class="sxs-lookup"><span data-stu-id="3015b-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="3015b-114">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="3015b-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="3015b-115">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="3015b-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="3015b-116">**SWbemServices. instances**</span><span class="sxs-lookup"><span data-stu-id="3015b-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="3015b-117">**SWbemServices. References**</span><span class="sxs-lookup"><span data-stu-id="3015b-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="3015b-118">**SWbemServices. subclasses**</span><span class="sxs-lookup"><span data-stu-id="3015b-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="3015b-119">El objeto **SWbemObjectSet** no admite los métodos opcionales para **Agregar** y **quitar** colecciones.</span><span class="sxs-lookup"><span data-stu-id="3015b-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="3015b-120">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="3015b-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="3015b-121">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="3015b-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="3015b-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="3015b-122">Members</span></span>

<span data-ttu-id="3015b-123">El objeto **SWbemObjectSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3015b-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="3015b-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="3015b-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="3015b-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3015b-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3015b-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="3015b-126">Methods</span></span>

<span data-ttu-id="3015b-127">El objeto **SWbemObjectSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3015b-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="3015b-128">Método</span><span class="sxs-lookup"><span data-stu-id="3015b-128">Method</span></span>                              | <span data-ttu-id="3015b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3015b-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3015b-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3015b-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="3015b-131">Recupera un objeto [**SWbemObject**](swbemobject.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="3015b-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="3015b-132">Este es el método predeterminado del objeto.</span><span class="sxs-lookup"><span data-stu-id="3015b-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3015b-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3015b-133">Properties</span></span>

<span data-ttu-id="3015b-134">El objeto **SWbemObjectSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3015b-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="3015b-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3015b-135">Property</span></span>                                                  | <span data-ttu-id="3015b-136">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="3015b-136">Access type</span></span>          | <span data-ttu-id="3015b-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="3015b-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="3015b-138">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="3015b-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="3015b-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3015b-139">Read-only</span></span><br/> | <span data-ttu-id="3015b-140">Número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="3015b-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="3015b-141">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="3015b-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="3015b-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3015b-142">Read-only</span></span><br/> | <span data-ttu-id="3015b-143">Se usa para leer o cambiar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3015b-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3015b-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3015b-144">Remarks</span></span>

<span data-ttu-id="3015b-145">Un **SWbemObjectSet** es una colección de cero o más objetos [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="3015b-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="3015b-146">Cada **SWbemObject** de un **SWbemObjectSet** puede representar una de estas dos cosas:</span><span class="sxs-lookup"><span data-stu-id="3015b-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="3015b-147">Instancia de un recurso administrado por WMI.</span><span class="sxs-lookup"><span data-stu-id="3015b-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="3015b-148">Una instancia de una definición de clase.</span><span class="sxs-lookup"><span data-stu-id="3015b-148">An instance of a class definition.</span></span>

<span data-ttu-id="3015b-149">El uso más común de esta clase en WMI es como el valor devuelto para una llamada a [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) o a [**instancias**](swbemservices-instancesof.md) , como se describe en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3015b-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="3015b-150">En su mayor parte, lo único que tendrá que hacer con un **SWbemObjectSet** es enumerar todos los objetos contenidos en la propia colección.</span><span class="sxs-lookup"><span data-stu-id="3015b-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="3015b-151">Sin embargo, **SWbemObjectSet** incluye un recuento de propiedades que puede ser útil en el scripting de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="3015b-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="3015b-152">Como implica el nombre, Count indica el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="3015b-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="3015b-153">Por ejemplo, este script recupera una colección de todos los servicios instalados en un equipo y, a continuación, devuelve el número total de servicios encontrados:</span><span class="sxs-lookup"><span data-stu-id="3015b-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="3015b-154">Para obtener más información sobre cómo usar esta clase, consulte [enumeración de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="3015b-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3015b-155">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3015b-155">Examples</span></span>

<span data-ttu-id="3015b-156">El siguiente ejemplo de código VBScript muestra cómo se manipulan las colecciones **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="3015b-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="3015b-157">El siguiente ejemplo de código Perl muestra cómo se manipulan las colecciones **SWbemObjectSet** .</span><span class="sxs-lookup"><span data-stu-id="3015b-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
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



## <a name="requirements"></a><span data-ttu-id="3015b-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3015b-158">Requirements</span></span>



| <span data-ttu-id="3015b-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="3015b-159">Requirement</span></span> | <span data-ttu-id="3015b-160">Value</span><span class="sxs-lookup"><span data-stu-id="3015b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3015b-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3015b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="3015b-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3015b-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3015b-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3015b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="3015b-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3015b-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3015b-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3015b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="3015b-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3015b-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3015b-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3015b-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="3015b-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3015b-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3015b-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3015b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3015b-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3015b-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3015b-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="3015b-171">CLSID</span></span><br/>                    | <span data-ttu-id="3015b-172">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="3015b-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="3015b-173">IID</span><span class="sxs-lookup"><span data-stu-id="3015b-173">IID</span></span><br/>                      | <span data-ttu-id="3015b-174">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="3015b-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="3015b-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="3015b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3015b-176">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="3015b-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





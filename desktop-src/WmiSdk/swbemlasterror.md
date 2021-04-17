---
description: Los métodos y las propiedades del objeto SWbemLastError contienen y manipulan los objetos de error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objeto SWbemLastError (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696798"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="dd49b-103">Objeto SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="dd49b-103">SWbemLastError object</span></span>

<span data-ttu-id="dd49b-104">Los métodos y las propiedades del objeto **SWbemLastError** contienen y manipulan los objetos de error.</span><span class="sxs-lookup"><span data-stu-id="dd49b-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="dd49b-105">Los métodos y las propiedades de este objeto son exactamente iguales que los del objeto [**SWbemObject**](swbemobject.md) , pero se usan para contener información de error en lugar de la información de clase WMI.</span><span class="sxs-lookup"><span data-stu-id="dd49b-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="dd49b-106">Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="dd49b-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="dd49b-107">Puede crear un objeto de error **SWbemLastError** para inspeccionar la información de error extendida asociada a una llamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="dd49b-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="dd49b-108">Si la información del error no está disponible, se producirá un error al intentar crear un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="dd49b-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="dd49b-109">Si la llamada se realiza correctamente y se devuelve un objeto de error, se restablece el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="dd49b-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="dd49b-110">Se producirá un error al intentar recuperar un objeto de error hasta que se produzca un nuevo error.</span><span class="sxs-lookup"><span data-stu-id="dd49b-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="dd49b-111">Si realiza una llamada asincrónica que genera un error, puede que el evento [**SWbemSink. Alcompleted**](swbemsink-oncompleted.md) devuelva un objeto **SWbemLastError** en el parámetro *objWbemErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="dd49b-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="dd49b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd49b-112">Members</span></span>

<span data-ttu-id="dd49b-113">El objeto **SWbemLastError** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd49b-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="dd49b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd49b-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd49b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd49b-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd49b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd49b-116">Methods</span></span>

<span data-ttu-id="dd49b-117">El objeto **SWbemLastError** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dd49b-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="dd49b-118">Método</span><span class="sxs-lookup"><span data-stu-id="dd49b-118">Method</span></span>                                                   | <span data-ttu-id="dd49b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd49b-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd49b-120">**Asociadores\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-120">**Associators\_**</span></span>                                        | <span data-ttu-id="dd49b-121">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-121">Not used.</span></span> <span data-ttu-id="dd49b-122">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-123">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="dd49b-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-124">Not used.</span></span> <span data-ttu-id="dd49b-125">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="dd49b-126">**Clonar\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="dd49b-127">Realiza una copia del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="dd49b-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="dd49b-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="dd49b-129">Comprueba la igualdad de dos objetos.</span><span class="sxs-lookup"><span data-stu-id="dd49b-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="dd49b-130">**Elimínelos\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-130">**Delete\_**</span></span>                                             | <span data-ttu-id="dd49b-131">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-131">Not used.</span></span> <span data-ttu-id="dd49b-132">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="dd49b-134">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-134">Not used.</span></span> <span data-ttu-id="dd49b-135">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="dd49b-137">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-137">Not used.</span></span> <span data-ttu-id="dd49b-138">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="dd49b-140">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-140">Not used.</span></span> <span data-ttu-id="dd49b-141">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="dd49b-142">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="dd49b-143">Recupera la representación textual del objeto escrito con la sintaxis MOF.</span><span class="sxs-lookup"><span data-stu-id="dd49b-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="dd49b-144">**Instancias\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-144">**Instances\_**</span></span>                                          | <span data-ttu-id="dd49b-145">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-145">Not used.</span></span> <span data-ttu-id="dd49b-146">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-147">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="dd49b-148">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-148">Not used.</span></span> <span data-ttu-id="dd49b-149">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-150">**Pondrán\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-150">**Put\_**</span></span>                                                | <span data-ttu-id="dd49b-151">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-151">Not used.</span></span> <span data-ttu-id="dd49b-152">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-153">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="dd49b-154">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-154">Not used.</span></span> <span data-ttu-id="dd49b-155">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-156">**Referencias\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-156">**References\_**</span></span>                                         | <span data-ttu-id="dd49b-157">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-157">Not used.</span></span> <span data-ttu-id="dd49b-158">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-159">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="dd49b-160">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-160">Not used.</span></span> <span data-ttu-id="dd49b-161">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="dd49b-163">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-163">Not used.</span></span> <span data-ttu-id="dd49b-164">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="dd49b-166">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-166">Not used.</span></span> <span data-ttu-id="dd49b-167">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-168">**Subclases \_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="dd49b-169">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-169">Not used.</span></span> <span data-ttu-id="dd49b-170">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="dd49b-171">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="dd49b-172">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-172">Not used.</span></span> <span data-ttu-id="dd49b-173">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dd49b-174">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd49b-174">Properties</span></span>

<span data-ttu-id="dd49b-175">El objeto **SWbemLastError** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd49b-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="dd49b-176">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dd49b-176">Property</span></span>                                                      | <span data-ttu-id="dd49b-177">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="dd49b-177">Access type</span></span>          | <span data-ttu-id="dd49b-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd49b-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd49b-179">**Derivación\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="dd49b-180">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-180">Read-only</span></span><br/> | <span data-ttu-id="dd49b-181">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-181">Not used.</span></span> <span data-ttu-id="dd49b-182">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="dd49b-183">**Métodos\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="dd49b-184">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-184">Read-only</span></span><br/> | <span data-ttu-id="dd49b-185">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-185">Not used.</span></span> <span data-ttu-id="dd49b-186">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="dd49b-187">**Ruta\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="dd49b-188">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-188">Read-only</span></span><br/> | <span data-ttu-id="dd49b-189">Contiene un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual.</span><span class="sxs-lookup"><span data-stu-id="dd49b-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="dd49b-190">**Propiedades\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="dd49b-191">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-191">Read-only</span></span><br/> | <span data-ttu-id="dd49b-192">Representa la colección de propiedades del objeto **SWbemLastError** .</span><span class="sxs-lookup"><span data-stu-id="dd49b-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="dd49b-193">Esta propiedad es un objeto [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="dd49b-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="dd49b-194">**Calificadores\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="dd49b-195">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-195">Read-only</span></span><br/> | <span data-ttu-id="dd49b-196">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-196">Not used.</span></span> <span data-ttu-id="dd49b-197">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="dd49b-198">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="dd49b-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="dd49b-199">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd49b-199">Read-only</span></span><br/> | <span data-ttu-id="dd49b-200">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd49b-200">Not used.</span></span> <span data-ttu-id="dd49b-201">El objeto [**SWbemObject**](swbemobject.md) proporciona el mismo método.</span><span class="sxs-lookup"><span data-stu-id="dd49b-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="dd49b-202">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dd49b-202">Examples</span></span>

<span data-ttu-id="dd49b-203">El siguiente ejemplo de VBScript muestra cómo inspeccionar la información de los objetos de error y error.</span><span class="sxs-lookup"><span data-stu-id="dd49b-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="dd49b-204">En el siguiente ejemplo de Perl se muestra cómo inspeccionar la información de objetos de error y error.</span><span class="sxs-lookup"><span data-stu-id="dd49b-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="dd49b-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd49b-205">Requirements</span></span>



| <span data-ttu-id="dd49b-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd49b-206">Requirement</span></span> | <span data-ttu-id="dd49b-207">Value</span><span class="sxs-lookup"><span data-stu-id="dd49b-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd49b-208">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd49b-208">Minimum supported client</span></span><br/> | <span data-ttu-id="dd49b-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd49b-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd49b-210">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd49b-210">Minimum supported server</span></span><br/> | <span data-ttu-id="dd49b-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd49b-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd49b-212">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd49b-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd49b-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd49b-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd49b-214">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dd49b-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd49b-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dd49b-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dd49b-216">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd49b-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd49b-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd49b-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd49b-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="dd49b-218">CLSID</span></span><br/>                    | <span data-ttu-id="dd49b-219">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="dd49b-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="dd49b-220">IID</span><span class="sxs-lookup"><span data-stu-id="dd49b-220">IID</span></span><br/>                      | <span data-ttu-id="dd49b-221">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="dd49b-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="dd49b-222">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd49b-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd49b-223">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="dd49b-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





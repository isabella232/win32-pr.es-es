---
description: Puede usar los métodos y las propiedades del objeto SWbemObject para representar una definición de clase Instrumental de administración de Windows (WMI) o una instancia de objeto.
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Objeto SWbemObject (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706049"
---
# <a name="swbemobject-object"></a><span data-ttu-id="970cd-103">Objeto SWbemObject</span><span class="sxs-lookup"><span data-stu-id="970cd-103">SWbemObject object</span></span>

<span data-ttu-id="970cd-104">Puede usar los métodos y las propiedades del objeto **SWbemObject** para representar una definición de clase instrumental de administración de Windows (WMI) o una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="970cd-105">Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="970cd-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="970cd-106">Este objeto admite dos tipos de propiedades y métodos.</span><span class="sxs-lookup"><span data-stu-id="970cd-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="970cd-107">Los definidos en esta sección son propiedades y métodos genéricos que se aplican a todos los objetos de WMI.</span><span class="sxs-lookup"><span data-stu-id="970cd-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="970cd-108">Además, este objeto expone las propiedades y los métodos del objeto subyacente como propiedades y métodos de automatización dinámica de **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="970cd-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="970cd-109">Los nombres y tipos de estas propiedades y métodos dependen del objeto WMI subyacente.</span><span class="sxs-lookup"><span data-stu-id="970cd-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="970cd-110">Para obtener más información sobre cómo se exponen estas propiedades y métodos dinámicos, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="970cd-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="970cd-111">Desde la perspectiva del cliente WMI, este objeto siempre está en proceso.</span><span class="sxs-lookup"><span data-stu-id="970cd-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="970cd-112">Las operaciones de escritura solo afectan a la copia local del objeto y las operaciones de lectura siempre recuperan los valores de la copia local.</span><span class="sxs-lookup"><span data-stu-id="970cd-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="970cd-113">Las actualizaciones de WMI solo se realizan cuando se escriben objetos completos mediante una llamada al método [**SWbemObject \_ . put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="970cd-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="970cd-114">Si modifica las propiedades o los métodos en un objeto **SWbemObject** , los cambios no se escriben en WMI hasta que llame a **SWbemObject \_ . put**.</span><span class="sxs-lookup"><span data-stu-id="970cd-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="970cd-115">Los nombres de método y propiedad genéricos definidos en esta sección terminan siempre con un carácter de subrayado final (" \_ ") para diferenciarlos de los métodos y propiedades de WMI dinámicos del objeto subyacente.</span><span class="sxs-lookup"><span data-stu-id="970cd-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="970cd-116">Tenga en cuenta que **SWbemObject** no se puede crear con el método [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx). de VBScript.</span><span class="sxs-lookup"><span data-stu-id="970cd-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="970cd-117">Si desea crear una nueva clase vacía, use [**SWbemServices. Get**](swbemservices-get.md) con un parámetro de ruta de acceso vacío.</span><span class="sxs-lookup"><span data-stu-id="970cd-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="970cd-118">Esta llamada devuelve un objeto **SWbemObject** vacío que puede convertirse en una clase.</span><span class="sxs-lookup"><span data-stu-id="970cd-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="970cd-119">Después, puede proporcionar un nombre de clase para la propiedad de [**clase**](swbemobjectpath-class.md) del objeto [**SWbemObjectPath**](swbemobjectpath.md) devuelto por la llamada de [**ruta de acceso \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="970cd-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="970cd-120">Agregue propiedades a la nueva clase mediante el [**método \_ Properties**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="970cd-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="970cd-121">Para crear una instancia, llame a **GetObject** en la nueva clase.</span><span class="sxs-lookup"><span data-stu-id="970cd-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="970cd-122">En el ejemplo de código siguiente se muestra cómo obtener una nueva clase y agregarle una propiedad.</span><span class="sxs-lookup"><span data-stu-id="970cd-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="970cd-123">El objeto **SWbemObject** que representa la clase debe volver a escribirse en el repositorio WMI mediante una llamada [**a \_ Put**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="970cd-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="970cd-124">Puede examinar el repositorio con una herramienta de visualización como [CIM Studio](further-information.md) para comprobar que aparece la nueva clase e instancia.</span><span class="sxs-lookup"><span data-stu-id="970cd-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="970cd-125">Para obtener un ejemplo de cómo quitar una clase y una instancia del repositorio, vea [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="970cd-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="970cd-126">Miembros</span><span class="sxs-lookup"><span data-stu-id="970cd-126">Members</span></span>

<span data-ttu-id="970cd-127">El objeto **SWbemObject** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="970cd-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="970cd-128">Métodos</span><span class="sxs-lookup"><span data-stu-id="970cd-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="970cd-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="970cd-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="970cd-130">Métodos</span><span class="sxs-lookup"><span data-stu-id="970cd-130">Methods</span></span>

<span data-ttu-id="970cd-131">El objeto **SWbemObject** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="970cd-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="970cd-132">Método</span><span class="sxs-lookup"><span data-stu-id="970cd-132">Method</span></span>                                                        | <span data-ttu-id="970cd-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="970cd-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="970cd-134">**Asociadores\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="970cd-135">Recupera los asociadores del objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="970cd-136">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="970cd-137">Recupera asincrónicamente los asociados del objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="970cd-138">**Clonar\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="970cd-139">Realiza una copia del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="970cd-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="970cd-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="970cd-141">Comprueba la igualdad de dos objetos.</span><span class="sxs-lookup"><span data-stu-id="970cd-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="970cd-142">**Elimínelos\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="970cd-143">Elimina el objeto de WMI.</span><span class="sxs-lookup"><span data-stu-id="970cd-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="970cd-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="970cd-145">Elimina de forma asincrónica el objeto de WMI.</span><span class="sxs-lookup"><span data-stu-id="970cd-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="970cd-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="970cd-147">Ejecuta un método exportado por un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="970cd-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="970cd-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="970cd-149">Ejecuta de forma asincrónica un método exportado por un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="970cd-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="970cd-150">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="970cd-151">Recupera la representación textual del objeto (sintaxis MOF).</span><span class="sxs-lookup"><span data-stu-id="970cd-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="970cd-152">**Instancias\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="970cd-153">Devuelve una colección de instancias del objeto (que debe ser una clase WMI).</span><span class="sxs-lookup"><span data-stu-id="970cd-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="970cd-154">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="970cd-155">Devuelve de forma asincrónica una colección de instancias del objeto (que debe ser una clase WMI).</span><span class="sxs-lookup"><span data-stu-id="970cd-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="970cd-156">**Pondrán\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="970cd-157">Crea o actualiza el objeto en WMI.</span><span class="sxs-lookup"><span data-stu-id="970cd-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="970cd-158">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="970cd-159">Crea o actualiza de forma asincrónica el objeto en WMI.</span><span class="sxs-lookup"><span data-stu-id="970cd-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="970cd-160">**Referencias\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="970cd-161">Devuelve las referencias al objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="970cd-162">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="970cd-163">Devuelve de forma asincrónica las referencias al objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="970cd-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="970cd-165">Crea una nueva clase derivada a partir del objeto actual (que debe ser una clase WMI).</span><span class="sxs-lookup"><span data-stu-id="970cd-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="970cd-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="970cd-167">Crea una nueva instancia de a partir del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="970cd-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="970cd-168">**Subclases \_**</span><span class="sxs-lookup"><span data-stu-id="970cd-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="970cd-169">Devuelve una colección de subclases del objeto (que debe ser una clase WMI).</span><span class="sxs-lookup"><span data-stu-id="970cd-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="970cd-170">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="970cd-171">Devuelve de forma asincrónica una colección de subclases del objeto (que debe ser una clase WMI).</span><span class="sxs-lookup"><span data-stu-id="970cd-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="970cd-172">Propiedades</span><span class="sxs-lookup"><span data-stu-id="970cd-172">Properties</span></span>

<span data-ttu-id="970cd-173">El objeto **SWbemObject** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="970cd-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="970cd-174">Propiedad</span><span class="sxs-lookup"><span data-stu-id="970cd-174">Property</span></span>                                                   | <span data-ttu-id="970cd-175">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="970cd-175">Access type</span></span>          | <span data-ttu-id="970cd-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="970cd-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="970cd-177">**Derivación\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="970cd-178">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-178">Read-only</span></span><br/> | <span data-ttu-id="970cd-179">Contiene una matriz de cadenas que describe la jerarquía de derivación de la clase.</span><span class="sxs-lookup"><span data-stu-id="970cd-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="970cd-180">**Métodos\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="970cd-181">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-181">Read-only</span></span><br/> | <span data-ttu-id="970cd-182">Un objeto [**SWbemMethodSet**](swbemmethodset.md) que es la colección de métodos para este objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="970cd-183">**Ruta\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="970cd-184">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-184">Read-only</span></span><br/> | <span data-ttu-id="970cd-185">Contiene un objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa la ruta de acceso del objeto de la clase o instancia actual.</span><span class="sxs-lookup"><span data-stu-id="970cd-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="970cd-186">**Propiedades\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="970cd-187">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-187">Read-only</span></span><br/> | <span data-ttu-id="970cd-188">Un objeto [**SWbemPropertySet**](swbempropertyset.md) que es la colección de propiedades de este objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="970cd-189">**Calificadores\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="970cd-190">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-190">Read-only</span></span><br/> | <span data-ttu-id="970cd-191">Un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que es la colección de calificadores para este objeto.</span><span class="sxs-lookup"><span data-stu-id="970cd-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="970cd-192">**Seguridad\_**</span><span class="sxs-lookup"><span data-stu-id="970cd-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="970cd-193">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="970cd-193">Read-only</span></span><br/> | <span data-ttu-id="970cd-194">Contiene un objeto [**SWbemSecurity**](swbemsecurity.md) que se usa para leer o cambiar la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="970cd-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="970cd-195">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="970cd-195">Examples</span></span>

<span data-ttu-id="970cd-196">La [lista de todas las propiedades y métodos de un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) ejemplo de código de VBScript de clase WMI en la galería de TechNet usa SWbemObject para enumerar todos los métodos y propiedades de una clase WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="970cd-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="970cd-197">Requisitos</span><span class="sxs-lookup"><span data-stu-id="970cd-197">Requirements</span></span>



| <span data-ttu-id="970cd-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="970cd-198">Requirement</span></span> | <span data-ttu-id="970cd-199">Value</span><span class="sxs-lookup"><span data-stu-id="970cd-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="970cd-200">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="970cd-200">Minimum supported client</span></span><br/> | <span data-ttu-id="970cd-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="970cd-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="970cd-202">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="970cd-202">Minimum supported server</span></span><br/> | <span data-ttu-id="970cd-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="970cd-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="970cd-204">Encabezado</span><span class="sxs-lookup"><span data-stu-id="970cd-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="970cd-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="970cd-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="970cd-206">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="970cd-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="970cd-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="970cd-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="970cd-208">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="970cd-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="970cd-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="970cd-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="970cd-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="970cd-210">CLSID</span></span><br/>                    | <span data-ttu-id="970cd-211">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="970cd-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="970cd-212">IID</span><span class="sxs-lookup"><span data-stu-id="970cd-212">IID</span></span><br/>                      | <span data-ttu-id="970cd-213">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="970cd-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="970cd-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="970cd-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="970cd-215">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="970cd-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="970cd-216">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="970cd-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 


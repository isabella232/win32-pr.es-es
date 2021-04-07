---
description: El objeto SWbemRefresher es un objeto contenedor que puede actualizar los datos de todos los objetos que se le han agregado. Conjunto de objetos agregados; cada elemento representado por una instancia de SWbemRefreshableItem se puede tratar como una colección y enumerarse.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objeto SWbemRefresher (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003391"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="06b34-104">Objeto SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="06b34-104">SWbemRefresher object</span></span>

<span data-ttu-id="06b34-105">El objeto **SWbemRefresher** es un objeto contenedor que puede actualizar los datos de todos los objetos que se agregan a él.</span><span class="sxs-lookup"><span data-stu-id="06b34-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="06b34-106">Las instancias únicas y los enumeradores de instancia se pueden agregar o quitar del contenedor.</span><span class="sxs-lookup"><span data-stu-id="06b34-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="06b34-107">El conjunto de objetos agregados, cada uno de los cuales se representa mediante una instancia de [**SWbemRefreshableItem**](swbemrefreshableitem.md) , se puede tratar como una colección y se pueden enumerar.</span><span class="sxs-lookup"><span data-stu-id="06b34-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="06b34-108">Las instancias de WMI de cualquier clase se pueden agregar al objeto **SWbemRefresher** .</span><span class="sxs-lookup"><span data-stu-id="06b34-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="06b34-109">Aunque el proveedor de los datos de instancia no sea un proveedor de alto rendimiento, el objeto actualizador todavía puede actualizar los datos en la llamada de [**actualización**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="06b34-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="06b34-110">Si los datos se proporcionan a través de un proveedor de alto rendimiento y la propiedad [**reconexión automática**](swbemrefresher-autoreconnect.md) es **true**, el objeto **SWbemRefresher** intenta restablecer una conexión interrumpida con el proveedor de datos.</span><span class="sxs-lookup"><span data-stu-id="06b34-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="06b34-111">Este objeto se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="06b34-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="06b34-112">La operación de actualización se puede realizar mediante una llamada al método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o al método [**SWbemObjectEx. \_ Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="06b34-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="06b34-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="06b34-113">Members</span></span>

<span data-ttu-id="06b34-114">El objeto **SWbemRefresher** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="06b34-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="06b34-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="06b34-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="06b34-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06b34-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="06b34-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="06b34-117">Methods</span></span>

<span data-ttu-id="06b34-118">El objeto **SWbemRefresher** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="06b34-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="06b34-119">Método</span><span class="sxs-lookup"><span data-stu-id="06b34-119">Method</span></span>                                        | <span data-ttu-id="06b34-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="06b34-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06b34-121">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="06b34-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="06b34-122">Agrega un nuevo objeto actualizable a la colección en el objeto actualizador.</span><span class="sxs-lookup"><span data-stu-id="06b34-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="06b34-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="06b34-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="06b34-124">Agrega un nuevo enumerador al objeto actualizador.</span><span class="sxs-lookup"><span data-stu-id="06b34-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="06b34-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="06b34-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="06b34-126">Quita todos los elementos de la colección en el objeto actualizador.</span><span class="sxs-lookup"><span data-stu-id="06b34-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="06b34-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06b34-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="06b34-128">Devuelve un elemento actualizador especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="06b34-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="06b34-129">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="06b34-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="06b34-130">Actualiza todos los elementos contenidos en el objeto actualizador.</span><span class="sxs-lookup"><span data-stu-id="06b34-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="06b34-131">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="06b34-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="06b34-132">Quita del actualizador el objeto de elemento de actualización o el conjunto de objetos con un índice especificado.</span><span class="sxs-lookup"><span data-stu-id="06b34-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="06b34-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06b34-133">Properties</span></span>

<span data-ttu-id="06b34-134">El objeto **SWbemRefresher** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="06b34-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="06b34-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06b34-135">Property</span></span>                                                         | <span data-ttu-id="06b34-136">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="06b34-136">Access type</span></span>          | <span data-ttu-id="06b34-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="06b34-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06b34-138">**Reconexión automática**</span><span class="sxs-lookup"><span data-stu-id="06b34-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="06b34-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="06b34-139">Read-only</span></span><br/> | <span data-ttu-id="06b34-140">Indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si se interrumpe la conexión.</span><span class="sxs-lookup"><span data-stu-id="06b34-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="06b34-141">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="06b34-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="06b34-142">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="06b34-142">Read-only</span></span><br/> | <span data-ttu-id="06b34-143">Contiene el número de elementos del objeto actualizador.</span><span class="sxs-lookup"><span data-stu-id="06b34-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="06b34-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06b34-144">Examples</span></span>

<span data-ttu-id="06b34-145">En el ejemplo siguiente se muestra cómo crear un objeto **SWbemRefresher** , mediante los métodos [**Add**](swbemrefresher-add.md) y [**AddEnum**](swbemrefresher-addenum.md) para almacenar una instancia única y una instancia de enumeración, la actualización de los datos y el uso de la propiedad Item para obtener los objetos [**SWbemRefreshableItem**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="06b34-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="06b34-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06b34-146">Requirements</span></span>



| <span data-ttu-id="06b34-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b34-147">Requirement</span></span> | <span data-ttu-id="06b34-148">Value</span><span class="sxs-lookup"><span data-stu-id="06b34-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06b34-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06b34-149">Minimum supported client</span></span><br/> | <span data-ttu-id="06b34-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06b34-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06b34-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06b34-151">Minimum supported server</span></span><br/> | <span data-ttu-id="06b34-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06b34-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06b34-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06b34-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="06b34-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="06b34-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="06b34-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="06b34-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06b34-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06b34-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06b34-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06b34-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="06b34-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="06b34-159">CLSID</span></span><br/>                    | <span data-ttu-id="06b34-160">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="06b34-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="06b34-161">IID</span><span class="sxs-lookup"><span data-stu-id="06b34-161">IID</span></span><br/>                      | <span data-ttu-id="06b34-162">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="06b34-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="06b34-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="06b34-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b34-164">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="06b34-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="06b34-165">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="06b34-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="06b34-166">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="06b34-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





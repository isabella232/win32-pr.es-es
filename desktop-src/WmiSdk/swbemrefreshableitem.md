---
description: Representa un único elemento en un objeto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objeto SWbemRefreshableItem (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820239"
---
# <a name="swbemrefreshableitem-object"></a><span data-ttu-id="794f8-103">Objeto SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="794f8-103">SWbemRefreshableItem object</span></span>

<span data-ttu-id="794f8-104">El objeto **SWbemRefreshableItem** representa un único elemento en un objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="794f8-104">The **SWbemRefreshableItem** object represents a single item in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="794f8-105">Un objeto **SWbemRefreshableItem** se obtiene a través de los métodos [**Add**](swbemrefresher-add.md) y [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="794f8-105">An **SWbemRefreshableItem** object is obtained through the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods of [**SWbemRefresher**](swbemrefresher.md).</span></span> <span data-ttu-id="794f8-106">Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="794f8-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="794f8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="794f8-107">Members</span></span>

<span data-ttu-id="794f8-108">El objeto **SWbemRefreshableItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="794f8-108">The **SWbemRefreshableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="794f8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="794f8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="794f8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="794f8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="794f8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="794f8-111">Methods</span></span>

<span data-ttu-id="794f8-112">El objeto **SWbemRefreshableItem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="794f8-112">The **SWbemRefreshableItem** object has these methods.</span></span>



| <span data-ttu-id="794f8-113">Método</span><span class="sxs-lookup"><span data-stu-id="794f8-113">Method</span></span>                                        | <span data-ttu-id="794f8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="794f8-114">Description</span></span>                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="794f8-115">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="794f8-115">**Remove**</span></span>](swbemrefreshableitem-remove.md) | <span data-ttu-id="794f8-116">Quita el objeto **SWbemRefreshableItem** del objeto [**SWbemRefresher**](swbemrefresher.md) primario.</span><span class="sxs-lookup"><span data-stu-id="794f8-116">Removes the **SWbemRefreshableItem** object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="794f8-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="794f8-117">Properties</span></span>

<span data-ttu-id="794f8-118">El objeto **SWbemRefreshableItem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="794f8-118">The **SWbemRefreshableItem** object has these properties.</span></span>



| <span data-ttu-id="794f8-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="794f8-119">Property</span></span>                                                       | <span data-ttu-id="794f8-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="794f8-120">Access type</span></span>           | <span data-ttu-id="794f8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="794f8-121">Description</span></span>                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="794f8-122">**Ajustar**</span><span class="sxs-lookup"><span data-stu-id="794f8-122">**Index**</span></span>](swbemrefreshableitem-index.md)<br/>         | <span data-ttu-id="794f8-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="794f8-123">Read/write</span></span><br/> | <span data-ttu-id="794f8-124">Índice del elemento en su objeto primario [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="794f8-124">Index of the item in its parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/>                                          |
| [<span data-ttu-id="794f8-125">**IsSet**</span><span class="sxs-lookup"><span data-stu-id="794f8-125">**IsSet**</span></span>](swbemrefreshableitem-isset.md)<br/>         | <span data-ttu-id="794f8-126">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="794f8-126">Read/write</span></span><br/> | <span data-ttu-id="794f8-127">Indica si el objeto **SWbemRefreshableItem** representa un único objeto o un conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="794f8-127">Indicates whether the **SWbemRefreshableItem** object represents a single object or an object set.</span></span><br/>                        |
| [<span data-ttu-id="794f8-128">**Object**</span><span class="sxs-lookup"><span data-stu-id="794f8-128">**Object**</span></span>](swbemrefreshableitem-object.md)<br/>       | <span data-ttu-id="794f8-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="794f8-129">Read/write</span></span><br/> | <span data-ttu-id="794f8-130">Representa un objeto [**SWbemObject**](swbemobject.md) único que se actualiza.</span><span class="sxs-lookup"><span data-stu-id="794f8-130">Represents a single [**SWbemObject**](swbemobject.md) object that is refreshed.</span></span><br/>                                          |
| [<span data-ttu-id="794f8-131">**ObjectSet**</span><span class="sxs-lookup"><span data-stu-id="794f8-131">**ObjectSet**</span></span>](swbemrefreshableitem-objectset.md)<br/> | <span data-ttu-id="794f8-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="794f8-132">Read/write</span></span><br/> | <span data-ttu-id="794f8-133">Representa el conjunto de objetos que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="794f8-133">Represents the object set to be refreshed.</span></span><br/>                                                                                |
| [<span data-ttu-id="794f8-134">**Actualizador**</span><span class="sxs-lookup"><span data-stu-id="794f8-134">**Refresher**</span></span>](swbemrefreshableitem-refresher.md)<br/> | <span data-ttu-id="794f8-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="794f8-135">Read-only</span></span><br/>  | <span data-ttu-id="794f8-136">Representa el objeto [**SWbemRefresher**](swbemrefresher.md) primario que contiene el objeto **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="794f8-136">Represents the parent [**SWbemRefresher**](swbemrefresher.md) object which contains the **SWbemRefreshableItem** object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="794f8-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="794f8-137">Remarks</span></span>

<span data-ttu-id="794f8-138">El método [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript no se puede usar para crear objetos **SWbemRefreshableItem** directamente.</span><span class="sxs-lookup"><span data-stu-id="794f8-138">The VBScript method [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) cannot be used to create **SWbemRefreshableItem** objects directly.</span></span>

## <a name="examples"></a><span data-ttu-id="794f8-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="794f8-139">Examples</span></span>

<span data-ttu-id="794f8-140">El siguiente script muestra la creación de un objeto [**SWbemRefresher**](swbemrefresher.md) y la adición de un solo objeto y un enumerador **SWbemRefreshableItem** a él.</span><span class="sxs-lookup"><span data-stu-id="794f8-140">The following script illustrates the creation of an [**SWbemRefresher**](swbemrefresher.md) object and the addition of single object and enumerator **SWbemRefreshableItem** to it.</span></span>


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a><span data-ttu-id="794f8-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="794f8-141">Requirements</span></span>



| <span data-ttu-id="794f8-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="794f8-142">Requirement</span></span> | <span data-ttu-id="794f8-143">Value</span><span class="sxs-lookup"><span data-stu-id="794f8-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="794f8-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="794f8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="794f8-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="794f8-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="794f8-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="794f8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="794f8-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="794f8-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="794f8-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="794f8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="794f8-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="794f8-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="794f8-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="794f8-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="794f8-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="794f8-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="794f8-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="794f8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="794f8-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="794f8-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="794f8-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="794f8-154">CLSID</span></span><br/>                    | <span data-ttu-id="794f8-155">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="794f8-155">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="794f8-156">IID</span><span class="sxs-lookup"><span data-stu-id="794f8-156">IID</span></span><br/>                      | <span data-ttu-id="794f8-157">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="794f8-157">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="794f8-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="794f8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794f8-159">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="794f8-159">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 





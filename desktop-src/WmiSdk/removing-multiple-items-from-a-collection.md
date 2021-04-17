---
description: Si intenta quitar más de un elemento de una colección, es posible que no se quiten algunos elementos.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Quitar varios elementos de una colección WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717047"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a><span data-ttu-id="15686-103">Quitar varios elementos de una colección WMI</span><span class="sxs-lookup"><span data-stu-id="15686-103">Removing Multiple Items from a WMI Collection</span></span>

<span data-ttu-id="15686-104">Si intenta quitar más de un elemento de una colección, es posible que no se quiten algunos elementos.</span><span class="sxs-lookup"><span data-stu-id="15686-104">If you attempt to remove more than one item in a collection, you may find that some items are not removed.</span></span> <span data-ttu-id="15686-105">No se puede recorrer en iteración una colección mientras se quitan elementos, porque cuando se quita un elemento de una colección, el puntero de la colección se mueve al siguiente elemento.</span><span class="sxs-lookup"><span data-stu-id="15686-105">You cannot iterate a collection while removing items, because when you remove an element from a collection, the collection pointer is moved on to the next element.</span></span> <span data-ttu-id="15686-106">Por ejemplo, un intento de quitar todos los elementos de una colección produce la eliminación de todos los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="15686-106">For example, an attempt to remove all of the items from a collection results in the removal of every other item.</span></span> <span data-ttu-id="15686-107">Es posible que vea este problema al quitar elementos con los métodos [**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md) o [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="15686-107">You may see this problem when you are removing items with the [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) or [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) methods.</span></span> <span data-ttu-id="15686-108">Puede evitar este problema si recorre en bucle la colección y coloca los nombres de los elementos que se van a quitar en una matriz.</span><span class="sxs-lookup"><span data-stu-id="15686-108">You can avoid this problem by looping through the collection and putting the names of the items to remove in an array.</span></span> <span data-ttu-id="15686-109">A continuación, puede recorrer la matriz y eliminar los elementos mencionados en la matriz.</span><span class="sxs-lookup"><span data-stu-id="15686-109">You then can loop through the array and delete the items named in the array.</span></span> <span data-ttu-id="15686-110">Las colecciones, como [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)y [**SWbemRefresher**](swbemrefresher.md), también tienen un método que elimina todos los elementos del contenedor del actualizador.</span><span class="sxs-lookup"><span data-stu-id="15686-110">The collections, such as [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md), and [**SWbemRefresher**](swbemrefresher.md), also have a method that deletes all items in the refresher container.</span></span>

<span data-ttu-id="15686-111">En el siguiente script se muestra cómo quitar varios elementos de una colección.</span><span class="sxs-lookup"><span data-stu-id="15686-111">The following script illustrates how to remove several items from a collection.</span></span>


```VB
Const WBEM_CIMTYPE_STRING = 8    ' Value for string data type
Dim names()
Redim names (0)
set objSWbemService = GetObject("winmgmts:root\default")
set objClass = ObjSWbemService.Get()

Wscript.Echo "Creating class NewClass"
objClass.Path_.Class = "NewClass"
For i = 1 to 5
    objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
Next
objClass.Put_
Getprops()

' Get all the property names in an array
For Each oprop in objClass.properties_
    Redim Preserve names(Ubound(names)+1)
    names(Ubound(names)-1) = oprop.name
Next
Wscript.Echo "Remove first 3 properties using array of names:"

For i = Lbound(names) to Ubound(names)-1
    If (i < 3) Then
       Wscript.Echo "Removing " & names(i)
       objClass.Properties_.Remove names(i)
    End If
Next

objClass.Put_
Wscript.Echo "Result:"
Getprops()

Sub Getprops()
    Wscript.Echo "Number of properties = " _
        & objClass.Properties_.Count
    For Each oprop in objClass.Properties_
        Wscript.Echo oprop.name
    Next
End Sub
```



No se pueden quitar propiedades y calificadores en una instancia de clase o en una clase derivada que tenga propiedades heredadas. Dicho intento de eliminación genera un error y no se quita la propiedad o el calificador; en su lugar, WMI restablece el valor predeterminado de la propiedad o el calificador. <span data-ttu-id="15686-114">En el caso de una clase derivada con propiedades heredadas, WMI restablece la propiedad heredada en el valor predeterminado de la propiedad en la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="15686-114">In the case of a derived class with inherited properties, WMI resets the inherited property to the default value of the property in the parent class.</span></span>

<span data-ttu-id="15686-115">Para obtener más información, vea [manipular información de clase e instancia](manipulating-class-and-instance-information.md), [obtener acceso a una colección](accessing-a-collection.md)y [quitar un solo elemento de una colección](removing-a-single-item-from-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="15686-115">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Accessing a Collection](accessing-a-collection.md), and [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).</span></span>

 

 




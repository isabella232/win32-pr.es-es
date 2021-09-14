---
description: Si intenta quitar más de un elemento de una colección, es posible que no se quiten algunos elementos.
ms.assetid: 7c82321e-059f-497c-8561-33c3e9306d41
ms.tgt_platform: multiple
title: Quitar varios elementos de una colección WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c44203f3279163a1de595cac8a00270dccd31c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973733"
---
# <a name="removing-multiple-items-from-a-wmi-collection"></a>Quitar varios elementos de una colección WMI

Si intenta quitar más de un elemento de una colección, es posible que no se quiten algunos elementos. No se puede iterar una colección al quitar elementos, porque cuando se quita un elemento de una colección, el puntero de colección se mueve al elemento siguiente. Por ejemplo, un intento de quitar todos los elementos de una colección da como resultado la eliminación de todos los demás elementos. Es posible que vea este problema al quitar elementos con los métodos [**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md) o [**SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Puede evitar este problema si recorre en bucle la colección y coloca los nombres de los elementos que se quitarán en una matriz. A continuación, puede recorrer en bucle la matriz y eliminar los elementos denominados en la matriz. Las colecciones, como [**SWbemNamedValueSet**](swbemnamedvalueset.md), [**SWbemPrivilegeSet**](swbemprivilegeset.md)y [**SWbemRefresher**](swbemrefresher.md), también tienen un método que elimina todos los elementos del contenedor del actualizador.

El siguiente script muestra cómo quitar varios elementos de una colección.


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



No se pueden quitar propiedades y calificadores en una instancia de clase o clase derivada que tenga propiedades heredadas. Este intento de eliminación genera un error y no se quita la propiedad o calificador; en su lugar, WMI restablece la propiedad o calificador al valor predeterminado. En el caso de una clase derivada con propiedades heredadas, WMI restablece la propiedad heredada al valor predeterminado de la propiedad de la clase primaria.

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), Accessing a [Collection](accessing-a-collection.md)y [Removing a Single Item from a Collection](removing-a-single-item-from-a-collection.md).

 

 




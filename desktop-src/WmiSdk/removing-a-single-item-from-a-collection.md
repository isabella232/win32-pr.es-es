---
description: Uno de los propósitos principales de acceder a una colección es quitar un elemento de la colección. Puede quitar un elemento de una colección con una llamada al método SWbemPropertySet.Remove. Este método no está disponible para SWbemObjectSet o SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Quitar un único elemento de una colección WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dabeb3ff2e7e70cf6fe25f1ddfb0b14032119d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973734"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Quitar un único elemento de una colección WMI

Uno de los propósitos principales de acceder a una colección es quitar un elemento de la colección. Puede quitar un elemento de una colección con una llamada al [**método SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Este método no está disponible para [**SWbemObjectSet**](swbemobjectset.md) o [**SWbemMethodSet**](swbemmethodset.md).

Los elementos se quitan por nombre de [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet y**](swbemqualifierset.md) [**SWbemNamedValueSet**](swbemnamedvalueset.md). Sin embargo, los elementos [**de SWbemRefresher**](swbemrefresher.md) se quitan por índice y de [**SWbemPrivilegeSet**](swbemprivilegeset.md) mediante la constante que representa el nombre de privilegio.

**Para quitar un elemento de una colección**

-   En el ejemplo de código siguiente se muestra cómo quitar el elemento con una llamada al [**método SWbemPropertySet.Remove.**](swbempropertyset-remove.md)

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    En el ejemplo siguiente se crea una nueva clase denominada "NewClass" en el espacio de nombres predeterminado raíz y \\ se le agregan tres propiedades. A continuación, el script usa el código del ejemplo anterior para eliminar la segunda propiedad.

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

Para obtener más información, vea [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), Accessing a [Collection](accessing-a-collection.md)y [Removing Multiple Items from a Collection](removing-multiple-items-from-a-collection.md).

 

 




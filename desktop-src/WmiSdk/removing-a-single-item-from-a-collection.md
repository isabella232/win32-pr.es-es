---
description: Uno de los propósitos principales de acceder a una colección es quitar un elemento de la colección. Puede quitar un elemento de una colección con una llamada al método SWbemPropertySet.Remove. Este método no está disponible para SWbemObjectSet o SWbemMethodSet.
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: Quitar un único elemento de una colección WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50364173aff9f28362878e84d5f3ddb496e430521dc5b1bb92bbc11e7e6b528c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995905"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>Quitar un único elemento de una colección WMI

Uno de los propósitos principales de acceder a una colección es quitar un elemento de la colección. Puede quitar un elemento de una colección con una llamada al [**método SWbemPropertySet.Remove.**](swbempropertyset-remove.md) Este método no está disponible para [**SWbemObjectSet**](swbemobjectset.md) o [**SWbemMethodSet**](swbemmethodset.md).

Los elementos se quitan por nombre de [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)y [**SWbemNamedValueSet**](swbemnamedvalueset.md). Sin embargo, los [**elementos de SWbemRefresher**](swbemrefresher.md) se quitan por índice y de [**SWbemPrivilegeSet**](swbemprivilegeset.md) por la constante que representa el nombre de privilegio.

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

 

 




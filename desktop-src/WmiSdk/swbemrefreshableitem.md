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
# <a name="swbemrefreshableitem-object"></a>Objeto SWbemRefreshableItem

El objeto **SWbemRefreshableItem** representa un único elemento en un objeto [**SWbemRefresher**](swbemrefresher.md) . Un objeto **SWbemRefreshableItem** se obtiene a través de los métodos [**Add**](swbemrefresher-add.md) y [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md). Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemRefreshableItem** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemRefreshableItem** tiene estos métodos.



| Método                                        | Descripción                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Retirar**](swbemrefreshableitem-remove.md) | Quita el objeto **SWbemRefreshableItem** del objeto [**SWbemRefresher**](swbemrefresher.md) primario.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemRefreshableItem** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Ajustar**](swbemrefreshableitem-index.md)<br/>         | Lectura/escritura<br/> | Índice del elemento en su objeto primario [**SWbemRefresher**](swbemrefresher.md) .<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | Lectura/escritura<br/> | Indica si el objeto **SWbemRefreshableItem** representa un único objeto o un conjunto de objetos.<br/>                        |
| [**Object**](swbemrefreshableitem-object.md)<br/>       | Lectura/escritura<br/> | Representa un objeto [**SWbemObject**](swbemobject.md) único que se actualiza.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Lectura/escritura<br/> | Representa el conjunto de objetos que se va a actualizar.<br/>                                                                                |
| [**Actualizador**](swbemrefreshableitem-refresher.md)<br/> | Solo lectura<br/>  | Representa el objeto [**SWbemRefresher**](swbemrefresher.md) primario que contiene el objeto **SWbemRefreshableItem** .<br/> |



 

## <a name="remarks"></a>Observaciones

El método [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript no se puede usar para crear objetos **SWbemRefreshableItem** directamente.

## <a name="examples"></a>Ejemplos

El siguiente script muestra la creación de un objeto [**SWbemRefresher**](swbemrefresher.md) y la adición de un solo objeto y un enumerador **SWbemRefreshableItem** a él.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | \_ISWBEMREFRESHABLEITEM IID<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> </dl>

 

 





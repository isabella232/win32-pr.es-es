---
description: Representa un único elemento de un objeto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objeto SWbemRefreshableItem (Wbemdisp.h)
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
ms.openlocfilehash: ed47d78a133269231d9e43cde3d104a3b0ba95e59240862a5d787d1651cc9de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921866"
---
# <a name="swbemrefreshableitem-object"></a>Objeto SWbemRefreshableItem

El **objeto SWbemRefreshableItem** representa un único elemento en un [**objeto SWbemRefresher.**](swbemrefresher.md) Un **objeto SWbemRefreshableItem** se obtiene a través de los métodos [**Add**](swbemrefresher-add.md) y [**AddEnum**](swbemrefresher-addenum.md) [**de SWbemRefresher**](swbemrefresher.md). La llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript no puede crear este objeto.

## <a name="members"></a>Miembros

El **objeto SWbemRefreshableItem** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemRefreshableItem** tiene estos métodos.



| Método                                        | Descripción                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Quitar**](swbemrefreshableitem-remove.md) | Quita el **objeto SWbemRefreshableItem** del objeto [**SWbemRefresher**](swbemrefresher.md) primario.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemRefreshableItem** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Índice**](swbemrefreshableitem-index.md)<br/>         | Lectura/escritura<br/> | Índice del elemento en su objeto [**SWbemRefresher**](swbemrefresher.md) primario.<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | Lectura/escritura<br/> | Indica si el **objeto SWbemRefreshableItem** representa un único objeto o un conjunto de objetos.<br/>                        |
| [**Objeto**](swbemrefreshableitem-object.md)<br/>       | Lectura/escritura<br/> | Representa un único [**objeto SWbemObject**](swbemobject.md) que se actualiza.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Lectura/escritura<br/> | Representa el conjunto de objetos que se va a actualizar.<br/>                                                                                |
| [**Actualización**](swbemrefreshableitem-refresher.md)<br/> | Solo lectura<br/>  | Representa el objeto [**SWbemRefresher**](swbemrefresher.md) primario que contiene el **objeto SWbemRefreshableItem.**<br/> |



 

## <a name="remarks"></a>Comentarios

El método [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) de VBScript no se puede usar para crear **objetos SWbemRefreshableItem** directamente.

## <a name="examples"></a>Ejemplos

El siguiente script muestra la creación de un objeto [**SWbemRefresher**](swbemrefresher.md) y la adición de un único objeto y enumerador **SWbemRefreshableItem** a él.


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
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 





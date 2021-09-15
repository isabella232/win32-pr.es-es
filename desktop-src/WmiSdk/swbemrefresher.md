---
description: El objeto SWbemRefresher es un objeto contenedor que puede actualizar los datos de todos los objetos agregados a él. El conjunto de objetos agregados, cada elemento representado por una instancia de SWbemRefreshableItem se puede tratar como una colección y enumerarse.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objeto SWbemRefresher (Wbemdisp.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465492"
---
# <a name="swbemrefresher-object"></a>Objeto SWbemRefresher

El **objeto SWbemRefresher** es un objeto contenedor que puede actualizar los datos de todos los objetos que se le agregan. Las instancias únicas y los enumeradores de instancia se pueden agregar o quitar del contenedor. El conjunto de objetos agregados, cada elemento representado por una instancia [**de SWbemRefreshableItem,**](swbemrefreshableitem.md) se puede tratar como una colección y enumerarse. Las instancias wmi de cualquier clase se pueden agregar al **objeto SWbemRefresher.** Incluso si el proveedor para los datos de instancia no es un proveedor de alto rendimiento, el objeto de actualizador todavía puede actualizar los datos en la [**llamada de**](swbemrefresher-refresh.md) actualización. Si los datos se proporcionan a través de un proveedor de alto rendimiento y la propiedad [**AutoReconnect**](swbemrefresher-autoreconnect.md) es **TRUE,** el objeto **SWbemRefresher** intenta restablecer una conexión rota con el proveedor de datos. Este objeto se puede crear mediante la llamada **CreateObject de** VBScript.

La operación de actualización se puede llevar a cabo llamando al método [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) o al [**método SWbemObjectEx.Refresh. \_**](swbemobjectex-refresh-.md)

## <a name="members"></a>Members

El **objeto SWbemRefresher** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemRefresher** tiene estos métodos.



| Método                                        | Descripción                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Añadir**](swbemrefresher-add.md)             | Agrega un nuevo objeto actualizable a la colección en el objeto de actualizador.<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | Agrega un nuevo enumerador al objeto de actualizador.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Quita todos los elementos de la colección en el objeto de actualizador.<br/>                             |
| [**Elemento**](swbemrefresher-item.md)           | Devuelve un elemento de actualizador especificado de la colección.<br/>                                    |
| [**Actualizar**](swbemrefresher-refresh.md)     | Actualiza todos los elementos contenidos en el objeto de actualizador.<br/>                          |
| [**Remove**](swbemrefresher-remove.md)       | Quita del actualizador el objeto de elemento de actualización o el conjunto de objetos con un índice especificado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemRefresher** tiene estas propiedades.



| Propiedad                                                         | Tipo de acceso          | Descripción                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Conexión automática**](swbemrefresher-autoreconnect.md)<br/> | Solo lectura<br/> | Indica si el actualizador se vuelve a conectar automáticamente a un proveedor remoto si se ha roto la conexión.<br/> |
| [**Contar**](swbemrefresher-count.md)<br/>                 | Solo lectura<br/> | Contiene el número de elementos del objeto de actualización.<br/>                                                      |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la creación de un objeto **SWbemRefresher,** el uso de los métodos [**Add**](swbemrefresher-add.md) y [**AddEnum**](swbemrefresher-addenum.md) para almacenar una instancia única y una instancia de enumeración, la actualización de los datos y el uso de la propiedad Item para obtener los objetos [**SWbemRefreshableItem.**](swbemrefreshableitem.md)


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> </dl>

 

 





---
title: MediaCollection. Remove (método)
description: El método Remove quita un elemento de la colección de medios.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- quitar Media Player de Windows de método
- método Remove Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, Remove (método)
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690293"
---
# <a name="mediacollectionremove-method"></a>MediaCollection. Remove (método)

El método **Remove** quita un elemento de la colección de medios.

## <a name="syntax"></a>Sintaxis


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se va a quitar.

</dd> <dt>

*eliminar* \[ de\]
</dt> <dd>

**Valor booleano** que indica si se va a quitar el elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método elimina un elemento de la biblioteca. Este método no elimina archivos del equipo del usuario.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript, después de solicitar al usuario, se elimina de forma permanente el primer elemento multimedia de la colección de medios mediante *MediaCollection*. **quitar**. El objeto **Player** se creó con ID = "Player".


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection. Add**](mediacollection-add.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






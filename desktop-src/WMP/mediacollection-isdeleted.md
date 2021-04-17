---
title: MediaCollection. isDeleted (método)
description: El método isDeleted recupera un valor que indica si el elemento multimedia especificado se encuentra en la carpeta elementos eliminados.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690294"
---
# <a name="mediacollectionisdeleted-method"></a>MediaCollection. isDeleted (método)

El método **IsDeleted** recupera un valor que indica si el elemento multimedia especificado se encuentra en la carpeta elementos eliminados.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se puede eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método siempre devuelve **false**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **IsDeleted** para probar si un elemento multimedia determinado, almacenado en la variable denominada mediaObject, se encuentra en la carpeta elementos eliminados. Si el elemento multimedia no se ha eliminado ya, se mueve a la carpeta elementos eliminados. El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0, Windows Media Player versión 7,1 o Windows Media Player para Windows XP. Este método no es compatible con Windows Media Player 9 series o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.setDeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






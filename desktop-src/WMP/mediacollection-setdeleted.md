---
title: MediaCollection. setDeleted, método
description: El método setDeleted mueve el elemento multimedia especificado a la carpeta elementos eliminados. | MediaCollection. setDeleted, método
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- método setDeleted de Windows Media Player
- método setDeleted de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método setDeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690292"
---
# <a name="mediacollectionsetdeleted-method"></a>MediaCollection. setDeleted, método

El método **setDeleted** mueve el elemento multimedia especificado a la carpeta elementos eliminados.

## <a name="syntax"></a>Sintaxis


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se está moviendo.

</dd> <dt>

*true* \[ de\]
</dt> <dd>

Especifique siempre este valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método no quita los archivos del equipo del usuario.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **setDeleted** para trasladar un elemento multimedia determinado, almacenado en la variable denominada mediaObject, a la carpeta elementos eliminados. *MediaCollection*. el método **IsDeleted** primero comprueba si el elemento ya se ha eliminado. El objeto **Player** se creó con ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

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

[**MediaCollection. isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






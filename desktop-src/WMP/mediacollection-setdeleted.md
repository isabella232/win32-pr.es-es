---
title: Método MediaCollection.setDeleted
description: El método setDeleted mueve el elemento multimedia especificado a la carpeta de elementos eliminados. | Método MediaCollection.setDeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Método setDeleted Reproductor de Windows Media
- Método setDeleted Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media método , setDeleted
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
ms.openlocfilehash: 63dcb4c0062acbd5f457cd09b9c1370ff9c4f7683fd8758a4a64ce5f510a6948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647845"
---
# <a name="mediacollectionsetdeleted-method"></a>Método MediaCollection.setDeleted

El **método setDeleted** mueve el elemento multimedia especificado a la carpeta de elementos eliminados.

## <a name="syntax"></a>Sintaxis


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*item* \[ En\]
</dt> <dd>

**Objeto multimedia** que se va a mover.

</dd> <dt>

*true* \[ En\]
</dt> <dd>

Especifique siempre este valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método no quita archivos del equipo del usuario.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **setDeleted para** mover un elemento multimedia determinado, almacenado en la variable denominada mediaObject, a la carpeta de elementos eliminados. *MediaCollection*. **El método isDeleted** comprueba primero si el elemento ya se ha eliminado. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0, Reproductor de Windows Media versión 7.1 o Reproductor de Windows Media para Windows XP. Este método no se admite para Reproductor de Windows Media serie 9 o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






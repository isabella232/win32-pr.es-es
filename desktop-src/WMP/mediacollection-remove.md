---
title: Método MediaCollection.remove
description: El método remove quita un elemento de la colección de medios.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- remove method Reproductor de Windows Media
- remove method Reproductor de Windows Media , Clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media , método remove
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
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574612"
---
# <a name="mediacollectionremove-method"></a>Método MediaCollection.remove

El **método remove** quita un elemento de la colección de medios.

## <a name="syntax"></a>Sintaxis


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*item* \[ En\]
</dt> <dd>

**Objeto** multimedia que se va a quitar.

</dd> <dt>

*delete* \[ En\]
</dt> <dd>

**Valor** booleano que indica si se va a quitar el elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método elimina un elemento de la biblioteca. Este método no elimina archivos del equipo del usuario.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el JScript ejemplo siguiente, después de preguntar al usuario, elimina permanentemente el primer elemento multimedia de la colección de medios mediante *MediaCollection*. **quite**. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






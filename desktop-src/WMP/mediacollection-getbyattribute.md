---
title: MediaCollection. getByAttribute, método
description: El método getByAttribute recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- método getByAttribute de Windows Media Player
- método getByAttribute de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690636"
---
# <a name="mediacollectiongetbyattribute-method"></a>MediaCollection. getByAttribute, método

El método **getByAttribute** recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ de de\]
</dt> <dd>

**Cadena** que indica el nombre del atributo que se va a buscar. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

**Cadena** que indica el valor que debe tener el atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Este método se puede utilizar para crear una consulta genérica para los elementos multimedia que coinciden con un valor para un atributo de la base de datos. Esto es útil en el caso de los atributos definidos por el usuario. Si el atributo no existe, se producirá un error.

Puede utilizar este método para recuperar todos los elementos multimedia de un tipo específico. Use el nombre de atributo "MediaType" y uno de los siguientes valores:



| Value    | Descripción                                                |
|----------|------------------------------------------------------------|
| audio    | Música y otros elementos de solo audio.                          |
| automáticas | Listas de reproducción representadas como objetos **multimedia** .                |
| radio    | Elementos de la estación de radio. No lo usa Windows Media Player 10.  |
| video    | Elementos de vídeo.                                               |
| álbum    | Elementos de fotografía. Requiere Windows Media Player 10.             |
| Otros    | Otros elementos, como archivos ASF o direcciones URL, a medios de streaming. |



 

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByAttribute** para reproducir todo el contenido de la biblioteca por el intérprete llamado Triode 48. El objeto **Player** se creó con ID = "Player".


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






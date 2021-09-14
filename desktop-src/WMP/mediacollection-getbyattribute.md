---
title: Método MediaCollection.getByAttribute
description: El método getByAttribute recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- Método getByAttribute Reproductor de Windows Media
- Método getByAttribute Reproductor de Windows Media , clase MediaCollection
- Clase MediaCollection Reproductor de Windows Media , método getByAttribute
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068373"
---
# <a name="mediacollectiongetbyattribute-method"></a>Método MediaCollection.getByAttribute

El **método getByAttribute** recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*atributo* \[ En\]
</dt> <dd>

**Cadena** que indica el nombre del atributo que se buscará. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*value* \[ En\]
</dt> <dd>

**Cadena** que indica el valor que debe tener el atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Observaciones

Este método se puede usar para crear una consulta genérica para elementos multimedia que coincidan con un valor para un atributo de la base de datos. Esto es útil en el caso de los atributos definidos por el usuario. Si el atributo no existe, se producirá un error.

Puede usar este método para recuperar todos los elementos multimedia de un tipo específico. Use el nombre de atributo "MediaType" y uno de los valores siguientes:



| Value    | Descripción                                                |
|----------|------------------------------------------------------------|
| audio    | Música y otros elementos de solo audio.                          |
| Reproducción | Listas de reproducción representadas como **objetos** Multimedia.                |
| radio    | Elementos de estación de radio. No lo usa Reproductor de Windows Media 10.  |
| video    | Elementos de vídeo.                                               |
| Foto    | Elementos de foto. Requiere Reproductor de Windows Media 10.             |
| otro    | Otros elementos, como archivos ASF o direcciones URL a medios de streaming. |



 

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa MediaCollection*. **getByAttribute para** reproducir todo el contenido de la biblioteca por el intérprete llamado Alde 48. El **objeto Player** se creó con id. = "Player".


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
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






---
title: Método Playlist.setItemInfo
description: El método setItemInfo especifica el valor de un atributo de lista de reproducción.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Método setItemInfo Reproductor de Windows Media
- Método setItemInfo Reproductor de Windows Media , clase Playlist
- Clase Playlist Reproductor de Windows Media método , setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47208d1fad03a57e26d1f5591adf658c7553a9087254b49c7aecfd904bd4d95f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335752"
---
# <a name="playlistsetiteminfo-method"></a>Método Playlist.setItemInfo

El **método setItemInfo** especifica el valor de un atributo de lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo que se va a establecer. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo .](attribute-reference.md)

</dd> <dt>

*value* \[ En\]
</dt> <dd>

**Cadena** que contiene el nuevo valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un uso especial del **método setItemInfo** consiste en ordenar los elementos de la lista de reproducción mediante el atributo SortAttribute. En el JScript siguiente se ordena una lista de reproducción por los valores del atributo UserLastPlayedTime. La lista de reproducción variable es una referencia a un objeto **Playlist.**


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

Vea la [propiedad attributeCount](playlist-attributecount.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






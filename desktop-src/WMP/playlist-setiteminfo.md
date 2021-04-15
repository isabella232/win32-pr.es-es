---
title: Método playlist. setItemInfo
description: El método setItemInfo especifica el valor de un atributo de lista de reproducción.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método setItemInfo
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
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709264"
---
# <a name="playlistsetiteminfo-method"></a>Método playlist. setItemInfo

El método **setItemInfo** especifica el valor de un atributo de lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo que se va a establecer. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> <dt>

*valor* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nuevo valor para el atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un uso especial del método **setItemInfo** es ordenar los elementos de la lista de reproducción mediante el atributo SortAttribute. En el siguiente ejemplo de JScript se ordena una lista de reproducción por los valores del atributo UserLastPlayedTime. La lista de reproducción de variables es una referencia a un objeto de **lista de reproducción** .


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

Vea la propiedad [attributeCount](playlist-attributecount.md) para ver el código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reproducción. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






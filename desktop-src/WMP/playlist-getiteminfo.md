---
title: Método playlist. getItemInfo
description: El método getItemInfo recupera el valor de un atributo de lista de reproducción.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649515"
---
# <a name="playlistgetiteminfo-method"></a>Método playlist. getItemInfo

El método **getItemInfo** recupera el valor de un atributo de lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo que se va a recuperar. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

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

[**Lista de reproducción. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






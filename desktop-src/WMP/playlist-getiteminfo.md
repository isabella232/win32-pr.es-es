---
title: Método Playlist.getItemInfo
description: El método getItemInfo recupera el valor de un atributo de lista de reproducción.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media , método getItemInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243189"
---
# <a name="playlistgetiteminfo-method"></a>Método Playlist.getItemInfo

El **método getItemInfo** recupera el valor de un atributo de lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* \[ En\]
</dt> <dd>

**Cadena** que contiene el nombre del atributo que se va a recuperar. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

Vea la [propiedad attributeCount](playlist-attributecount.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






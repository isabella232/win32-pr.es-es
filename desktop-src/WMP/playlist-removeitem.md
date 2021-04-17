---
title: Playlist. removeItem (método)
description: El método removeItem quita el elemento especificado de la lista de reproducción.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- método removeItem Media Player Windows
- método removeItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- Playlist.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de03333e2373744f9e9197be8ed8582997c557d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708808"
---
# <a name="playlistremoveitem-method"></a>Playlist. removeItem (método)

El método **RemoveItem** quita el elemento especificado de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el elemento que se quita es la pista actual (*jugador*.**currentMedia**), se detiene la reproducción y el siguiente elemento de la lista de reproducción se convierte en el actual. Si no hay ningún elemento siguiente, se usa el elemento anterior o si no hay otros elementos y, a continuación, el *jugador*. **currentMedia** se establece en **null**.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reproducción. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






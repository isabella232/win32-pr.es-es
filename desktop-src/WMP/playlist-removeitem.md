---
title: Método Playlist.removeItem
description: El método removeItem quita el elemento especificado de la lista de reproducción.
ms.assetid: 294ba4fb-967b-4a03-b0c5-6e9c15db3bff
keywords:
- Método removeItem Reproductor de Windows Media
- método removeItem Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media , método removeItem
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359488"
---
# <a name="playlistremoveitem-method"></a>Método Playlist.removeItem

El **método removeItem** quita el elemento especificado de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.removeItem(
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*item* \[ En\]
</dt> <dd>

**Objeto** multimedia que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el elemento quitado es la pista que se está reproduciendo actualmente (*Player*.**currentMedia**), la reproducción se detiene y el siguiente elemento de la lista de reproducción se convierte en el actual. Si no hay ningún elemento siguiente, se usa el elemento anterior o si no hay ningún otro elemento, *player*. **currentMedia** se establece en **NULL.**

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






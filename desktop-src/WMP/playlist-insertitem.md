---
title: Método Playlist.insertItem
description: El método insertItem inserta un elemento multimedia en la lista de reproducción en la ubicación especificada.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- Método insertItem Reproductor de Windows Media
- Método insertItem Reproductor de Windows Media , clase Playlist
- Clase playlist Reproductor de Windows Media método , insertItem
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359501"
---
# <a name="playlistinsertitem-method"></a>Método Playlist.insertItem

El **método insertItem** inserta un elemento multimedia en la lista de reproducción en la ubicación especificada.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice en el que se va a agregar el elemento.

</dd> <dt>

*item* \[ En\]
</dt> <dd>

**Objeto** multimedia que se insertará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Todos los elementos después del elemento insertado tendrán sus números de índice aumentados en uno.

Para usar este método, se requiere acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.item**](playlist-item.md)
</dt> <dt>

[**Playlist.removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






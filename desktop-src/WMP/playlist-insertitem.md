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
ms.openlocfilehash: 7a71d9ceb39b29c1627ea7596166c39b3dc2f6c76faf45e5ffb54bea14154ac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995705"
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

## <a name="remarks"></a>Comentarios

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

 

 






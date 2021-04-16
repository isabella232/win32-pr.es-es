---
title: Playlist.name
description: La propiedad Name especifica o recupera el nombre de la lista de reproducción.
ms.assetid: f951954a-c280-44e9-96e1-ae18738bc95a
keywords:
- Playlist.name Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a6d34a7b1afb355712a325b1c0f8100c78e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708811"
---
# <a name="playlistname"></a>Playlist.name

La `name` propiedad especifica o recupera el nombre de la lista de reproducción.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentPlaylist*. **nombre** de

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para especificar el valor, se requiere acceso completo. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






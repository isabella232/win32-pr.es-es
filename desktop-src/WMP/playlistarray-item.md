---
title: Método PlaylistArray.item
description: El método item recupera la lista de reproducción en el índice especificado.
ms.assetid: cc851695-f9a2-4594-8bd3-3555c18bfa10
keywords:
- método item Reproductor de Windows Media
- método item Reproductor de Windows Media , clase PlaylistArray
- Clase PlaylistArray Reproductor de Windows Media método , item
topic_type:
- apiref
api_name:
- PlaylistArray.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a45bb38250285563d9e4b7abcc1a4bfd1f7a0bea35b41b7e4cd801f8eff1d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335432"
---
# <a name="playlistarrayitem-method"></a>Método PlaylistArray.item

El **método item** recupera la lista de reproducción en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = PlaylistArray.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que contiene el índice de la lista de reproducción que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **Playlist.**

## <a name="remarks"></a>Comentarios

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto PlaylistArray**](playlistarray-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






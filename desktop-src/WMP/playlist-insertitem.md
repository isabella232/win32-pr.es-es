---
title: Playlist. insertItem (método)
description: El método insertItem inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- método insertItem Media Player Windows
- método insertItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método insertItem
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708224"
---
# <a name="playlistinsertitem-method"></a>Playlist. insertItem (método)

El método **insertItem** inserta un elemento multimedia en la lista de reproducción de la ubicación especificada.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice en el que se va a agregar el elemento.

</dd> <dt>

*elemento* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Todos los elementos después del elemento insertado tendrán los números de índice incrementados en uno.

Para usar este método, se necesita acceso completo a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Playlist. Item**](playlist-item.md)
</dt> <dt>

[**Lista de reproducción. removeItem**](playlist-removeitem.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






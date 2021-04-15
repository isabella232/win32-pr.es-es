---
title: Playlist. moveItem (método)
description: El método moveItem cambia la ubicación de un elemento en la lista de reproducción.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709204"
---
# <a name="playlistmoveitem-method"></a>Playlist. moveItem (método)

El método **moveItem** cambia la ubicación de un elemento en la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oldIndex* \[ de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice anterior.

</dd> <dt>

*NewIndex* \[ de\]
</dt> <dd>

**Número** (**largo**) que contiene el nuevo índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las listas de reproducción almacenadas en la biblioteca pueden cambiar fuera del control. Asegúrese de supervisar y controlar todos los eventos relacionados con la lista de reproducción adecuados para que el orden de los elementos de la lista de reproducción no cambie de forma inesperada.

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

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 






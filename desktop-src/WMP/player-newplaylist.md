---
title: Player. reproducción (método)
description: El método reproducción crea un nuevo objeto de lista de reproducción.
ms.assetid: a566006e-8647-4c51-ab77-762728f25a30
keywords:
- método reproducción de Windows Media Player
- método reproducción Windows Media Player, clase Player
- Clase Player Media Player Windows, método reproducción
topic_type:
- apiref
api_name:
- Player.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa65ae4b453fe919116a33c5ee86b14ba353f681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708251"
---
# <a name="playernewplaylist-method"></a>Player. reproducción (método)

El método **reproducción** crea un nuevo objeto de **lista de reproducción** .

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Player.newPlaylist(
  name,
  URL
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre* \[ de de\]
</dt> <dd>

**Cadena** que contiene el nombre de la nueva lista de reproducción.

</dd> <dt>

*Dirección URL* \[ de\]
</dt> <dd>

**Cadena** que contiene la dirección URL de la lista de reproducción del metarchivo de Windows Media para crear el objeto de **lista de reproducción** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto de **lista de reproducción** .

## <a name="remarks"></a>Observaciones

Si el parámetro de *dirección URL* se establece en null o en "" (cadena vacía), se creará un objeto de **lista de reproducción** vacío. Si el parámetro *Name* se establece en "", se utiliza el nombre del metarchivo.

La nueva lista de reproducción creada con este método no se agrega a la biblioteca. Para agregar una nueva lista de reproducción a la biblioteca, use *PlaylistCollection*. **importPlaylist** o *PlaylistCollection*. **reproducción**. Los espacios iniciales o finales del nombre de la lista de reproducción se quitan automáticamente cuando se agregan a la biblioteca.

Dado que la biblioteca permite varias listas de reproducción con el mismo nombre, es posible que desee comprobar la presencia de una lista de reproducción con un nombre determinado antes de agregar una nueva.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**PlaylistCollection.importPlaylist**](playlistcollection-importplaylist.md)
</dt> <dt>

[**PlaylistCollection. reproducción**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Metaarchivos de Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 






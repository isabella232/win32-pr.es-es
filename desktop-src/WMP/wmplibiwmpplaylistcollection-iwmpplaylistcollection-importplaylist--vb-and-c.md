---
title: IWMPPlaylistCollection importPlaylist, método
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | IWMPPlaylistCollection importPlaylist, método
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- método importPlaylist de Windows Media Player
- método importPlaylist Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708220"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>IWMPPlaylistCollection:: importPlaylist (método)

El método **importPlaylist** agrega una lista de reproducción estática a la biblioteca.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItem* \[ de\]
</dt> <dd>

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que este método va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción agregada.

## <a name="remarks"></a>Observaciones

Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método. Para crear una lista de reproducción vacía en la biblioteca, use el método **reproducción** . Después, puede rellenar la lista de reproducción resultante con elementos multimedia mediante **IWMPPlaylist. appendItem** o **IWMPPlaylist. insertItem**.

Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática. Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use **IWMPMediaCollection. Add**. Para obtener más información, vea [listas de reproducción estáticas y automáticas](static-and-auto-playlists.md).

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMediaCollection. Add (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. reproducción (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 






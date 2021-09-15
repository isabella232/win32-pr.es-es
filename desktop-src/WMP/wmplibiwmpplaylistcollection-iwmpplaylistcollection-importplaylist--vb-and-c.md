---
title: IWMPPlaylistCollection importPlaylist (método)
description: El método importPlaylist agrega una lista de reproducción estática a la biblioteca. | IWMPPlaylistCollection importPlaylist (método)
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- Método importPlaylist Reproductor de Windows Media
- Método importPlaylist Reproductor de Windows Media , interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Reproductor de Windows Media , método importPlaylist
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466994"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>IWMPPlaylistCollection::importPlaylist (método)

El **método importPlaylist** agrega una lista de reproducción estática a la biblioteca.

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

*pItem* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción que agregará este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción agregada.

## <a name="remarks"></a>Observaciones

Las listas de reproducción que no contienen elementos multimedia no se pueden agregar a la biblioteca mediante este método. Para crear una lista de reproducción vacía en la biblioteca, use el **método newPlaylist.** A continuación, puede rellenar la lista de reproducción resultante con elementos multimedia mediante **IWMPPlaylist.appendItem** o **IWMPPlaylist.insertItem**.

Si pasa este método a una lista de reproducción automática, la consulta se ejecuta una vez y el resultado se agrega a la biblioteca como una lista de reproducción estática. Para agregar una lista de reproducción automática a la biblioteca y conservar su comportamiento automático, use **IWMPMediaCollection.add**. Para obtener más información, vea [Listas de reproducción estáticas y automáticas.](static-and-auto-playlists.md)

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior.<br/>                                                                     |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPMediaCollection.add (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.appendItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistCollection (VB y C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.newPlaylist (VB y C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 






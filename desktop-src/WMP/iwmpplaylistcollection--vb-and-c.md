---
title: Interfaz IWMPPlaylistCollection (VB y C) (Wmp.h)
description: Proporciona métodos para manipular interfaces IWMPPlaylist e IWMPPlaylistArray en una colección.
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- Interfaz IWMPPlaylistCollection (VB y C) Reproductor de Windows Media
- Interfaz IWMPPlaylistCollection (VB y C) Reproductor de Windows Media , descrito
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae130b9134d9ad6e19fa062946a591cdf7749b428201750fda8ff55252c3212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575221"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>Interfaz IWMPPlaylistCollection (VB y C#)

Proporciona métodos para manipular **interfaces IWMPPlaylist** **e IWMPPlaylistArray** en una colección.

## <a name="members"></a>Miembros

La **interfaz IWMPPlaylistCollection (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMPPlaylistCollection (VB y C#)** tiene estos métodos.



| Método                                                                                                 | Descripción                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | Devuelve una **interfaz IWMPPlaylistArray** que proporciona acceso a todas las listas de reproducción de la biblioteca.<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | Devuelve una **interfaz IWMPPlaylistArray** que proporciona acceso a las listas de reproducción con el nombre especificado, si existe alguna.<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | Agrega una lista de reproducción estática a la biblioteca.<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | Devuelve un valor que indica si la lista de reproducción especificada está en la carpeta de elementos eliminados.<br/>                           |
| [**newPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | Devuelve una **interfaz IWMPPlaylist** para una nueva lista de reproducción vacía en la biblioteca.<br/>                                     |
| [**eliminar**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | Quita una lista de reproducción de la biblioteca.<br/>                                                                                |
| **setDeleted**                                                                                         | Ya no se admite.<br/>                                                                                                |



 

Obtenga una **interfaz IWMPPlaylistCollection** mediante la siguiente propiedad.



| Object                                                                   | Propiedad                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistCollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylistArray (VB y C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 






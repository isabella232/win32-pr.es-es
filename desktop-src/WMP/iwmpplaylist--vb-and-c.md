---
title: Interfaz IWMPPlaylist (VB y C, Wmp.h)
description: Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción. La interfaz IWMPPlaylist expone las siguientes propiedades.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- IWMPPlaylist (VB y C) interfaz de Windows Media Player
- IWMPPlaylist (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690586"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Interfaz IWMPPlaylist (VB y C#)

Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción.

La interfaz **IWMPPlaylist** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPPlaylist (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPPlaylist (VB y C#)** tiene estos métodos.



| Método                                                                       | Descripción                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Agrega un elemento multimedia al final de la lista de reproducción.<br/>                |
| [**claridad**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Reservado para uso futuro.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Devuelve el valor de un atributo de lista de reproducción especificado por nombre.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Inserta un elemento multimedia en una ubicación especificada de una lista de reproducción.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Cambia la ubicación de un elemento multimedia en la lista de reproducción.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Quita el elemento multimedia especificado de la lista de reproducción.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Establece el valor de un atributo de lista de reproducción.<br/>                      |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPPlaylist (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso           | Descripción                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el número de atributos asociados a una lista de reproducción.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Solo lectura<br/>  | Obtiene el nombre de un atributo de lista de reproducción especificado por un índice. En C#, este es el \_ método get attributeName.<br/>                               |
| [**contabiliza**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Solo lectura<br/>  | Obtiene el número de elementos multimedia de una lista de reproducción.<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Solo lectura<br/>  | Obtiene un valor que indica si la lista de reproducción especificada es idéntica a la lista de reproducción actual. En C#, este es el \_ método get isIdentical.<br/> |
| [**Elemento**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Solo lectura<br/>  | Obtiene una interfaz para el elemento multimedia en el índice especificado. En C#, este es el \_ método get Item.<br/>                                         |
| [**name**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el nombre de la lista de reproducción.<br/>                                                                                                   |



 

Obtenga una interfaz **IWMPPlaylist** con las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.



| Objeto o interfaz                                                | Propiedad o método                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Lista de reproducción**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md), [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum), [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md), [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md), [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **reproducción**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Elemento**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**Reproducción**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 






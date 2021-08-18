---
title: Interfaz IWMPPlaylist (VB y C, Wmp.h)
description: Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción. La interfaz IWMPPlaylist expone las siguientes propiedades.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- Interfaz IWMPPlaylist (VB y C) Reproductor de Windows Media
- Interfaz IWMPPlaylist (VB y C) Reproductor de Windows Media , descrita
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
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119029"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>Interfaz IWMPPlaylist (VB y C#)

Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción.

La **interfaz IWMPPlaylist** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPPlaylist (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPPlaylist (VB y C#)** tiene estos métodos.



| Método                                                                       | Descripción                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Agrega un elemento multimedia al final de la lista de reproducción.<br/>                |
| [**Claro**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Reservado para uso futuro.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Devuelve el valor de un atributo de lista de reproducción especificado por nombre.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Inserta un elemento multimedia en una ubicación especificada de una lista de reproducción.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Cambia la ubicación de un elemento multimedia en la lista de reproducción.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Quita el elemento multimedia especificado de la lista de reproducción.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Establece el valor de un atributo de lista de reproducción.<br/>                      |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPPlaylist (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso           | Descripción                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el número de atributos asociados a una lista de reproducción.<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Solo lectura<br/>  | Obtiene el nombre de un atributo de lista de reproducción especificado por un índice. En C# este es el método get \_ attributeName.<br/>                               |
| [**recuento**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Solo lectura<br/>  | Obtiene el número de elementos multimedia de una lista de reproducción.<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Solo lectura<br/>  | Obtiene un valor que indica si la lista de reproducción especificada es idéntica a la lista de reproducción actual. En C# este es el método \_ get isIdentical.<br/> |
| [**Elemento**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Solo lectura<br/>  | Obtiene una interfaz para el elemento multimedia en el índice especificado. En C# este es el método get \_ Item.<br/>                                         |
| [**Nombre**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el nombre de la lista de reproducción.<br/>                                                                                                   |



 

Obtenga una **interfaz IWMPPlaylist** mediante las siguientes propiedades o métodos a los que se accede a través del siguiente objeto o interfaz.



| Objeto o interfaz                                                | Propiedad o método                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**Lista de reproducción**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll,**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md) [**getByAlbum,**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum) [**getByAttribute,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md) [**getByAuthor,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md) [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md), [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md), [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Elemento**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 






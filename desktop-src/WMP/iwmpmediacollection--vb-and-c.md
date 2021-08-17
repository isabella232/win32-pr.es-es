---
title: Interfaz IWMPMediaCollection (VB y C) (Wmp.h)
description: Proporciona métodos que se pueden usar para organizar una gran colección de elementos multimedia.
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- Interfaz IWMPMediaCollection (VB y C) Reproductor de Windows Media
- Interfaz IWMPMediaCollection (VB y C) Reproductor de Windows Media , descrito
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468455"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>Interfaz IWMPMediaCollection (VB y C#)

Proporciona métodos que se pueden usar para organizar una gran colección de elementos multimedia.

## <a name="members"></a>Miembros

La **interfaz IWMPMediaCollection (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMPMediaCollection (VB y C#)** tiene estos métodos.



| Método                                                                                                                       | Descripción                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | Agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | Devuelve una **interfaz IWMPPlaylist** que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | Devuelve una **interfaz IWMPStringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio.<br/> |
| [**getByAlbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | Devuelve una **interfaz IWMPPlaylist** que proporciona acceso a elementos multimedia del álbum especificado.<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | Devuelve una **interfaz IWMPPlaylist** que corresponde al atributo especificado que tiene el valor especificado.<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | Devuelve una **interfaz IWMPPlaylist** que proporciona acceso a los elementos multimedia por parte del autor especificado.<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | Devuelve una **interfaz IWMPPlaylist** que proporciona acceso a elementos multimedia del género especificado.<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | Devuelve una **interfaz IWMPPlaylist** que proporciona acceso a elementos multimedia con el nombre especificado.<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | Devuelve el índice de un atributo especificado.<br/>                                                                                        |
| **isDeleted**                                                                                                                | Ya no se admite.<br/>                                                                                                               |
| [**eliminar**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | Quita el elemento multimedia especificado de la colección de medios.<br/>                                                                        |
| [**setDeleted**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | Mueve el elemento multimedia especificado a la carpeta de elementos eliminados.<br/>                                                                        |



 

Obtenga una **interfaz IWMPMediaCollection** mediante las siguientes propiedades a las que se accede a través del siguiente objeto o interfaz.



| Objeto o interfaz                                               | Propiedad                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2 (interfaz)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 






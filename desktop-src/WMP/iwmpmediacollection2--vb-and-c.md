---
title: Interfaz IWMPMediaCollection2 (VB y C) (WMP. h)
description: Proporciona métodos que complementan la interfaz IWMPMediaCollection.
ms.assetid: 204f336c-ea78-43d4-9686-bcab72362bc9
keywords:
- IWMPMediaCollection2 (VB y C) interfaz de Windows Media Player
- IWMPMediaCollection2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMediaCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58175e80fbf0f706a9ae6c6b3b69afbd26d52af3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690524"
---
# <a name="iwmpmediacollection2-vb-and-c-interface"></a>Interfaz IWMPMediaCollection2 (VB y C#)

Proporciona métodos que complementan la interfaz **IWMPMediaCollection** .

## <a name="members"></a>Miembros

La interfaz **IWMPMediaCollection2 (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMPMediaCollection2 (VB y C#)** tiene estos métodos.



| Método                                                                                                                     | Descripción                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**createQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)                               | Devuelve una interfaz **IWMPQuery** que representa una nueva consulta.<br/>                                                                                               |
| [**getByAttributeAndMediaType**](wmplibiwmpmediacollection2-iwmpmediacollection2-getbyattributeandmediatype--vb-and-c.md) | Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.<br/>                                     |
| [**getPlaylistByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)                 | Devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.<br/>                                                    |
| [**getStringCollectionByQuery**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md) | Devuelve una interfaz **IWMPStringCollection** que proporciona acceso al conjunto de todos los valores de cadena para un atributo especificado que coinciden con las condiciones de la consulta.<br/> |



 

Obtenga una interfaz **IWMPMediaCollection2** convirtiendo el valor devuelto por la propiedad [**AxWindowsMediaPlayer. mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) o el valor devuelto por la propiedad [**IWMPLibrary. mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 






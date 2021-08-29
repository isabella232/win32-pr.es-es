---
title: Interfaz IWMPMedia2 (VB y C) (Wmp.h)
description: Proporciona acceso a una propiedad de elemento multimedia adicional.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- Interfaz IWMPMedia2 (VB y C) Reproductor de Windows Media
- Interfaz IWMPMedia2 (VB y C) Reproductor de Windows Media , descrito
topic_type:
- apiref
api_name:
- IWMPMedia2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b12b7fe5c3598ff6b6e7f68dabefa93913881776fda4527fe0c0b31b2a94d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054813"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a>Interfaz IWMPMedia2 (VB y C#)

Proporciona acceso a una propiedad de elemento multimedia adicional.

Además de las propiedades y los métodos heredados de **IWMPMedia,** la **interfaz IWMPMedia2** expone la siguiente propiedad.



| Propiedad                                                 | Descripción                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [Error](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | Obtiene una **interfaz IWMPErrorItem** si el elemento multimedia tiene una condición de error. |



 

Obtenga una **interfaz IWMPMedia2** mediante la conversión del valor devuelto por una de las siguientes propiedades o métodos a los que se accede a través del siguiente objeto o interfaz.



| Objeto o interfaz                                               | Propiedad o método                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [Currentitem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Item](iwmpplaylist-item--vb-and-c.md) ( **get \_ Item** in C#)                                                                   |



 

## <a name="members"></a>Miembros

La **interfaz IWMPMedia2 (VB y C#)** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 






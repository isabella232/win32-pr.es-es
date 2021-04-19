---
title: Interfaz IWMPMedia2 (VB y C) (WMP. h)
description: Proporciona acceso a una propiedad de elemento multimedia adicional.
ms.assetid: 7d9f8304-ae26-4175-b9d4-9f272861ef87
keywords:
- IWMPMedia2 (VB y C) interfaz de Windows Media Player
- IWMPMedia2 (VB y C) interfaz de Windows Media Player, se describe
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
ms.openlocfilehash: bb1a77322e0e6649d9a286c920ccd9ddc77890f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689983"
---
# <a name="iwmpmedia2-vb-and-c-interface"></a>Interfaz IWMPMedia2 (VB y C#)

Proporciona acceso a una propiedad de elemento multimedia adicional.

Además de las propiedades y los métodos heredados de **IWMPMedia**, la interfaz **IWMPMedia2** expone la propiedad siguiente.



| Propiedad                                                 | Descripción                                                                   |
|----------------------------------------------------------|-------------------------------------------------------------------------------|
| [Error](wmplibiwmpmedia2-iwmpmedia2-error--vb-and-c.md) | Obtiene una interfaz **IWMPErrorItem** si el elemento multimedia tiene una condición de error. |



 

Obtenga una interfaz **IWMPMedia2** convirtiendo el valor devuelto por una de las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.



| Objeto o interfaz                                               | Propiedad o método                                                                                                                |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [IWMPControls](iwmpcontrols--vb-and-c.md)                        | [currentItem](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                          |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [currentMedia](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md) , [newMedia](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                        | [Elemento](iwmpplaylist-item--vb-and-c.md) ( **obtener \_ elemento** en C#)                                                                   |



 

## <a name="members"></a>Miembros

La interfaz **IWMPMedia2 (VB y C#)** no define ningún miembro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



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

 

 






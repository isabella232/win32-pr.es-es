---
title: Objeto PlayerApplication
description: El objeto PlayerApplication proporciona una manera de coordinar el cambio entre un control de Windows Media Player remoto y el modo completo de Windows Media Player.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Objeto PlayerApplication Media Player de Windows
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104358341"
---
# <a name="playerapplication-object"></a>Objeto PlayerApplication

El objeto **PlayerApplication** proporciona una manera de coordinar el cambio entre un control de Windows Media Player remoto y el modo completo de Windows Media Player. Este objeto solo se usa con programas de C++ que implementan la interfaz **IWMPRemoteMediaServices** e incrustan el control Player en modo remoto. Los archivos de máscara usados como interfaces personalizadas para el control remoto de Windows Media Player tienen acceso a este objeto en el código de script a través del atributo global **playerApplication** .

El objeto **PlayerApplication** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player. |
| [playerDocked](playerapplication-playerdocked.md) | Recupera un valor que indica si el Media Player de Windows está en un estado acoplado.                          |



 

El objeto **PlayerApplication** admite los siguientes métodos.



| Método                                                                       | Descripción                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Cambia un control de Windows Media Player remoto al estado acoplado.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Cambia un control de Windows Media Player remoto al modo completo del reproductor. |



 

Se tiene acceso al objeto **PlayerApplication** a través de la propiedad siguiente.



| Object                      | Propiedad                                          |
|-----------------------------|---------------------------------------------------|
| [Reproductor](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





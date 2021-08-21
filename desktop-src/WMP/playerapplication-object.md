---
title: Objeto PlayerApplication
description: El objeto PlayerApplication proporciona una manera de coordinar el cambio entre un control Reproductor de Windows Media remoto y el modo completo de Reproductor de Windows Media.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- PlayerApplication Object Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46ac009ead54fc4d32b1a302f9228f84484ba6911b353ebb5443653378d9ce61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571836"
---
# <a name="playerapplication-object"></a>Objeto PlayerApplication

El **objeto PlayerApplication** proporciona una manera de coordinar el cambio entre un control Reproductor de Windows Media remoto y el modo completo de Reproductor de Windows Media. Este objeto solo se usa con programas de C++ que implementan la interfaz **IWMPRemoteMediaServices** e insertan el control Player en modo remoto. Los archivos de máscara usados como interfaces personalizadas para el control Reproductor de Windows Media acceso a este objeto en el código de script a través del atributo global **playerApplication.**

El **objeto PlayerApplication** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [hasDisplay](playerapplication-hasdisplay.md)     | Recupera un valor que indica si el vídeo se puede mostrar a través del control Reproductor de Windows Media remoto. |
| [playerDocked](playerapplication-playerdocked.md) | Recupera un valor que indica si Reproductor de Windows Media está en estado acoplado.                          |



 

El **objeto PlayerApplication** admite los métodos siguientes.



| Método                                                                       | Descripción                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [switchToControl](playerapplication-switchtocontrol.md)                     | Cambia un control Reproductor de Windows Media remoto al estado acoplado.            |
| [switchToPlayerApplication](playerapplication-switchtoplayerapplication.md) | Cambia un control Reproductor de Windows Media remoto al modo completo del reproductor. |



 

Se tiene acceso al objeto **PlayerApplication** a través de la propiedad siguiente.



| Object                      | Propiedad                                          |
|-----------------------------|---------------------------------------------------|
| [Reproductor](player-object.md) | [playerApplication](player-playerapplication.md) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





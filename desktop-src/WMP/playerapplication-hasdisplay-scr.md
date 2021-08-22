---
title: Atributo PLAYERAPPLICATION.hasDisplay
description: El atributo hasDisplay recupera un valor que indica si el vídeo se puede mostrar a través del control Reproductor de Windows Media remoto.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION.hasDisplay Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac144f7e9f96db707944cbb016028578d2446be43a0f06cd0293cb5d56f84c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571948"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

El **atributo hasDisplay** recupera un valor que indica si el vídeo se puede mostrar a través del control Reproductor de Windows Media remoto.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de **solo lectura.**



| Valor | Descripción               |
|-------|---------------------------|
| True  | El vídeo se puede mostrar.    |
| Falso | El vídeo no se puede mostrar. |



 

## <a name="remarks"></a>Comentarios

Este atributo solo se usa cuando se usa la comunicación remota Reproductor de Windows Media control .

Varios Reproductor de Windows Media pueden ejecutarse de forma remota al mismo tiempo, pero el vídeo solo se puede mostrar en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles remotos. Use esta propiedad para determinar si el control actual es el a través del cual se puede mostrar el vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 






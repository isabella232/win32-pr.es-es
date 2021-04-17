---
title: Atributo PLAYERAPPLICATION. hasDisplay
description: El atributo hasDisplay recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- PLAYERAPPLICATION. hasDisplay Windows Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708753"
---
# <a name="playerapplicationhasdisplay"></a>PLAYERAPPLICATION.hasDisplay

El atributo **hasDisplay** recupera un valor que indica si el vídeo puede mostrarse a través del control remoto de Windows Media Player.

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de solo lectura.



| Value | Descripción               |
|-------|---------------------------|
| True  | El vídeo se puede mostrar.    |
| False | No se puede mostrar el vídeo. |



 

## <a name="remarks"></a>Observaciones

Este atributo solo se usa cuando la comunicación remota del control de Media Player de Windows.

Varios controles de Windows Media Player se pueden ejecutar de forma remota al mismo tiempo, pero el vídeo solo puede mostrarse en una ubicación a la vez, ya sea en el modo completo del reproductor o en uno de los controles remotos. Utilice esta propiedad para determinar si el control actual es el que se puede mostrar en el vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYERAPPLICATION**](playerapplication-element.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 






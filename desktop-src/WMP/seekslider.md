---
title: SEEKSLIDER
description: Este es un control deslizante predefinido con los siguientes valores predeterminados. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649614"
---
# <a name="seekslider"></a>SEEKSLIDER

Este es un **control deslizante** predefinido con los siguientes valores predeterminados.

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>Observaciones

Esto crea un control **deslizante** que busca el archivo multimedia en cualquier posición. La información sobre herramientas está localizada. Todas las propiedades de este **control deslizante** se pueden invalidar si se especifican de forma explícita.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Windows Media Player 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> </dl>

 

 






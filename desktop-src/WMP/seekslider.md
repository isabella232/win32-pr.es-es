---
title: SEEKSLIDER
description: Se trata de un control SLIDER predefinido con los siguientes valores predeterminados. | SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SeekSLIDER Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070868"
---
# <a name="seekslider"></a>SEEKSLIDER

Se trata de un **control SLIDER** predefinido con los siguientes valores predeterminados.

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

Esto crea un control **SLIDER** que busca el archivo multimedia en cualquier posición. La información sobre herramientas está localizada. Todas las propiedades de **este CONTROL DESLIZANTE** se pueden invalidar si se especifican explícitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 






---
title: SLIDEr. foregroundProgress
description: El atributo foregroundProgress especifica o recupera la posición actual de la barra de progreso del primer plano como un porcentaje del área del control deslizante.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- CONTROL SLIDEr. foregroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661000"
---
# <a name="sliderforegroundprogress"></a>SLIDEr. foregroundProgress

El atributo **foregroundProgress** especifica o recupera la posición actual de la barra de progreso del primer plano como un porcentaje del área del control deslizante.

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) que va de 0 a 100.

## <a name="remarks"></a>Observaciones

Este atributo se usa principalmente para realizar el seguimiento del progreso de la descarga de un archivo multimedia mientras realiza un seguimiento simultáneo de la posición de reproducción actual del archivo mediante el atributo de **valor** . La posición del control deslizante está restringida al área del progreso en primer plano. Esto permite que la búsqueda interactiva tenga lugar solo dentro de la parte disponible de un archivo de descarga.

Para usar esta funcionalidad, el atributo **useForegroundProgress** debe establecerse en true.

## <a name="examples"></a>Ejemplos


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento SLIDEr**](slider-element.md)
</dt> <dt>

[**SLIDEr. min**](slider-min.md)
</dt> <dt>

[**Control deslizante. Max**](slider-max.md)
</dt> <dt>

[**SLIDEr. useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**Control deslizante. valor**](slider-value.md)
</dt> </dl>

 

 






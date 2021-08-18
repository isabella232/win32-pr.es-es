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
ms.openlocfilehash: a294eede05ec2b2f0f84e925aa299c9bcb2388ee2151385e48f2c68e6b4c1328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833344"
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

## <a name="remarks"></a>Comentarios

Esto crea un control **SLIDER** que busca el archivo multimedia en cualquier posición. La información sobre herramientas se localiza. Todas las propiedades de **este CONTROL DESLIZANTE** se pueden invalidar especificándolos explícitamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 






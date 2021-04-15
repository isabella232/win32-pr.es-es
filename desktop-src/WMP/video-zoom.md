---
title: VÍDEO. zoom
description: El atributo zoom especifica el porcentaje por el que se va a escalar el vídeo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VÍDEO. zoom Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708150"
---
# <a name="videozoom"></a>VÍDEO. zoom

El atributo **zoom** especifica el porcentaje por el que se va a escalar el vídeo.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**largo**) que va desde 1 hasta el tamaño máximo que se aloja en el ancho y el alto del control de vídeo. Tiene un valor predeterminado de 100.

## <a name="remarks"></a>Observaciones

Este atributo no se puede usar junto con el atributo de **pantalla completa** .

Si se especifican el **ancho** y el **alto** , y la ventana de vídeo resultante es mayor que el vídeo que se está reproduciendo, el vídeo se puede aumentar escalando hasta el tamaño máximo que se encuentra en la ventana. Si no se especifican el **ancho** y el **alto** , el **zoom** se limita a los valores de 100 o menos.

Si el valor de la propiedad **shrinkToFit** es false, el vídeo cambiará de proporción al zoom, para ajustarse al espacio disponible. Si **shrinkToFit** es true, el vídeo se reducirá para caber en la dimensión más restrictiva, a la vez que conserva sus proporciones originales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vídeo**](video-element.md)
</dt> <dt>

[**VÍDEO. fullScreen**](video-fullscreen.md)
</dt> <dt>

[**VÍDEO. shrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 






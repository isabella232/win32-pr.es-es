---
title: VIDEO.zoom
description: El atributo de zoom especifica el porcentaje por el que se va a escalar el vídeo.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- Video.zoom Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070801"
---
# <a name="videozoom"></a>VIDEO.zoom

El **atributo de** zoom especifica el porcentaje por el que se va a escalar el vídeo.

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un  número de lectura y escritura (long)que va desde 1 hasta el tamaño máximo que se adapta al ancho y alto del control Vídeo. Tiene un valor predeterminado de 100.

## <a name="remarks"></a>Observaciones

Este atributo no se puede usar junto con el **atributo fullScreen.**

Si  se **especifican** el ancho y el alto, y la ventana de vídeo resultante es mayor que el vídeo que se reproduce, el vídeo se puede ampliar escalando verticalmente hasta el tamaño máximo que se adapta a la ventana. Si **no** se **especifican el** ancho y el alto, el **zoom** se limita a los valores de 100 o menos.

Si la **propiedad shrinkToFit** es false, el vídeo cambiará la proporción al acercarse para ajustarse al espacio disponible. Si **shrinkToFit es** true, el vídeo se reducirá para ajustarse a la dimensión más restrictiva, conservando al mismo tiempo sus proporciones originales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO.fullScreen**](video-fullscreen.md)
</dt> <dt>

[**VIDEO.shrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 






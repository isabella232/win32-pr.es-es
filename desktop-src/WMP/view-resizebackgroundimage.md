---
title: VIEW.resizeBackgroundImage
description: El atributo resizeBackgroundImage especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.
ms.assetid: d18f3def-777f-4a71-961e-73bae98a4c64
keywords:
- VIEW.resizeBackgroundImage Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizeBackgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 397929d69cc6ac6ad51c29883898c153218afdca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567472"
---
# <a name="viewresizebackgroundimage"></a>VIEW.resizeBackgroundImage

El **atributo resizeBackgroundImage** especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.

``` syntax
        elementID.resizeBackgroundImage
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valores | Descripción                                      |
|--------|--------------------------------------------------|
| true   | Se puede cambiar el tamaño de la imagen de fondo.             |
| false  | Predeterminada. No se puede cambiar el tamaño de la imagen de fondo. |



 

## <a name="remarks"></a>Observaciones

Si establece este atributo en true, el tamaño de la imagen de fondo se ajustará a los valores actuales de los **atributos de** ancho **y** alto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Version<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ELEMENTO VIEW**](view-element.md)
</dt> <dt>

[**VIEW.backgroundImage**](view-backgroundimage.md)
</dt> </dl>

 

 






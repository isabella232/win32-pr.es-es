---
title: BUTTON.tiled
description: El atributo en mosaico especifica o recupera un valor que indica si la imagen BUTTON se va a aplicar en mosaico.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- Button.tiled Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889393"
---
# <a name="buttontiled"></a>BUTTON.tiled

El **atributo en** mosaico especifica o recupera un valor que indica si la imagen **BUTTON** se va a aplicar en mosaico.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                       |
|-------|-----------------------------------|
| true  | La imagen se mostrará en mosaico.              |
| false | Predeterminada. La imagen no se mostrará en mosaico. |



 

## <a name="remarks"></a>Observaciones

Si la imagen es menor que la región real del control, el rellenado de la imagen la repetirá hasta que rellene toda la región. Si no se especifica una imagen o no se puede recuperar, **el mosaico** se establecerá en false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 






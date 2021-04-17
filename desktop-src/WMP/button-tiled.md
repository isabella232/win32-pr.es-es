---
title: BOTÓN. en mosaico
description: El atributo en mosaico especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del botón.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BOTÓN. Media Player de Windows en mosaico
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700356"
---
# <a name="buttontiled"></a>BOTÓN. en mosaico

El atributo en **mosaico** especifica o recupera un valor que indica si se va a colocar en mosaico la imagen del **botón** .

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                       |
|-------|-----------------------------------|
| true  | La imagen se mostrará en mosaico.              |
| false | Predeterminada. La imagen no se mostrará en mosaico. |



 

## <a name="remarks"></a>Observaciones

Si la imagen es menor que la región real del control, el mosaico de la imagen se repetirá hasta que se llene toda la región. Si no se especifica una imagen o no se puede recuperar, en **mosaico** se establecerá en false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÓN. imagen**](button-image.md)
</dt> </dl>

 

 






---
title: EFFECTs. windowed
description: El atributo windowed especifica o recupera un valor que indica si la visualización se va a mostrar o no en ventanas, es decir, si todo el rectángulo del control será visible en todo momento o si se puede recortar.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFECTOS. ventanas de Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700343"
---
# <a name="effectswindowed"></a>EFFECTs. windowed

El atributo **windowed** especifica o recupera un valor que indica si la visualización se va a mostrar o no en ventanas, es decir, si todo el rectángulo del control será visible en todo momento o si se puede recortar. Este atributo solo se puede establecer en tiempo de diseño.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura después.



| Value | Descripción                              |
|-------|------------------------------------------|
| true  | El control se mostrará en la ventana.            |
| false | Predeterminada. El control no tendrá ventanas. |



 

## <a name="remarks"></a>Observaciones

Si se desea una ventana de visualización no rectangular, o si una imagen incluye alguna parte de la ventana, este atributo debe establecerse en false. Esto sacrifica algún rendimiento para realizar el recorte necesario.

Si **windowed** está establecido en true, se omite cualquier imagen que abarque la ventana de visualización y la ventana de visualización tiene el orden z de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EFFECTs, elemento**](effects-element.md)
</dt> </dl>

 

 






---
title: EFFECTS.windowed
description: El atributo windowed especifica o recupera un valor que indica si la visualización se va a usar en ventanas o sin ventanas, es decir, si todo el rectángulo del control estará visible en todo momento o si se puede recortar.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFECTS.windowed Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651005"
---
# <a name="effectswindowed"></a>EFFECTS.windowed

El atributo **windowed** especifica o recupera un valor que indica si la visualización se va a usar en ventanas o sin ventanas, es decir, si todo el rectángulo del control estará visible en todo momento o si se puede recortar. Este atributo solo se puede establecer en tiempo de diseño.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura a partir de entonces.



| Valor | Descripción                              |
|-------|------------------------------------------|
| true  | El control se abrirá en ventanas.            |
| false | Predeterminada. El control no tendrá ventanas. |



 

## <a name="remarks"></a>Comentarios

Si se desea una ventana de visualización no rectangular o si alguna parte de la ventana está cubierta por una imagen, este atributo debe establecerse en false. Esto sacrifique cierto rendimiento para realizar el recorte necesario.

Si **windowed** se establece en true, se omite cualquier imagen que cubre la ventana de visualización y la ventana de visualización tiene el orden Z de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO EFFECTS**](effects-element.md)
</dt> </dl>

 

 






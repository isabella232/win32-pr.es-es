---
title: VÍDEO. sin ventanas
description: El atributo sin ventana especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VÍDEO Media Player ventanas sin ventanas
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708880"
---
# <a name="videowindowless"></a>VÍDEO. sin ventanas

El atributo **sin ventana** especifica o recupera un valor que indica si el control de vídeo se va a mostrar o no en ventanas; es decir, si todo el rectángulo del control será visible en todo momento o se puede recortar. Solo se puede establecer en tiempo de diseño.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura después.



| Value | Descripción                              |
|-------|------------------------------------------|
| true  | El control de vídeo no tendrá ventanas.        |
| false | Predeterminada. El control de vídeo se mostrará en una ventana. |



 

## <a name="remarks"></a>Observaciones

Si se desea una ventana de vídeo no rectangular, o si quiere cubrir cualquier parte de la ventana de vídeo con una imagen, este atributo debe establecerse en true. Esto sacrifica algún rendimiento para realizar el recorte necesario.

La reproducción de vídeo está optimizada para la reproducción no recortada. En este caso, el atributo **Windowless** está establecido en false y siempre se muestra el rectángulo de vídeo completo. Se omite cualquier imagen que abarque la ventana de vídeo y la ventana de vídeo tiene el orden z de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vídeo**](video-element.md)
</dt> </dl>

 

 






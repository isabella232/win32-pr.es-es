---
title: VIDEO.windowless
description: El atributo sin ventanas especifica o recupera un valor que indica si el control Vídeo se abrirá o no. es decir, si todo el rectángulo del control estará visible en todo momento o se puede recortar.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- Video.windowless Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070803"
---
# <a name="videowindowless"></a>VIDEO.windowless

El **atributo sin** ventanas especifica o recupera un valor que indica si el control Vídeo se abrirá o no. es decir, si todo el rectángulo del control estará visible en todo momento o se puede recortar. Solo se puede establecer en tiempo de diseño.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** especificado en tiempo de diseño y de solo lectura a partir de entonces.



| Value | Descripción                              |
|-------|------------------------------------------|
| true  | El control de vídeo no tendrá ventanas.        |
| false | Predeterminada. El control de vídeo se abrirá en ventanas. |



 

## <a name="remarks"></a>Observaciones

Si se desea una ventana de vídeo no rectangular o si desea cubrir cualquier parte de la ventana de vídeo con una imagen, este atributo debe establecerse en true. Esto sacrifique cierto rendimiento para realizar el recorte necesario.

La reproducción de vídeo está optimizada para la reproducción sin velocidad. En este caso, el **atributo sin** ventanas se establece en false y siempre se muestra todo el rectángulo de vídeo. Cualquier imagen que cubre la ventana de vídeo se omite y la ventana de vídeo tiene el orden Z de nivel superior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 






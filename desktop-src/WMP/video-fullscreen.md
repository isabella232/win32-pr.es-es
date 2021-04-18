---
title: VÍDEO. fullScreen
description: El atributo fullScreen especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VÍDEO de Windows. fullScreen Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709010"
---
# <a name="videofullscreen"></a>VÍDEO. fullScreen

El atributo **Fullscreen** especifica o recupera un valor que indica si el vídeo se muestra en el modo de pantalla completa.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | El vídeo se muestra en el modo de pantalla completa.                  |
| false | Predeterminada. El vídeo no se muestra en el modo de pantalla completa. |



 

## <a name="remarks"></a>Observaciones

Esta propiedad solo se puede especificar en tiempo de ejecución, después de que se haya cargado un archivo. Por lo tanto, debe establecerse en un controlador de eventos de script. El botón escape se usa para volver a la vista normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de vídeo**](video-element.md)
</dt> <dt>

[**VÍDEO. maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VÍDEO. shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VÍDEO. stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 






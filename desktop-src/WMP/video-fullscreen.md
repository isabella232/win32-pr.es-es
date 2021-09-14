---
title: VIDEO.fullScreen
description: El atributo fullScreen especifica o recupera un valor que indica si el vídeo se muestra en modo de pantalla completa.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- Video.fullScreen Reproductor de Windows Media
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070823"
---
# <a name="videofullscreen"></a>VIDEO.fullScreen

El **atributo fullScreen** especifica o recupera un valor que indica si el vídeo se muestra en modo de pantalla completa.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un valor booleano de lectura **y escritura.**



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | El vídeo se muestra en modo de pantalla completa.                  |
| false | Predeterminada. El vídeo no se muestra en modo de pantalla completa. |



 

## <a name="remarks"></a>Observaciones

Esta propiedad solo se puede especificar en tiempo de ejecución, una vez cargado un archivo. Por lo tanto, debe establecerse dentro de un controlador de eventos de script. El botón de escape se usa para volver a la vista normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> <dt>

[**VIDEO.maintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**VIDEO.shrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**VIDEO.stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 






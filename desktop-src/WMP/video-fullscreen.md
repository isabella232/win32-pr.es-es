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
ms.openlocfilehash: e8150843ab14148d398b11cba82aa52711621c15962976ca37d5332a6ae58f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465704"
---
# <a name="videofullscreen"></a>VIDEO.fullScreen

El **atributo fullScreen** especifica o recupera un valor que indica si el vídeo se muestra en modo de pantalla completa.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Value | Descripción                                          |
|-------|------------------------------------------------------|
| true  | El vídeo se muestra en modo de pantalla completa.                  |
| false | Predeterminada. El vídeo no se muestra en modo de pantalla completa. |



 

## <a name="remarks"></a>Observaciones

Esta propiedad solo se puede especificar en tiempo de ejecución, una vez cargado un archivo. Por lo tanto, debe establecerse dentro de un controlador de eventos de script. El botón de escape se usa para volver a la visualización normal.

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

 

 






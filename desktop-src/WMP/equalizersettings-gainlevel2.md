---
title: EQUALIZERSETTINGS.gainLevel2
description: El atributo gainLevel2 especifica o recupera el nivel de ganancia de la banda 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS.gainLevel2 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339835"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

El **atributo gainLevel2** especifica o recupera el nivel de ganancia de la banda 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 62Hz.

Si no se especifica este atributo, se conservará el valor anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






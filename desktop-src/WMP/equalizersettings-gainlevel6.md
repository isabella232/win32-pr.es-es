---
title: EQUALIZERSETTINGS.gainLevel6
description: El atributo gainLevel6 especifica o recupera el nivel de ganancia de la banda 6. Tiene un valor predeterminado de cero.
ms.assetid: da3e1df5-434b-44db-bcde-8ad9c9874627
keywords:
- EQUALIZERSETTINGS.gainLevel6 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel6
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7238fc2d90828bdae8e3a4c0ca7cf3700462cd27b7a180169e4a7293c1ae3472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650935"
---
# <a name="equalizersettingsgainlevel6"></a>EQUALIZERSETTINGS.gainLevel6

El **atributo gainLevel6** especifica o recupera el nivel de ganancia de la banda 6. Tiene un valor predeterminado de cero.

``` syntax
        elementID.gainLevel6
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 1 kHz.

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

 

 






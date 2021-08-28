---
title: EQUALIZERSETTINGS.gainLevel3
description: El atributo gainLevel3 especifica o recupera el nivel de ganancia de la banda 3.
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- EQUALIZERSETTINGS.gainLevel3 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8e719cd59a253ded35ad10e067f537d6f7d3a68d0d0b05a4cf79d0cd976f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123655"
---
# <a name="equalizersettingsgainlevel3"></a>EQUALIZERSETTINGS.gainLevel3

El **atributo gainLevel3** especifica o recupera el nivel de ganancia de la banda 3.

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 125Hz.

Si no se especifica este atributo, se conservará el valor anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






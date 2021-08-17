---
title: EQUALIZERSETTINGS.gainLevel7
description: El atributo gainLevel7 especifica o recupera el nivel de ganancia de la banda 7.
ms.assetid: f39e1475-b0c8-4204-b2d8-943bc8b4f830
keywords:
- EQUALIZERSETTINGS.gainLevel7 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel7
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbb18676e97bc7b850dca9683f13d8e6983a138a3b674f03392645d81ab3d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935132"
---
# <a name="equalizersettingsgainlevel7"></a>EQUALIZERSETTINGS.gainLevel7

El **atributo gainLevel7** especifica o recupera el nivel de ganancia de la banda 7.

``` syntax
        elementID.gainLevel7
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 2 kHz.

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

 

 






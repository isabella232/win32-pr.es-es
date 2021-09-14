---
title: EQUALIZERSETTINGS.gainLevel10
description: El atributo gainLevel10 especifica o recupera el nivel de ganancia de la banda 10.
ms.assetid: 0d645719-86aa-4475-8e87-ea6c20e4fed7
keywords:
- EQUALIZERSETTINGS.gainLevel10 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512819d4c01524e82a92fee9849a9589366a36ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240968"
---
# <a name="equalizersettingsgainlevel10"></a>EQUALIZERSETTINGS.gainLevel10

El **atributo gainLevel10** especifica o recupera el nivel de ganancia de la banda 10.

``` syntax
        elementID.gainLevel10
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 16 kHz.

Si no se especifica este atributo, se conservará el valor anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






---
title: EQUALIZERSETTINGS.gainLevel9
description: El atributo gainLevel9 especifica o recupera el nivel de ganancia de la banda 9.
ms.assetid: 2bed7486-4d4c-4c71-8bab-8dd0c4f56911
keywords:
- EQUALIZERSETTINGS.gainLevel9 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel9
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd03197b4d1b6be48b0e91193b3eebfaf28a768
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071009"
---
# <a name="equalizersettingsgainlevel9"></a>EQUALIZERSETTINGS.gainLevel9

El **atributo gainLevel9** especifica o recupera el nivel de ganancia de la banda 9.

``` syntax
        elementID.gainLevel9
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** (**float**) con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 8 kHz.

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

 

 






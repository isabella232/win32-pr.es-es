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
ms.openlocfilehash: 1762613b54e488f1f364b13b9970104287e8cf53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073276"
---
# <a name="equalizersettingsgainlevel6"></a>EQUALIZERSETTINGS.gainLevel6

El **atributo gainLevel6** especifica o recupera el nivel de ganancia de la banda 6. Tiene un valor predeterminado de cero.

``` syntax
        elementID.gainLevel6
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 1 kHz.

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

 

 






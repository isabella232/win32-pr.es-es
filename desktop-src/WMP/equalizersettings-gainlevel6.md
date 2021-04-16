---
title: EQUALIZERSETTINGS.gainLevel6
description: El atributo gainLevel6 especifica o recupera el nivel de ganancia de la banda 6. Tiene un valor predeterminado de cero.
ms.assetid: da3e1df5-434b-44db-bcde-8ad9c9874627
keywords:
- EQUALIZERSETTINGS. gainLevel6 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel6
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1762613b54e488f1f364b13b9970104287e8cf53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699453"
---
# <a name="equalizersettingsgainlevel6"></a>EQUALIZERSETTINGS.gainLevel6

El atributo **gainLevel6** especifica o recupera el nivel de ganancia de la banda 6. Tiene un valor predeterminado de cero.

``` syntax
        elementID.gainLevel6
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de frecuencias de audio centrada en 1kHz.

Si no se especifica este atributo, se conservará el valor anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 






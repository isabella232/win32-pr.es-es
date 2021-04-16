---
title: EQUALIZERSETTINGS.gainLevel4
description: El atributo gainLevel4 especifica o recupera el nivel de ganancia de la banda 4.
ms.assetid: 01383171-f991-4d09-858a-ce21ce93e14e
keywords:
- EQUALIZERSETTINGS. gainLevel4 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea5359a9dae8bac12f89effa8afbeceaef9f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699457"
---
# <a name="equalizersettingsgainlevel4"></a>EQUALIZERSETTINGS.gainLevel4

El atributo **gainLevel4** especifica o recupera el nivel de ganancia de la banda 4.

``` syntax
        elementID.gainLevel4
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de la frecuencia de audio centrada en 250Hz.

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

 

 






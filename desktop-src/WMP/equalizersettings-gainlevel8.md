---
title: EQUALIZERSETTINGS.gainLevel8
description: El atributo gainLevel8 especifica o recupera el nivel de ganancia de la banda 8.
ms.assetid: 1cd4fa26-ed9b-4312-8272-9fe8011658e8
keywords:
- EQUALIZERSETTINGS. gainLevel8 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel8
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 814f22a94d1e69c2d101154c6f4a3984a67bd75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699447"
---
# <a name="equalizersettingsgainlevel8"></a>EQUALIZERSETTINGS.gainLevel8

El atributo **gainLevel8** especifica o recupera el nivel de ganancia de la banda 8.

``` syntax
        elementID.gainLevel8
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de la frecuencia de audio centrada en 4kHz.

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

 

 






---
title: EQUALIZERSETTINGS.gainLevel5
description: El atributo gainLevel5 especifica o recupera el nivel de ganancia de la banda 5.
ms.assetid: 6077a4dc-b9b8-4e00-8b29-14afe5a44321
keywords:
- EQUALIZERSETTINGS. gainLevel5 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel5
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b68e3567b4064a650a9f69cc4608e2b69600cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699456"
---
# <a name="equalizersettingsgainlevel5"></a>EQUALIZERSETTINGS.gainLevel5

El atributo **gainLevel5** especifica o recupera el nivel de ganancia de la banda 5.

``` syntax
        elementID.gainLevel5
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **número** de lectura/escritura (**float**) con un valor que normalmente oscila entre 20 y + 20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de la frecuencia de audio centrada en 500Hz.

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

 

 






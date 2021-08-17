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
ms.openlocfilehash: 9e80e05686d06871aa40e8a649a119a41fb1a7a59bbb60a77b56497561ae9f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748822"
---
# <a name="equalizersettingsgainlevel10"></a>EQUALIZERSETTINGS.gainLevel10

El **atributo gainLevel10** especifica o recupera el nivel de ganancia de la banda 10.

``` syntax
        elementID.gainLevel10
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 16 kHz.

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

 

 






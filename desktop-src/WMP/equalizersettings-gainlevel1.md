---
title: EQUALIZERSETTINGS.gainLevel1
description: El atributo gainLevel1 especifica o recupera el nivel de ganancia de la banda 1.
ms.assetid: 3d681ade-3fd4-432d-ae92-c083d927346f
keywords:
- EQUALIZERSETTINGS.gainLevel1 Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel1
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3299c2b9275eabb4812c83670f28bcbb3d2aeef9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240969"
---
# <a name="equalizersettingsgainlevel1"></a>EQUALIZERSETTINGS.gainLevel1

El **atributo gainLevel1** especifica o recupera el nivel de ganancia de la banda 1.

``` syntax
        elementID.gainLevel1
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(float)** con un valor que normalmente oscila entre 20 y +20. Tiene un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

Este atributo ajusta la parte del espectro de frecuencia de audio centrada en 31Hz.

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

 

 






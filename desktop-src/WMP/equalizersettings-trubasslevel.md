---
title: EQUALIZERSETTINGS.truBassLevel
description: El atributo truBassLevel especifica o recupera el nivel de SrS TruBass.
ms.assetid: 9f8c9dbe-d535-42af-8ea7-74fc10526fba
keywords:
- EQUALIZERSETTINGS.truBassLevel Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.truBassLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17fdb293ee081c99055a88fcd8a6ffeb420c9eb922be655f92df04c71058af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901955"
---
# <a name="equalizersettingstrubasslevel"></a>EQUALIZERSETTINGS.truBassLevel

El **atributo truBassLevel** especifica o recupera el nivel de SrS TruBass.

``` syntax
        elementID.truBassLevel
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(long)** que va de 0 a 100 con un valor predeterminado de 50.

## <a name="remarks"></a>Comentarios

TruBass es un efecto que mejora el sonido de los niveles de bajo de la pista de audio. Este atributo se omite si **enhancedAudio** está establecido en false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 






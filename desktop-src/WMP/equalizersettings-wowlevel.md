---
title: EQUALIZERSETTINGS.wowLevel
description: El atributo wowLevel especifica o recupera el nivel de efecto WOW de SRS.
ms.assetid: 8f99d7e1-39b9-42be-ab6d-8435ba7022fa
keywords:
- EQUALIZERSETTINGS.wowLevel Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.wowLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ceef9ed737018951478baac1c62571e6cf9b2ff8eb6cf8d1bedc78f068aef60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123645"
---
# <a name="equalizersettingswowlevel"></a>EQUALIZERSETTINGS.wowLevel

El **atributo wowLevel** especifica o recupera el nivel de efecto WOW de SRS.

``` syntax
        elementID.wowLevel
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un número de lectura y **escritura** **(long)** que va de 0 a 100 con un valor predeterminado de 50.

## <a name="remarks"></a>Comentarios

El efecto WOW de SRS es un efecto de mejora de audio. Este atributo se omite si **enhancedAudio** está establecido en false.

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

 

 






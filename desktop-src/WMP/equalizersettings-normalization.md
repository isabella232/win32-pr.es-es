---
title: EQUALIZERSETTINGS.normalization
description: El atributo de normalización especifica o recupera un valor que indica si la normalización está habilitada.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS.normalization Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f2befdd62f0508822d5547cb3b894b93ea095f52db4cf9bbdb4a444d99251c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578177"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS.normalization

El **atributo de normalización** especifica o recupera un valor que indica si la normalización está habilitada.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un booleano de lectura **y escritura.**



| Valor | Descripción                         |
|-------|-------------------------------------|
| true  | La normalización está habilitada.           |
| false | Predeterminada. La normalización está deshabilitada. |



 

## <a name="remarks"></a>Comentarios

Cuando se habilita la normalización, la señal de audio de un archivo multimedia digital completo se escala verticalmente hasta el valor máximo. Esto permite reproducir varios archivos aproximadamente en el mismo volumen sin necesidad de ajustes de volumen.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 






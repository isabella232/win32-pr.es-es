---
title: EQUALIZERSETTINGS. Normalization
description: El atributo Normalization especifica o recupera un valor que indica si está habilitada la normalización.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normal Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699445"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS. Normalization

El atributo **Normalization** especifica o recupera un valor que indica si está habilitada la normalización.

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>Valores posibles

Este atributo es un **valor booleano** de lectura/escritura.



| Value | Descripción                         |
|-------|-------------------------------------|
| true  | La normalización está habilitada.           |
| false | Predeterminada. La normalización está deshabilitada. |



 

## <a name="remarks"></a>Observaciones

Cuando se habilita la normalización, la señal de audio de un archivo multimedia digital completo se escala hasta el valor máximo. Esto permite reproducir varios archivos aproximadamente en el mismo volumen sin necesidad de ajustes de volumen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 






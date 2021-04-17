---
description: Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Propiedad AVEncDDDialogNormalization (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495623"
---
# <a name="avencdddialognormalization-property"></a>Propiedad AVEncDDDialogNormalization

Especifica el nivel de normalización del cuadro de diálogo, en decibelios (dB), en una secuencia de audio Dolby digital. Esta propiedad se aplica a los codificadores de audio Dolby digital.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncDDDialogNormalization**

## <a name="property-value"></a>Valor de propiedad

Esta propiedad tiene un intervalo de valores lineal. Para obtener el intervalo admitido, llame a [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





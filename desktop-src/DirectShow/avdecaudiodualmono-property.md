---
description: 'Propiedad AVDecAudioDualMono: especifica si el audio de 2 canales se codifica como estéreo o mono dual.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propiedad AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096573"
---
# <a name="avdecaudiodualmono-property"></a>AvDecAudioDualMono, propiedad

Especifica si el audio de 2 canales se codifica como estéreo o mono dual.

Esta propiedad es de solo lectura.

## <a name="data-type"></a>Tipo de datos

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecAudioDualMono.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)

## <a name="remarks"></a>Comentarios

Esta propiedad solo se aplica cuando la secuencia de bits de entrada del descodificador contiene audio de dos canales. Una secuencia de audio de dos canales se puede codificar como estéreo o como mono dual. Si el audio es mono dual, puede establecer la propiedad [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) para configurar cómo reproduce el audio el descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones de escritorio para \[ UWP de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones de escritorio de Windows 2000 Server \[ \| para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





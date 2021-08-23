---
description: 'Propiedad AVDecAudioDualMono: especifica si el audio de 2 canales se codifica como estéreo o mono dual.'
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Propiedad AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a26bd6685cb9c9f326babbc01120019c93760fd7e1f9bf33f2a540d488300ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873395"
---
# <a name="avdecaudiodualmono-property"></a>AvDecAudioDualMono, propiedad

Especifica si el audio de 2 canales está codificado como estéreo o mono dual.

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional \[ aplicaciones de escritorio para \| UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 





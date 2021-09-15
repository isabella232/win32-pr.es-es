---
description: Especifica el modo de bajada estéreo para un descodificador de audio Dolby Digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: CODECAPI_AVDecDDStereoDownMixMode propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574977"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>Propiedad CODECAPI \_ AVDecDDStereoDownMixMode

Especifica el modo de bajada estéreo para un descodificador de audio Dolby Digital.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la [**enumeración eAVDecDDStereoDownMixMode.**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode)

## <a name="remarks"></a>Observaciones

Este atributo se aplica cuando la entrada al descodificador es audio PCM multicanal y la salida es audio estéreo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 


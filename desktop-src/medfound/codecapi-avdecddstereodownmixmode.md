---
description: Especifica el modo downmix estéreo para un descodificador de audio Dolby digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: Propiedad CODECAPI_AVDecDDStereoDownMixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423571"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>\_Propiedad AVDecDDStereoDownMixMode de CODECAPI

Especifica el modo downmix estéreo para un descodificador de audio Dolby digital.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valor de propiedad

El valor de esta propiedad es un miembro de la enumeración [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .

## <a name="remarks"></a>Observaciones

Este atributo se aplica cuando la entrada para el descodificador es audio PCM multicanal y el resultado es audio estéreo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 


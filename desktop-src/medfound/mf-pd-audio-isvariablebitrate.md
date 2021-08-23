---
description: Especifica si las secuencias de audio de una presentación tienen una velocidad de bits variable.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: MF_PD_AUDIO_ISVARIABLEBITRATE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5c8c15c12bcd867342fb11f5e753c196f9954aea0393b2a461e1804f411339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664195"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a>Atributo \_ MF PD AUDIO \_ \_ ISVARIABLEBITRATE

Especifica si las secuencias de audio de una presentación tienen una velocidad de bits variable.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Comentarios

Se trata de un atributo opcional para los descriptores de presentación. Si el atributo es **TRUE** (distinto de cero), la presentación contiene al menos una secuencia de audio de velocidad de bits variable (VBR). Si el atributo es **FALSE,** todas las secuencias de audio tienen una velocidad de bits constante.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 





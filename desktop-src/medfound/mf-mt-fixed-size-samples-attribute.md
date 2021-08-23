---
description: Especifica para un tipo de medio si las muestras tienen un tamaño fijo.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: MF_MT_FIXED_SIZE_SAMPLES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3662532d1e10857945a828ec3f46beef991fb438dfea0f33dc7d73832aeca7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605635"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a>Atributo MF \_ MT \_ FIXED SIZE \_ \_ SAMPLES

Especifica para un tipo de medio si las muestras tienen un tamaño fijo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE**, cada muestra de la secuencia tiene el mismo tamaño (en bytes). De lo contrario, las muestras pueden variar de tamaño.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 





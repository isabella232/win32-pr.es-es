---
description: Especifica para un tipo de medio si los ejemplos tienen un tamaño fijo.
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: MF_MT_FIXED_SIZE_SAMPLES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659849"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a>\_Atributo MF MT \_ fixed \_ size \_ Samples

Especifica para un tipo de medio si los ejemplos tienen un tamaño fijo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, todas las muestras de la secuencia tienen el mismo tamaño (en bytes). De lo contrario, los ejemplos pueden variar en tamaño.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 





---
description: Contiene la etiqueta de formato WAVE original para una secuencia de audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89f05086858f54c619e3896f5978cf81005e9b1e80e858bc89c71e951ab48b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741670"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>Atributo MF \_ MT ORIGINAL WAVE FORMAT \_ \_ \_ \_ TAG

Contiene la etiqueta de formato WAVE original para una secuencia de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Dependiendo del archivo de origen, el origen de medios AVI podría establecer este atributo en los tipos de medios que ofrece.

Un archivo AVI contiene un encabezado de secuencia para cada secuencia del archivo. El origen multimedia AVI traduce el encabezado de secuencia en un tipo de medio. Para las secuencias de audio, el encabezado de secuencia contiene una etiqueta de formato que identifica el formato de audio. (La etiqueta de formato se encuentra en el **miembro wFormatTag** de la [**estructura DEFORMATEX).**](/previous-versions/dd757713(v=vs.85)) En la mayoría de los casos, el origen multimedia AVI convierte la etiqueta de formato directamente en un GUID de subtipo, como se describe en el tema [**Guid de subtipo de audio**](audio-subtype-guids.md). Sin embargo, en algunos casos, asigna la etiqueta de formato original a otra etiqueta de formato equivalente. Si es así, el origen del medio almacena la etiqueta de formato original en el tipo de medio, mediante el atributo MF \_ MT ORIGINAL WAVE FORMAT \_ \_ \_ \_ TAG.

Las asignaciones de formato se almacenan en el Registro con la clave siguiente:

**HKEY \_ CLASSES \_ ROOT** \\ **MediaFoundation** \\ **MapAudioFormatTag**

Cada entrada es un **valor DWORD.** El nombre de la entrada es la representación decimal de la etiqueta de formato. El valor de la entrada es la etiqueta de formato equivalente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 

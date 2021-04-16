---
description: Contiene la etiqueta de formato de onda original para una secuencia de audio.
ms.assetid: 2b30a1c2-4a42-4b09-acb6-b76267cc7ed0
title: MF_MT_ORIGINAL_WAVE_FORMAT_TAG atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba89171f9ae2bf3ab99df05bd3ae64b7d52be6d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678503"
---
# <a name="mf_mt_original_wave_format_tag-attribute"></a>MF \_ MT \_ original \_ \_ atributo de etiqueta de formato de onda \_

Contiene la etiqueta de formato de onda original para una secuencia de audio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Dependiendo del archivo de origen, el origen de medios AVI podría establecer este atributo en los tipos de medios que ofrece.

Un archivo AVI contiene un encabezado de secuencia para cada flujo del archivo. El origen de medios AVI traduce el encabezado de secuencia en un tipo de medio. En el caso de las secuencias de audio, el encabezado de flujo contiene una etiqueta de formato que identifica el formato de audio. (La etiqueta de formato se encuentra en el miembro **wFormatTag** de la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ). En la mayoría de los casos, el origen de medios AVI convierte la etiqueta de formato directamente en un GUID de subtipo, tal y como se describe en el tema [**GUID de subtipo de audio**](audio-subtype-guids.md). En algunos casos, sin embargo, asigna la etiqueta de formato original a otra etiqueta de formato equivalente. Si es así, el origen de medios almacena la etiqueta de formato original en el tipo de medio mediante el \_ \_ atributo de etiqueta de formato de onda original MF MT \_ \_ \_ .

Las asignaciones de formato se almacenan en el registro con la siguiente clave:

**HKEY \_ MediaFoundation \_ raíz de clases** \\  \\ **MapAudioFormatTag**

Cada entrada es un valor **DWORD** . El nombre de la entrada es la representación decimal de la etiqueta de formato. El valor de la entrada es la etiqueta de formato equivalente.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 

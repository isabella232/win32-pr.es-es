---
description: Contiene el objeto FOURCC del códec original para una secuencia de vídeo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: MF_MT_ORIGINAL_4CC atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002626"
---
# <a name="mf_mt_original_4cc-attribute"></a>MF \_ MT \_ original \_ 4cc atributo

Contiene el objeto FOURCC del códec original para una secuencia de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Dependiendo del archivo de origen, el origen de medios AVI podría establecer este atributo en los tipos de medios que ofrece.

Un archivo AVI contiene un encabezado de secuencia para cada flujo del archivo. El origen de medios AVI traduce el encabezado de secuencia en un tipo de medio. En el caso de las secuencias de vídeo comprimidas, el encabezado de flujo contiene un FOURCC que identifica el códec de vídeo. En la mayoría de los casos, el origen de medios AVI convierte este FOURCC directamente en un GUID de subtipo, tal y como se describe en el tema [GUID de subtipo de vídeo](video-subtype-guids.md). En algunos casos, sin embargo, asigna el FOURCC original a otro FOURCC equivalente. Si es así, el origen de medios almacena el FOURCC original en el tipo de medio, mediante el \_ \_ atributo 4cc original MF MT \_ .

Las asignaciones de FOURCC se almacenan en el registro con la siguiente clave:

**HKEY \_ MediaFoundation \_ raíz de clases** \\  \\ **MapVideo4cc**

Cada entrada es un valor **DWORD** . El nombre de la entrada es la representación hexadecimal del FOURCC, sin un prefijo "0x", y con el primer carácter que aparece primero en la cadena. Por ejemplo, el código FOURCC ' abcd ' aparecería como "61626364". El valor de la entrada es el código FOURCC equivalente.

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

 

 





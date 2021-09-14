---
description: Contiene el códec original FOURCC para una secuencia de vídeo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: MF_MT_ORIGINAL_4CC atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363990"
---
# <a name="mf_mt_original_4cc-attribute"></a>Atributo MF \_ MT \_ ORIGINAL \_ 4CC

Contiene el códec original FOURCC para una secuencia de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

Según el archivo de origen, el origen multimedia AVI podría establecer este atributo en los tipos de medios que ofrece.

Un archivo AVI contiene un encabezado de secuencia para cada secuencia del archivo. El origen multimedia AVI traduce el encabezado de secuencia en un tipo de medio. En el caso de las secuencias de vídeo comprimidas, el encabezado de secuencia contiene un FOURCC que identifica el códec de vídeo. En la mayoría de los casos, el origen multimedia AVI convierte este FOURCC directamente en un GUID de subtipo, como se describe en el tema Guid [de subtipo de vídeo](video-subtype-guids.md). En algunos casos, sin embargo, asigna el FOURCC original a otro FOURCC equivalente. Si es así, el origen multimedia almacena el FOURCC original en el tipo de medio, mediante el atributo MF \_ MT \_ ORIGINAL \_ 4CC.

Las asignaciones de FOURCC se almacenan en el Registro con la siguiente clave:

**HKEY \_ CLASSES \_ ROOT** \\ **MediaFoundation** \\ **MapVideo4cc**

Cada entrada es un **valor DWORD.** El nombre de la entrada es la representación hexadecimal de FOURCC, sin un prefijo "0x" y con el primer carácter que aparece primero en la cadena. Por ejemplo, el código FOURCC "abcd" aparecería como "61626364". El valor de la entrada es el código FOURCC equivalente.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 





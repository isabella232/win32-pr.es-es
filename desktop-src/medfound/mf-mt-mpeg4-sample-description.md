---
description: Contiene el cuadro de descripción de ejemplo para un archivo MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741836"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>Atributo MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION

Contiene el cuadro de descripción de ejemplo para un archivo MP4 o 3GP.

## <a name="data-type"></a>Tipo de datos

**Byte\[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

En el cuadro de descripción de ejemplo se describe la codificación utilizada para una secuencia en el archivo .

El origen de archivo MPEG-4 establece este atributo en el tipo de medio para cada secuencia. El valor del atributo son los datos sin procesar del cuadro de descripción de ejemplo. Si el origen del archivo MPEG-4 puede analizar la descripción de ejemplo, también agrega los detalles de formato al tipo de medio. De lo contrario, la aplicación o el descodificador deben analizar la descripción de ejemplo del atributo MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION.

Al establecer este atributo en el receptor MPEG-4 a través del método [**MFMediaTypeHandler::SetCurrentMediaType,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) los datos del atributo MF MT MPEG4 SAMPLE DESCRIPTION no deben cambiar después de que se hayan enviado una o varias muestras al receptor en la interfaz \_ \_ \_ \_ [**DENSink::P rocessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) del flujo correspondiente.

La constante GUID de este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 





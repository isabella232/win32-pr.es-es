---
description: Contiene el cuadro de Descripción del ejemplo para un archivo MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912162"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>\_Atributo de \_ \_ Descripción de muestra MPEG4 \_ de MF MT

Contiene el cuadro de Descripción del ejemplo para un archivo MP4 o 3GP.

## <a name="data-type"></a>Tipo de datos

**BYTES\[\]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Se aplica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Observaciones

El cuadro Descripción del ejemplo describe la codificación utilizada para una secuencia en el archivo.

El origen de archivo MPEG-4 establece este atributo en el tipo de medio para cada flujo. El valor del atributo son los datos sin procesar en el cuadro Descripción del ejemplo. Si el origen de archivo MPEG-4 puede analizar la descripción del ejemplo, también agrega los detalles del formato al tipo de medio. De lo contrario, la aplicación o el descodificador deben analizar la descripción del ejemplo del atributo de Descripción del ejemplo de MF \_ MT \_ MPEG4 \_ \_ .

Al establecer este atributo en el receptor MPEG-4 a través del método [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , los datos del atributo MF \_ MT \_ MPEG4 \_ Sample \_ Description no deben cambiar después de que se hayan enviado una o varias muestras al receptor en la interfaz [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) de la secuencia correspondiente.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 





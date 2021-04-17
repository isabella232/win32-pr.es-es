---
description: Indica el número de búferes sin comprimir que requiere el receptor multimedia del representador de vídeo mejorado (EVR) para Desentrelazar.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: MF_SA_REQUIRED_SAMPLE_COUNT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716347"
---
# <a name="mf_sa_required_sample_count-attribute"></a>Se \_ \_ requiere el \_ atributo de \_ recuento de muestras de MF SA

Indica el número de búferes sin comprimir que requiere el receptor multimedia del representador de vídeo mejorado (EVR) para Desentrelazar.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este es un atributo de nivel de secuencia. Para obtener el atributo de EVR, haga lo siguiente:

1.  Llame a [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) para obtener el receptor de la secuencia.
2.  Consulte el receptor de la secuencia para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Internamente, el mezclador proporciona este atributo a EVR. Para obtener el atributo del mezclador, llame a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 





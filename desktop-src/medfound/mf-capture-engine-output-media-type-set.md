---
description: 'Indica que se ha establecido el tipo de salida en el motor de captura en respuesta a IMFCaptureSink2:: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361928"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>\_Tipo de medio de salida del motor de captura MF \_ atributo de \_ \_ \_ \_ conjunto

Indica que se ha establecido el tipo de salida en el motor de captura en respuesta a [**IMFCaptureSink2:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Puede llamar a [**IMFMediaEvent:: getStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) para averiguar si la operación se realizó correctamente o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 





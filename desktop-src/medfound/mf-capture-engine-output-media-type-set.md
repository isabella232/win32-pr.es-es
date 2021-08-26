---
description: Indica que el tipo de salida se ha establecido en el motor de captura en respuesta a IMFCaptureSink2::SetOutputType.
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138a5893d4ccdd014354e00718a98eda9ba41616c1f1507c8749c9b36dcc0c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013415"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>Atributo SET \_ DE TIPO DE MEDIO DE SALIDA DEL MOTOR DE CAPTURA \_ \_ \_ \_ \_ DE MF

Indica que el tipo de salida se ha establecido en el motor de captura en respuesta a [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Puede llamar a [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) para averiguar si la operación se ha realizado correctamente o no.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 





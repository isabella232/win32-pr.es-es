---
description: Especifica si un descodificador expone tipos de salida IYUV/I420 (adecuados para la transcodificación) antes que otros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872344"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>EL DESCODIFICADOR DE MFT \_ EXPONE LOS TIPOS DE SALIDA EN EL atributo NATIVE \_ \_ \_ \_ \_ \_ ORDER

Especifica si un descodificador expone tipos de salida IYUV/I420 (adecuados para la transcodificación) antes que otros formatos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo es una sugerencia para que el descodificador organice su lista de tipos de salida en un orden determinado, en función del uso previsto, ya sea reproducción o transcodificación.

Para la mayoría de los formatos de codificación (H.264, MPEG-2, WMV), los descodificadores de vídeo de Microsoft Media Foundation admiten varias salidas YUV comunes, como NV12, YV12, YUY2, IYUV e I420. El descodificador ofrece una lista ordenada de tipos de salida a través de [**su método IMFTransform::GetOutputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)

Para la reproducción, NV12 es el formato más eficaz y ampliamente compatible. Por lo tanto, de forma predeterminada, los descodificadores suelen ofrecer NV12 como primer tipo de salida de la lista. Esto minimiza el tiempo necesario para resolver el tipo de medio al crear una topología de reproducción. Sin embargo, para la transcodificación, IYUV o I420 son más eficaces para la CPU y suelen ser preferidos por los codificadores.

Si un descodificador admite este atributo, el atributo tiene el comportamiento siguiente:

-   Si el atributo tiene un valor distinto de cero, IYUV e I420 aparecen primero en la lista de tipos de medios de salida. Esta configuración es más eficaz para la transcodificación.
-   Si el atributo es cero, NV12 aparece primero en la lista de tipos de medios de salida. Esta configuración es más eficaz para la reproducción y es el valor predeterminado.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) el descodificador para obtener un puntero [**DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





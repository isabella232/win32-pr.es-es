---
description: Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812608"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>\_DEScodificador \_ de MFT \_ exponer \_ tipos \_ de salida en el \_ atributo de \_ orden nativo

Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo es una sugerencia para que el descodificador organice su lista de tipos de salida en un orden determinado, en función del uso previsto, ya sea de reproducción o de transcodificación.

Para la mayoría de los formatos de codificación (H. 264, MPEG-2, WMV), los descodificadores de vídeo de Microsoft Media Foundation admiten varias salidas YUV comunes, como NV12, YV12, YUY2, IYUV y i420. El descodificador ofrece una lista ordenada de tipos de salida a través de su método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .

Para la reproducción, NV12 es el formato más eficaz y ampliamente compatible. Por consiguiente, de forma predeterminada, los descodificadores suelen ofrecer NV12 como primer tipo de salida en la lista. Esto minimiza el tiempo necesario para resolver el tipo de medio al compilar una topología de reproducción. Para la transcodificación, sin embargo, IYUV o i420 son más eficaces para la CPU y suelen ser preferidas por los codificadores.

Si un descodificador admite este atributo, el atributo tiene el siguiente comportamiento:

-   Si el atributo tiene un valor distinto de cero, IYUV y i420 aparecen en primer lugar en la lista de tipos de medios de salida. Esta configuración es más eficaz para la transcodificación.
-   Si el atributo es cero, NV12 aparece en primer lugar en la lista de tipos de medios de salida. Esta configuración es la más eficaz para la reproducción y es el valor predeterminado.

Para establecer este atributo:

1.  Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





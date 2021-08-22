---
description: Especifica el número máximo de muestras de salida que una Microsoft Media Foundation transformación (MFT) tendrá pendientes en la canalización en cualquier momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a7d00fcb5a11d756ed4848e3e600a6fd1cca32203ff7234cb01963dfcb5149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663915"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>Atributo MF \_ SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ COUNT

Especifica el número máximo de muestras de salida que una Microsoft Media Foundation transformación (MFT) tendrá pendientes en la canalización en cualquier momento.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo solo se aplica a las MTA que usan un búfer circular para asignar sus propios ejemplos de salida. Otras MTA omiten este atributo.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes en**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) el descodificador para obtener un puntero [**DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 





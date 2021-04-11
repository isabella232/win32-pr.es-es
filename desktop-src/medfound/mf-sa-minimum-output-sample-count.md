---
description: Especifica el número máximo de ejemplos de salida que una transformación de Microsoft Media Foundation (MFT) tendrá pendiente en la canalización en cualquier momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275690"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>\_Atributo de \_ \_ \_ recuento de ejemplo de salida mínima de SA de MF \_

Especifica el número máximo de ejemplos de salida que una transformación de Microsoft Media Foundation (MFT) tendrá pendiente en la canalización en cualquier momento.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo solo se aplica a MFTs que usan un búfer circular para asignar sus propios ejemplos de salida. Otros MFTs omiten este atributo.

Para establecer este atributo:

1.  Llame a [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el descodificador para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para agregar el atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 





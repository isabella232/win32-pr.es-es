---
description: Indica el número mínimo de muestras progresivas que la transformación de Microsoft Media Foundation (MFT) debe permitir que se pendientes en un momento dado.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277683"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>Recuento de \_ \_ muestras de salida mínimas \_ de \_ \_ MF SA \_

Indica el número mínimo de muestras progresivas que la transformación de Microsoft Media Foundation (MFT) debe permitir que se pendientes en un momento dado.

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
</dt> </dl>

 

 





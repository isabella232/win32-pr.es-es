---
description: Especifica cuántos búferes crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6b54cc5b2589649c954d9f2f41923af04fdf4aa7c00714067bee0b11dabbee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740372"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>Atributo MF \_ SA \_ BUFFERS \_ PER \_ SAMPLE

Especifica cuántos búferes crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Si usa la interfaz [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar ejemplos de vídeo, puede usar este atributo para crear ejemplos de vídeo que contengan varios búferes. Por ejemplo, si el valor del atributo es 2, el asignador crea dos búferes de vídeo para cada ejemplo de vídeo. Establezca el atributo en el *parámetro pAttributes* del método [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

El valor predeterminado es 1. Si no se establece el atributo, el asignador crea ejemplos de vídeo que contienen un único búfer por muestra.

Este atributo está pensado principalmente para transformaciones Media Foundation (MTA) que admiten la salida 3D estéreo, en la siguiente situación:

-   MFT admite Microsoft Infraestructura de gráficos de DirectX (DXGI).
-   MFT asigna sus propios ejemplos de salida.
-   El MFT usa la [**interfaz IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar los ejemplos de salida.
-   El formato de vídeo 3D usa un búfer independiente para cada vista.

Si todos estos criterios son true, MFT debe establecer el valor del atributo en 2 (un búfer por vista).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





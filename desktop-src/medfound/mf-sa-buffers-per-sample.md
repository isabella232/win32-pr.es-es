---
description: Especifica el número de búferes que crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811030"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>\_Búferes de SA MF \_ \_ por \_ atributo de ejemplo

Especifica el número de búferes que crea el asignador de ejemplo de vídeo para cada ejemplo de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Si usa la interfaz [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar ejemplos de vídeo, puede usar este atributo para crear ejemplos de vídeo que contengan varios búferes. Por ejemplo, si el valor del atributo es 2, el asignador crea dos búferes de vídeo para cada ejemplo de vídeo. Establezca el atributo en el parámetro *pAttributes* del método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

El valor predeterminado es 1. Si no se establece el atributo, el asignador crea muestras de vídeo que contienen un solo búfer por muestra.

Este atributo está pensado principalmente para Media Foundation transformaciones (MFTs) que admiten la salida 3D estéreo en la situación siguiente:

-   MFT es compatible con Microsoft DirectX Graphics Infrastructure (DXGI).
-   La MFT asigna sus propios ejemplos de salida.
-   MFT usa la interfaz [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) para asignar los ejemplos de salida.
-   El formato de vídeo 3D utiliza un búfer independiente para cada vista.

Si todos estos criterios son verdaderos, el MFT debe establecer el valor del atributo en 2 (un búfer por vista).

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

 

 





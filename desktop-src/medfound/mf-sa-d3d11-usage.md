---
description: Especifica cómo asignar superficies de Microsoft Direct3D 11 para ejemplos multimedia.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7364b9777d94baa1a6c25aead6631ad6b11dcddc12db83698da04affebe0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663955"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>Atributo MF \_ SA \_ D3D11 \_ USAGE

Especifica cómo asignar superficies de Microsoft Direct3D 11 para ejemplos multimedia. El uso refleja directamente si una CPU o GPU puede acceder a un ejemplo.

## <a name="data-type"></a>Tipo de datos

**D3D11 \_ USAGE** almacenado como **UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un [**valor \_ USAGE de D3D11.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation transformaciones

En este contexto, el atributo solo se aplica cuando la transformación de Microsoft Media Foundation (MFT) devuelve **TRUE** para el atributo [MF SA \_ \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)

Si un MFT admite Direct3D 11, este atributo proporciona una sugerencia a MFT al asignar superficies de Microsoft Direct3D para la salida. Establezca el atributo de la manera siguiente:

1.  Llame [**a IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obtener el almacén de atributos MFT.
2.  Llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La canalización Media Foundation establece el atributo antes de que se inicie el streaming. El MFT debe intentar respetar la configuración cuando asigna superficies. Si esto no es posible, MFT puede omitir el atributo, en lugar de dar error a la asignación.

Además, si MFT requiere superficies de Direct3D para la entrada, puede exponer este atributo como una sugerencia para cómo se deben asignar las superficies de entrada. Consulte el atributo como se muestra a continuación:

1.  Llame [**a IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obtener los atributos de flujo de entrada.
2.  Llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Asignador de ejemplo

Este atributo se puede establecer en el asignador de ejemplo de vídeo, en el [**método IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

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

 

 

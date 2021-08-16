---
description: Especifica las marcas de enlace que se usarán al asignar superficies de Microsoft Direct3D 11 para ejemplos multimedia.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65f0fbc607ccdc8f878e25109fcadfdf8956007d99909d9a21c0e668951106d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102468"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>Atributo \_ \_ \_ BINDFLAGS de MF SA D3D11

Especifica las marcas de enlace que se usarán al asignar superficies de Microsoft Direct3D 11 para ejemplos multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un **OR** bit a bit de marcas BIND FLAG de [**\_ \_ D3D11.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation transformaciones

En este contexto, el atributo solo se aplica cuando la transformación de Microsoft Media Foundation (MFT) devuelve **TRUE** para el atributo [MF SA \_ \_ D3D11 \_ AWARE.](mf-sa-d3d11-aware.md)

Si un MFT admite Direct3D 11, este atributo proporciona una sugerencia a MFT al asignar superficies de Microsoft Direct3D para la salida. Establezca el atributo de la manera siguiente:

1.  Llame [**a IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obtener el almacén de atributos MFT.
2.  Llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La canalización Media Foundation establece el atributo antes de que se inicie el streaming. El MFT debe intentar respetar la configuración cuando asigna superficies. Si esto no es posible, MFT puede omitir el atributo, en lugar de dar error a la asignación.

Además, si MFT requiere superficies de Direct3D para la entrada, puede exponer este atributo como una sugerencia sobre cómo se deben asignar las superficies de entrada. Consulte el atributo como se muestra a continuación:

1.  Llame [**a IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obtener los atributos de flujo de entrada.
2.  Llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Asignador de ejemplo

Este atributo se puede establecer en el asignador de ejemplo de vídeo, en el [**método IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx.**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

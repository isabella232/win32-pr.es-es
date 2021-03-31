---
description: Especifica las marcas de enlace que se van a usar al asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360766"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>MF \_ SA \_ D3D11 \_ BINDFLAGS atributo

Especifica las marcas de enlace que se van a usar al asignar las superficies de Microsoft Direct3D 11 para los ejemplos de medios.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es **una operación OR bit a bit** de marcas de [**\_ \_ marcador de enlace D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) .

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation transformaciones

En este contexto, el atributo solo se aplica cuando la transformación de Microsoft Media Foundation (MFT) devuelve **true** para el atributo de [ \_ reconocimiento de SA \_ \_ D3D11 de MF](mf-sa-d3d11-aware.md) .

Si una MFT es compatible con Direct3D 11, este atributo proporciona una sugerencia a la MFT al asignar las superficies de Microsoft Direct3D para la salida. Establezca el atributo de la siguiente manera:

1.  Llame a [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) para obtener el almacén de atributos de MFT.
2.  Llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

La canalización Media Foundation establece el atributo antes de que se inicie el streaming. La MFT debe intentar respetar la configuración cuando asigna superficies. Si eso no es posible, el MFT puede omitir el atributo, en lugar de generar un error en la asignación.

Además, si la MFT requiere superficies de Direct3D para la entrada, puede exponer este atributo como una sugerencia sobre cómo se deben asignar las superficies de entrada. Consulte el atributo como se indica a continuación:

1.  Llame a [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) para obtener los atributos del flujo de entrada.
2.  Llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Asignador de ejemplo

Este atributo se puede establecer en el asignador de ejemplo de vídeo, en el método [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .

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

 

 

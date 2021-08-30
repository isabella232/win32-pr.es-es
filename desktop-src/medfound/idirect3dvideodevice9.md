---
description: Habilita la descodización acelerada por hardware desde un dispositivo Direct3D 9 mediante DirectX Video Acceleration (DXVA) versión 1.0.
ms.assetid: abe3beac-f3f8-413d-8b83-9da3340b19ac
title: Interfaz IDirect3DVideoDevice9 (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 7dca1db868b4b268e71175f8f44aa198a6ebb45c8a14f8bfc1bec7044d5545f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958215"
---
# <a name="idirect3dvideodevice9-interface"></a>Interfaz IDirect3DVideoDevice9

Habilita la descodización acelerada por hardware desde un dispositivo Direct3D 9 mediante DirectX Video Acceleration (DXVA) versión 1.0.

## <a name="when-to-use"></a>Cuándo se usa

Esta interfaz no está pensada para el uso general de la aplicación. DirectShow de descodificador deben usar la [**interfaz IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) no **IDirect3DVideoDevice9**. Los pines de entrada del filtro Representador de mezcla de vídeo (VMR) y el filtro overlay Mixer exponen **IAMVideoAccelerator.**

## <a name="members"></a>Miembros

La **interfaz IDirect3DVideoDevice9** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDirect3DVideoDevice9** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDirect3DVideoDevice9** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                       |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md)                       | Crea un dispositivo descodificador DXVA.<br/>                                                                                         |
| [**CreateSurface**](idirect3dvideodevice9-createsurface.md)                             | Crea una superficie comprimida para la decodificación de DXVA.<br/>                                                                        |
| [**GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) | Obtiene información sobre los búferes comprimidos necesarios para lacodización acelerada por hardware.<br/>                                |
| [**GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)                               | Obtiene una lista de los perfiles de DXVA admitidos por el controlador para mostrar.<br/>                                             |
| [**GetDXVAInternalInfo**](idirect3dvideodevice9-getdxvainternalinfo.md)                 | Consulta la cantidad de memoria cero que asignará la capa de abstracción de hardware (LOD) para su uso privado. <br/> |
| [**GetUncompressedDXVAFormats**](idirect3dvideodevice9-getuncompresseddxvaformats.md)   | Obtiene una lista de formatos de píxeles sin comprimir que se pueden representar mediante un perfil DXVA especificado.<br/>                         |



 

## <a name="remarks"></a>Comentarios

Para obtener un puntero a esta interfaz, llame a **QueryInterface** en un [**puntero IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) [**o IDirect3DDevice9Ex.**](/windows/win32/api/d3d9/nn-d3d9-idirect3ddevice9ex)

Esta interfaz solo admite DXVA 1.0. No admite DXVA 2.0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de vídeo de Direct3D](direct3d-video-interfaces.md)
</dt> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Especificación dxva 1.0](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 

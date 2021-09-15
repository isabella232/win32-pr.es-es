---
description: Los siguientes GUID admiten las API de vídeo de Direct3D 12.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID de vídeo de Direct3D 12 (D3d11.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05f7a56227ccc2953504d8466a34d6b2160ce1e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574941"
---
# <a name="direct3d-12-video-guids"></a>GUID de vídeo de Direct3D 12

Los siguientes GUID admiten las API de vídeo de Direct3D 12.

## <a name="d3d12_video_decode_profile-guids"></a>GUID de _VIDEO \\ _DECODE _PROFILE D3D12 \\ \\

En la tabla siguiente se enumeran los GUID que identifican perfiles de decoding de vídeo de Direct3D 12. Las descripciones relacionan cada perfil de descodificación de vídeo de Direct3D 12 con el vídeo equivalente de Direct3D 11 o el perfil DXVA.

| Nombre                                                 | Value                                                                                | Descripción
|------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| D3D12 \_ VIDEO \_ DECODE PROFILE \_ \_ MPEG1 Y \_ \_ MPEG2           | 0x86695f12, 0x340e, 0x4f04, 0x9f, 0xd3, 0x92, 0x53, 0xdd, 0x32, 0x74, 0x60 | Equivalente a DXVA2 \_ ModeMPEG2and1 \_ VLD.                 |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ MPEG2                     | 0xee27417f, 0x5e28, 0x4e65, 0xbe, 0xea, 0x1d, 0x26, 0xb5, 0x08, 0xad, 0xc9           | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG2 \_ VLD y DXVA2 \_ ModeMPEG2 \_ VLD.                 |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ H264                      | 0x1b81be68, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5       | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD \_ NOFGT y DXVA \_ ModeH264 \_ VLD \_ NoFGT. |
| DESCODIFICACIÓN DE VÍDEO D3D12 \_ \_ PERFIL \_ \_ H264 \_ ESTÉREO \_ PROGRESIVA   | 0xd79be8da, 0x0cf1, 0x4c81, 0xb8, 0x2a, 0x69, 0xa4, 0xe2, 0x36, 0xf4, 0x3d          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD STEREO PROGRESSIVE \_ NOFGT y \_ \_ DXVA \_ ModeH264 \_ VLD Stereo Progressive \_ \_ \_ NoFGT. |
| DESCODIFICACIÓN DE VÍDEO D3D12 \_ \_ PERFIL \_ \_ H264 \_ ESTÉREO               | 0xf9aaccbb, 0xc2b6, 0x4cfc, 0x87, 0x79, 0x57, 0x07, 0xb1, 0x76, 0x05, 0x52          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD STEREO \_ \_ NOFGT y DXVA \_ ModeH264 \_ VLD Stereo \_ \_ NoFGT |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ H264 \_ MULTIVIEW            | 0x705b9d82, 0x76cf, 0x49d6, 0xb7, 0xe6, 0xac, 0x88, 0x72, 0xdb, 0x01, 0x3c          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ H264 \_ VLD \_ MULTIVIEW NOFGT y \_ DXVA \_ ModeH264 \_ VLD \_ Multiview \_ NoFGT. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ VC1                       | 0x1b81beA3, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ VC1 \_ VLD y DXVA \_ ModeVC1 \_ VLD. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ VC1 \_ D2010                 | 0x1b81beA4, 0xa0c7, 0x11d3, 0xb9, 0x84, 0x00, 0xc0, 0x4f, 0x2e, 0x73, 0xc5          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ VC1 \_ D2010 y DXVA \_ ModeVC1 \_ D2010. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ MPEG4PT2 \_ SIMPLE           | 0xefd64d74, 0xc9e8, 0x41d7, 0xa5, 0xe9, 0xe9, 0xb0, 0xe3, 0x9f, 0xa3, 0x19          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG4PT2 VLD SIMPLE y \_ \_ DXVA \_ ModeMPEG4pt2 \_ VLD \_ Simple. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ MPEG4PT2 \_ ADVSIMPLE \_ NOGMC  | 0xed418a9f, 0x010d, 0x4eda, 0x9a, 0xe3, 0x9a, 0x65, 0x35, 0x8d, 0x8d, 0x2e          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ MPEG4PT2 \_ VLD \_ ADVSIMPLE \_ NOGMC y DXVA \_ ModeMPEG4pt2 \_ VLD \_ AdvSimple \_ NoGMC. |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ HEVC \_ MAIN                 | 0x5b11d51b, 0x2f4c, 0x4452, 0xbc, 0xc3, 0x09, 0xf2, 0xa1, 0x16, 0x0c, 0xc0          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ HEVC \_ VLD MAIN y \_ DXVA \_ ModeHEVC \_ VLD \_ Main
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ HEVC \_ MAIN10               | 0x107af0e0, 0xef1a, 0x4d19, 0xab, 0xa8, 0x67, 0xa1, 0x63, 0x07, 0x3d, 0x13          | Equivalente a D3D11 \_ DECODER \_ PROFILE \_ HEVC \_ VLD \_ MAIN10 y DXVA \_ ModeHEVC \_ VLD \_ Main10.
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ VP9                       | 0x463707f8, 0xa1d0, 0x4585, 0x87, 0x6d, 0x83, 0xaa, 0x6d, 0x60, 0xb8, 0x9e | |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ VP9 \_ 10BIT \_ PROFILE2        | 0xa4c749ef, 0x6ecf, 0x48aa, 0x84, 0x48, 0x50, 0xa7, 0xa1, 0x16, 0x5f, 0xf7           | |
| D3D12 \_ VIDEO \_ DECODE \_ PROFILE \_ VP8                       | 0x90b899ea, 0x3a62, 0x4705, 0x88, 0xb3, 0x8d, 0xf0, 0x4b, 0x27, 0x44, 0xe7 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE0                       | 0xb8be4ccb, 0xcf53, 0x46ba, 0x8d, 0x59, 0xd6, 0xb8, 0xa6, 0xda, 0x5d, 0x2a | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE1                       | 0x6936ff0f, 0x45b1, 0x4163, 0x9c, 0xc1, 0x64, 0x6e, 0xf6, 0x94, 0x61, 0x08 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_PROFILE2                       | 0x0c5f2aa1, 0xe541, 0x4089, 0xbb, 0x7b, 0x98, 0x11, 0x0a, 0x19, 0xd7, 0xc8 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2                 | 0x17127009, 0xa00f, 0x4ce1, 0x99, 0x4e, 0xbf, 0x40, 0x81, 0xf6, 0xf3, 0xf0 | |
| D3D12_VIDEO_DECODE_PROFILE_AV1_12BIT_PROFILE2_420             | 0x2d80bed6, 0x9cac, 0x4835, 0x9e, 0x91, 0x32, 0x7b, 0xbc, 0x4f, 0x9e, 0xe8 | |

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 





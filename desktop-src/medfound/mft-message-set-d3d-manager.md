---
description: Establece o borra el valor de Direct3D Administrador de dispositivos para la a acceración de vídeo de DirectX (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0e7ccbf9f28615b17e6acded6ecc932334b4fb0fa4a607d6fd6213ba2cd214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848075"
---
# <a name="mft_message_set_d3d_manager"></a>MFT \_ MESSAGE \_ SET \_ D3D \_ MANAGER

Establece o borra la configuración [de Direct3D Administrador de dispositivos](direct3d-device-manager.md) la a acceración de vídeo de DirectX (DXVA).

## <a name="message-parameter"></a>Parámetro message

Cuando comienza el streaming, *el parámetro ulParam* contiene un **puntero IUnknown.** El MFT consultará este puntero para la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) para Direct3D 9 y la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) para Direct3D 11. Cuando se detiene el streaming, *ulParameter* contiene el valor **NULL.**

## <a name="remarks"></a>Comentarios

Para enviar este mensaje, llame [**a IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Este mensaje solo se aplica a las transformaciones de vídeo. El cliente no debe enviar este mensaje a menos que MFT devuelva **TRUE** para el atributo [**MF SA \_ \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) [(MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) para Direct3D 11).

No envíe este mensaje a un MFT con varias unidades organizativas.

### <a name="implementation"></a>Implementación

Un MFT solo debe admitir este mensaje si MFT usa la aceleración de vídeo directX para el procesamiento o lacodización de vídeo.

Si un MFT admite este mensaje, también debe implementar el método [**MFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) y devolver el valor **TRUE** para el atributo [**MF SA \_ \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) (([MF SA \_ \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) for Direct3D 11). Este atributo informa al cliente de que el cliente debe enviar el mensaje **MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER** al MFT antes de comenzar el streaming.

Si un MFT no admite este mensaje, debe devolver **E \_ NOTIMPL** desde [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Se trata de una excepción a la regla general de que un MFT puede devolver **S \_ OK** desde cualquier mensaje que ignore.

Para obtener más información, [vea Direct3D-Aware MFT](direct3d-aware-mfts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MTA con direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Compatibilidad con DXVA 2.0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Compatibilidad con la decodificación de vídeo de Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**TIPO DE \_ MENSAJE \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 





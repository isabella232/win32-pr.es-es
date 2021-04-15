---
description: Establece o borra el Administrador de dispositivos de Direct3D para DirectX video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715789"
---
# <a name="mft_message_set_d3d_manager"></a>\_ \_ Administrador D3D de conjunto de mensajes de \_ MFT \_

Establece o borra el [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) para DirectX video ACCERERATION (DXVA).

## <a name="message-parameter"></a>Parámetro de mensaje

Cuando se inicia el streaming, el parámetro *ulParam* contiene un puntero **IUnknown** . La MFT consultará este puntero para la interfaz [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) para Direct3D 9 y la interfaz [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) para Direct3D 11. Cuando se detiene el streaming, *ulParameter* contiene el valor **null**.

## <a name="remarks"></a>Observaciones

Para enviar este mensaje, llame a [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Este mensaje se aplica solo a las transformaciones de vídeo. El cliente no debe enviar este mensaje a menos que la MFT devuelva el **valor true** para el atributo [**MF \_ SA \_ \_ compatible**](mf-sa-d3d-aware-attribute.md) con el D3D ([MF \_ SA \_ D3D11 \_ compatible](mf-sa-d3d11-aware.md) con Direct3D 11).

No envíe este mensaje a una MFT con varios genera.

### <a name="implementation"></a>Implementación

Un MFT solo debe admitir este mensaje si MFT usa la aceleración de vídeo de DirectX para el procesamiento o la descodificación de vídeo.

Si un MFT es compatible con este mensaje, también debe implementar el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) y devolver el valor **true** para el atributo MF de ([MF \_ SA \_ D3D11 \_](mf-sa-d3d11-aware.md) para Direct3D 11). [**\_ \_ \_**](mf-sa-d3d-aware-attribute.md) Este atributo informa al cliente de que el cliente debe enviar el mensaje **de \_ \_ Administrador de \_ D3D \_ del conjunto de mensajes de MFT** a la MFT antes de comenzar la transmisión por secuencias.

Si una MFT no admite este mensaje, debe devolver **E \_ NOTIMPL** desde [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Esta es una excepción a la regla general de que una MFT puede devolver **S \_ correcto** desde cualquier mensaje que omita.

Para obtener más información, consulte [MFTs compatible con Direct3D](direct3d-aware-mfts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MFTs compatible con Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Compatibilidad con DXVA 2,0 en Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Compatibilidad con la descodificación de vídeo Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_tipo de mensaje de MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 





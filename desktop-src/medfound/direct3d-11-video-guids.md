---
description: Los siguientes GUID admiten las API de vídeo de Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID de vídeo de Direct3D 11 (D3d11.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905621e26edcc149d456d5d7b4ef7294ae39c80ae35955e9a19902484d5ff5eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346475"
---
# <a name="direct3d-11-video-guids"></a>GUID de vídeo de Direct3D 11

Los siguientes GUID admiten las API de vídeo de Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION**
</dt> <dd> <dl> <dt>



Indica que el descodificador recibirá datos de un componente DRM basado en hardware.

**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION** se puede especificar en el parámetro *pKeyExchangeType* de la función [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que la interfaz [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) se usará exclusivamente para la comunicación entre un componente DRM en modo de usuario y el entorno de ejecución segura.

Cuando se especifica este GUID, no se debe llamar a los métodos siguientes:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ DECODER \_ ENCRYPTION \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



Indica que el descodificador recibirá datos de un componente DRM basado en hardware.

Establecer este GUID en el miembro **guidConfigBitstreamEncryption** de la estructura DE CONFIGURACIÓN [**D3D11 \_ VIDEO \_ DECODER \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) pasada a la API [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica que se pasarán los parámetros siguientes en la llamada [**ID3D11VideoDevice::D ecoderBeginFrame:**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)



| Valor                 | Descripción                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contiene el tamaño de la estructura [**BEGIN \_ FRAME CRYPTO \_ \_ \_ \_ \_ SESSION del DESCODIFICADOR DE VÍDEO D3D11.**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)                                                                                                  |
| *pContentKey*    | Puntero a [**D3D11 \_ VIDEO DECODER BEGIN FRAME CRYPTO \_ \_ \_ \_ \_ SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) que proporciona [**id3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) y la información clave necesaria para descifrar el fotograma. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 





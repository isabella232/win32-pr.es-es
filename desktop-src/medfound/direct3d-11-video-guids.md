---
description: Los siguientes GUID admiten las API de vídeo de Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUID de vídeo de Direct3D 11 (D3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080319"
---
# <a name="direct3d-11-video-guids"></a>GUID de vídeo de Direct3D 11

Los siguientes GUID admiten las API de vídeo de Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Protección de \_ hardware de intercambio de claves de D3D11 \_ \_**
</dt> <dd> <dl> <dt>



Indica que el descodificador recibirá datos de un componente DRM basado en hardware

**D3D11 \_ La \_ \_ \_ protección de hardware de intercambio de claves** se puede especificar en el parámetro *pKeyExchangeType* de la función [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que la interfaz [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) se usará únicamente para la comunicación entre un componente DRM de modo de usuario y el entorno de ejecución seguro.

Cuando se especifica este GUID, no se debe llamar a los siguientes métodos:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 de \_ cifrado de DEScodificador de \_ \_ hardware \_ Cenc**
</dt> <dd> <dl> <dt>



Indica que el descodificador recibirá datos de un componente DRM basado en hardware

El establecimiento de este GUID en el miembro **guidConfigBitstreamEncryption** de la estructura de [**\_ \_ \_ configuración del descodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) que se pasa a la API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica que los siguientes parámetros se pasarán en la llamada [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contiene el tamaño de la estructura de la [**\_ \_ sesión de \_ \_ \_ CIFRAdo \_ de inicio del descodificador de vídeo D3D11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *pContentKey*    | Un puntero a un [**\_ descodificador de vídeo de D3D11 \_ \_ iniciar \_ \_ \_ sesión de cifrado de fotogramas**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) que proporciona el [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) y la información de clave necesaria para descifrar el marco. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 





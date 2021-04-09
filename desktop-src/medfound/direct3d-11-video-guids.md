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
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="bbd08-103">GUID de vídeo de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bbd08-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="bbd08-104">Los siguientes GUID admiten las API de vídeo de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="bbd08-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="bbd08-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Protección de \_ hardware de intercambio de claves de D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bbd08-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bbd08-106">Indica que el descodificador recibirá datos de un componente DRM basado en hardware</span><span class="sxs-lookup"><span data-stu-id="bbd08-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="bbd08-107">**D3D11 \_ La \_ \_ \_ protección de hardware de intercambio de claves** se puede especificar en el parámetro *pKeyExchangeType* de la función [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que la interfaz [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) se usará únicamente para la comunicación entre un componente DRM de modo de usuario y el entorno de ejecución seguro.</span><span class="sxs-lookup"><span data-stu-id="bbd08-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="bbd08-108">Cuando se especifica este GUID, no se debe llamar a los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="bbd08-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="bbd08-109">**ID3D11CryptoSession::GetCertificateSize**</span><span class="sxs-lookup"><span data-stu-id="bbd08-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="bbd08-110">**ID3D11CryptoSession:: GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="bbd08-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="bbd08-111">**ID3D11VideoContext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="bbd08-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="bbd08-112">**ID3D11VideoContext::D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="bbd08-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="bbd08-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="bbd08-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="bbd08-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="bbd08-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="bbd08-115">**ID3D11VideoContext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="bbd08-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="bbd08-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 de \_ cifrado de DEScodificador de \_ \_ hardware \_ Cenc**</span><span class="sxs-lookup"><span data-stu-id="bbd08-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bbd08-117">Indica que el descodificador recibirá datos de un componente DRM basado en hardware</span><span class="sxs-lookup"><span data-stu-id="bbd08-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="bbd08-118">El establecimiento de este GUID en el miembro **guidConfigBitstreamEncryption** de la estructura de [**\_ \_ \_ configuración del descodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) que se pasa a la API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica que los siguientes parámetros se pasarán en la llamada [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :</span><span class="sxs-lookup"><span data-stu-id="bbd08-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd08-119">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="bbd08-119">*ContentKeySize*</span></span> | <span data-ttu-id="bbd08-120">Contiene el tamaño de la estructura de la [**\_ \_ sesión de \_ \_ \_ CIFRAdo \_ de inicio del descodificador de vídeo D3D11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="bbd08-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="bbd08-121">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="bbd08-121">*pContentKey*</span></span>    | <span data-ttu-id="bbd08-122">Un puntero a un [**\_ descodificador de vídeo de D3D11 \_ \_ iniciar \_ \_ \_ sesión de cifrado de fotogramas**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) que proporciona el [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) y la información de clave necesaria para descifrar el marco.</span><span class="sxs-lookup"><span data-stu-id="bbd08-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbd08-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbd08-123">Requirements</span></span>



| <span data-ttu-id="bbd08-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbd08-124">Requirement</span></span> | <span data-ttu-id="bbd08-125">Value</span><span class="sxs-lookup"><span data-stu-id="bbd08-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd08-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbd08-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd08-127">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbd08-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbd08-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbd08-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd08-129">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbd08-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bbd08-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bbd08-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbd08-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbd08-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd08-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbd08-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd08-133">API de vídeo de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bbd08-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 





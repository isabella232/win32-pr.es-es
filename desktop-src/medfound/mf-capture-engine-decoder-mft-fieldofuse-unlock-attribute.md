---
description: Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715654"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="1cdd7-103">\_Módulo de captura MF \_ \_ descodificador de \_ MFT \_ FIELDOFUSE \_ Unlock \_ Attribute atributo</span><span class="sxs-lookup"><span data-stu-id="1cdd7-103">MF\_CAPTURE\_ENGINE\_DECODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="1cdd7-104">Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="1cdd7-104">Enables the capture engine to use a decoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="1cdd7-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1cdd7-105">Data type</span></span>

<span data-ttu-id="1cdd7-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="1cdd7-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="1cdd7-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cdd7-107">Remarks</span></span>

<span data-ttu-id="1cdd7-108">El valor de este atributo es un puntero a la interfaz [_ *IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="1cdd7-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="1cdd7-109">Se espera que la implementación del llamador de esta interfaz realice un protocolo de enlace con el descodificador, tal y como se describe en el [campo de restricciones de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="1cdd7-109">The caller's implementation of this interface is expected to perform a handshake with the decoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="1cdd7-110">Microsoft Media Foundation no define el protocolo de enlace, normalmente implicaría algún tipo de intercambio criptográfico.</span><span class="sxs-lookup"><span data-stu-id="1cdd7-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="1cdd7-111">Internamente, el motor de captura establece el puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) en el descodificador estableciendo el atributo [MFT \_ FIELDOFUSE \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) del descodificador.</span><span class="sxs-lookup"><span data-stu-id="1cdd7-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the decoder by setting the decoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cdd7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cdd7-112">Requirements</span></span>



| <span data-ttu-id="1cdd7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cdd7-113">Requirement</span></span> | <span data-ttu-id="1cdd7-114">Value</span><span class="sxs-lookup"><span data-stu-id="1cdd7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cdd7-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cdd7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1cdd7-116">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cdd7-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1cdd7-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cdd7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1cdd7-118">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1cdd7-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1cdd7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cdd7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cdd7-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cdd7-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cdd7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cdd7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cdd7-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1cdd7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1cdd7-123">Atributos del motor de captura</span><span class="sxs-lookup"><span data-stu-id="1cdd7-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1cdd7-124">**IMFCaptureEngine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1cdd7-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 





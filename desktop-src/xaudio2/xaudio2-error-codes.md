---
description: Códigos de error específicos de XAudio2 devueltos por los métodos de XAudio2.
ms.assetid: 42a1c21c-4b14-114a-d79e-15a61eb2139b
title: Códigos de error de XAudio2 (xaudio2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7011786c3db7f660dee7a3323861abd88c57835
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700184"
---
# <a name="xaudio2-error-codes"></a><span data-ttu-id="ef8e4-103">Códigos de error de XAudio2</span><span class="sxs-lookup"><span data-stu-id="ef8e4-103">XAudio2 Error Codes</span></span>

<span data-ttu-id="ef8e4-104">Códigos de error específicos de XAudio2 devueltos por los métodos de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="ef8e4-104">XAudio2 specific error codes returned by XAudio2 methods.</span></span>



| <span data-ttu-id="ef8e4-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="ef8e4-105">Constant/value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="ef8e4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef8e4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XAUDIO2_E_INVALID_CALL"></span><span id="xaudio2_e_invalid_call"></span><dl> <span data-ttu-id="ef8e4-107"><dt>**XAUDIO2 \_ E \_ \_ llamada no válida**</dt> <dt>0x88960001</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e4-107"><dt>**XAUDIO2\_E\_INVALID\_CALL**</dt> <dt>0x88960001</dt></span></span> </dl>                          | <span data-ttu-id="ef8e4-108">Lo devuelve XAudio2 para ciertos errores de uso de la API (llamadas no válidas, etc.) que son difíciles de evitar completamente y deben controlarse mediante un título en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ef8e4-108">Returned by XAudio2 for certain API usage errors (invalid calls and so on) that are hard to avoid completely and should be handled by a title at runtime.</span></span> <span data-ttu-id="ef8e4-109">(Los errores de uso de la API que son completamente evitables, como los parámetros no válidos, causan una ASERCIÓN en las compilaciones de depuración y el comportamiento indefinido en las compilaciones comerciales, por lo que no se define ningún código de error para ellos)</span><span class="sxs-lookup"><span data-stu-id="ef8e4-109">(API usage errors that are completely avoidable, such as invalid parameters, cause an ASSERT in debug builds and undefined behavior in retail builds, so no error code is defined for them.)</span></span><br/> |
| <span id="XAUDIO2_E_XMA_DECODER_ERROR"></span><span id="xaudio2_e_xma_decoder_error"></span><dl> <span data-ttu-id="ef8e4-110"><dt>**XAUDIO2 \_ E \_ XMA \_ \_ error del descodificador**</dt> <dt>0x88960002</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e4-110"><dt>**XAUDIO2\_E\_XMA\_DECODER\_ERROR**</dt> <dt>0x88960002</dt></span></span> </dl>          | <span data-ttu-id="ef8e4-111">Se produjo un error irrecuperable en el hardware de XMA de Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="ef8e4-111">The Xbox 360 XMA hardware suffered an unrecoverable error.</span></span><br/>                                                                                                                                                                                                                                                                                             |
| <span id="XAUDIO2_E_XAPO_CREATION_FAILED"></span><span id="xaudio2_e_xapo_creation_failed"></span><dl> <span data-ttu-id="ef8e4-112"><dt>**XAUDIO2 \_ \_ \_ \_ Error**</dt> en la creación de XAPO <dt>0x88960003</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e4-112"><dt>**XAUDIO2\_E\_XAPO\_CREATION\_FAILED**</dt> <dt>0x88960003</dt></span></span> </dl> | <span data-ttu-id="ef8e4-113">No se pudo crear una instancia de un efecto.</span><span class="sxs-lookup"><span data-stu-id="ef8e4-113">An effect failed to instantiate.</span></span><br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="XAUDIO2_E_DEVICE_INVALIDATED"></span><span id="xaudio2_e_device_invalidated"></span><dl> <span data-ttu-id="ef8e4-114"><dt>**XAUDIO2 \_ \_Dispositivo E \_ invalidado**</dt> <dt>0x88960004</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e4-114"><dt>**XAUDIO2\_E\_DEVICE\_INVALIDATED**</dt> <dt>0x88960004</dt></span></span> </dl>        | <span data-ttu-id="ef8e4-115">Un dispositivo de audio dejó de ser utilizable a través de desenchufado o algún otro evento.</span><span class="sxs-lookup"><span data-stu-id="ef8e4-115">An audio device became unusable through being unplugged or some other event.</span></span><br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="ef8e4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef8e4-116">Remarks</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ef8e4-117">Requisitos de la plataforma</span><span class="sxs-lookup"><span data-stu-id="ef8e4-117">Platform Requirements</span></span>

<span data-ttu-id="ef8e4-118">Windows 10 (XAudio 2.9); Windows 8, Windows Phone 8 (XAudio 2,8); SDK de DirectX (XAudio 2,7)</span><span class="sxs-lookup"><span data-stu-id="ef8e4-118">Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8e4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef8e4-119">Requirements</span></span>



| <span data-ttu-id="ef8e4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef8e4-120">Requirement</span></span> | <span data-ttu-id="ef8e4-121">Value</span><span class="sxs-lookup"><span data-stu-id="ef8e4-121">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8e4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef8e4-122">Header</span></span><br/> | <dl> <span data-ttu-id="ef8e4-123"><dt>Xaudio2. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef8e4-123"><dt>Xaudio2.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8e4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef8e4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8e4-125">XAudio2:: constantes</span><span class="sxs-lookup"><span data-stu-id="ef8e4-125">XAudio2::Constants</span></span>](constants.md)
</dt> </dl>

 

 





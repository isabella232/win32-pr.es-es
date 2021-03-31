---
title: Propiedad AudioCaptureRedirectionMode de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor booleano que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioCaptureRedirectionMode
- Propiedad AudioCaptureRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AudioCaptureRedirectionMode
- Propiedad AudioCaptureRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996598"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="34048-108">IMsRdpClientAdvancedSettings7:: AudioCaptureRedirectionMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="34048-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="34048-109">Especifica o recupera un valor booleano que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="34048-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="34048-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="34048-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="34048-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34048-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="34048-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="34048-112">Property value</span></span>

<span data-ttu-id="34048-113">Un **valor \_ booleano Variant** que especifica si se redirige la captura de audio.</span><span class="sxs-lookup"><span data-stu-id="34048-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="34048-114">Especifique **Variant \_ true** si desea que se redirija la captura de audio.</span><span class="sxs-lookup"><span data-stu-id="34048-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="34048-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34048-115">Requirements</span></span>



| <span data-ttu-id="34048-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="34048-116">Requirement</span></span> | <span data-ttu-id="34048-117">Value</span><span class="sxs-lookup"><span data-stu-id="34048-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34048-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34048-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34048-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="34048-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="34048-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34048-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34048-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="34048-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="34048-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="34048-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="34048-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34048-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="34048-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34048-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34048-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34048-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="34048-126">IID</span><span class="sxs-lookup"><span data-stu-id="34048-126">IID</span></span><br/>                      | <span data-ttu-id="34048-127">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="34048-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="34048-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="34048-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34048-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="34048-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="34048-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="34048-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






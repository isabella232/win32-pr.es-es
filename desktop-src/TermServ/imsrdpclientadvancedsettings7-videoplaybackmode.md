---
title: Propiedad VideoPlaybackMode de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica el modo de reproducción de vídeo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad VideoPlaybackMode
- Propiedad VideoPlaybackMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad VideoPlaybackMode
- Propiedad VideoPlaybackMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422627"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="19081-108">IMsRdpClientAdvancedSettings7:: VideoPlaybackMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="19081-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="19081-109">Especifica o recupera un valor que indica el modo de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="19081-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="19081-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="19081-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19081-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19081-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="19081-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="19081-112">Property value</span></span>

<span data-ttu-id="19081-113">Valor que especifica el modo de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="19081-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="19081-114">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="19081-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="19081-115">1</span><span class="sxs-lookup"><span data-stu-id="19081-115">1</span></span>
</dt> <dd>

<span data-ttu-id="19081-116">El modo de reproducción de vídeo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="19081-116">The default video playback mode.</span></span> <span data-ttu-id="19081-117">Cuando el modo de reproducción de vídeo se establece en este valor, la redirección de vídeo se controla mediante la propiedad [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) .</span><span class="sxs-lookup"><span data-stu-id="19081-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="19081-118">Cuando la propiedad **AudioRedirectionMode** se establece en el **modo de audio \_ \_ Redirect**, el vídeo se descodifica y se representa en el cliente.</span><span class="sxs-lookup"><span data-stu-id="19081-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="19081-119">0</span><span class="sxs-lookup"><span data-stu-id="19081-119">0</span></span>
</dt> <dd>

<span data-ttu-id="19081-120">La redirección de reproducción de vídeo está deshabilitada, incluso cuando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) está establecido en **\_ \_ redirigir el modo de audio**.</span><span class="sxs-lookup"><span data-stu-id="19081-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="19081-121">En este modo, el vídeo se descodifica y se representa en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="19081-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19081-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19081-122">Requirements</span></span>



| <span data-ttu-id="19081-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19081-123">Requirement</span></span> | <span data-ttu-id="19081-124">Value</span><span class="sxs-lookup"><span data-stu-id="19081-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19081-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19081-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19081-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19081-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="19081-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19081-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19081-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19081-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="19081-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="19081-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="19081-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19081-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19081-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19081-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19081-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19081-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19081-133">IID</span><span class="sxs-lookup"><span data-stu-id="19081-133">IID</span></span><br/>                      | <span data-ttu-id="19081-134">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="19081-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19081-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="19081-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19081-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19081-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19081-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19081-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






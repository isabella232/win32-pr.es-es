---
title: Propiedad AudioQualityMode de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido. De forma predeterminada, se establece en 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioQualityMode
- Propiedad AudioQualityMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AudioQualityMode
- Propiedad AudioQualityMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686032"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="961be-109">IMsRdpClientAdvancedSettings7:: AudioQualityMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="961be-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="961be-110">Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido.</span><span class="sxs-lookup"><span data-stu-id="961be-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="961be-111">De forma predeterminada, se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="961be-111">By default this is set to 0.</span></span>

<span data-ttu-id="961be-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="961be-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="961be-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="961be-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="961be-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="961be-114">Property value</span></span>

<span data-ttu-id="961be-115">Valor que especifica el modo de calidad de audio.</span><span class="sxs-lookup"><span data-stu-id="961be-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="961be-116">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="961be-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="961be-117">0</span><span class="sxs-lookup"><span data-stu-id="961be-117">0</span></span>
</dt> <dd>

<span data-ttu-id="961be-118">Calidad de audio dinámica.</span><span class="sxs-lookup"><span data-stu-id="961be-118">Dynamic audio quality.</span></span> <span data-ttu-id="961be-119">Esta es la configuración de calidad de audio predeterminada.</span><span class="sxs-lookup"><span data-stu-id="961be-119">This is the default audio quality setting.</span></span> <span data-ttu-id="961be-120">El servidor ajusta dinámicamente la calidad de salida de audio en respuesta a las condiciones de red y a las capacidades de cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="961be-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="961be-121">1</span><span class="sxs-lookup"><span data-stu-id="961be-121">1</span></span>
</dt> <dd>

<span data-ttu-id="961be-122">Calidad de audio media.</span><span class="sxs-lookup"><span data-stu-id="961be-122">Medium audio quality.</span></span> <span data-ttu-id="961be-123">El servidor usa un formato fijo pero comprimido para la salida de audio.</span><span class="sxs-lookup"><span data-stu-id="961be-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="961be-124">2</span><span class="sxs-lookup"><span data-stu-id="961be-124">2</span></span>
</dt> <dd>

<span data-ttu-id="961be-125">Calidad de audio alta.</span><span class="sxs-lookup"><span data-stu-id="961be-125">High audio quality.</span></span> <span data-ttu-id="961be-126">El servidor proporciona una salida de audio en formato PCM sin comprimir con una sobrecarga de procesamiento menor para la latencia.</span><span class="sxs-lookup"><span data-stu-id="961be-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="961be-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="961be-127">Requirements</span></span>



| <span data-ttu-id="961be-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="961be-128">Requirement</span></span> | <span data-ttu-id="961be-129">Value</span><span class="sxs-lookup"><span data-stu-id="961be-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="961be-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="961be-130">Minimum supported client</span></span><br/> | <span data-ttu-id="961be-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="961be-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="961be-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="961be-132">Minimum supported server</span></span><br/> | <span data-ttu-id="961be-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="961be-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="961be-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="961be-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="961be-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="961be-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="961be-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="961be-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="961be-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="961be-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="961be-138">IID</span><span class="sxs-lookup"><span data-stu-id="961be-138">IID</span></span><br/>                      | <span data-ttu-id="961be-139">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="961be-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="961be-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="961be-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961be-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="961be-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="961be-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="961be-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 






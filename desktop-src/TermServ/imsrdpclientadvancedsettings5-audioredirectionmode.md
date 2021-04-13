---
title: Propiedad AudioRedirectionMode de IMsRdpClientAdvancedSettings5
description: Establece y recupera el modo de redirección de audio y las distintas opciones de redirección de audio.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359703"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="d5c0b-112">IMsRdpClientAdvancedSettings5:: AudioRedirectionMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d5c0b-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="d5c0b-113">Establece y recupera el modo de redirección de audio y las distintas opciones de redirección de audio.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="d5c0b-114">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c0b-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c0b-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="d5c0b-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d5c0b-116">Property value</span></span>

<span data-ttu-id="d5c0b-117">Establece valores diferentes para el modo de redirección de audio.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="d5c0b-118">Este parámetro tiene los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="d5c0b-119">**Audio \_ de \_** Redireccionamiento de modo 0 (la redirección de audio está habilitada y la opción para la redirección es "traer a este equipo".</span><span class="sxs-lookup"><span data-stu-id="d5c0b-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="d5c0b-120">Este es el modo predeterminado).</span><span class="sxs-lookup"><span data-stu-id="d5c0b-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="d5c0b-121">**Audio \_ de MODO \_ Play \_ en el \_ servidor 1** (la redirección de audio está habilitada y la opción es "dejar en el equipo remoto".</span><span class="sxs-lookup"><span data-stu-id="d5c0b-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="d5c0b-122">La opción "dejar en el equipo remoto" solo se admite cuando se conecta de forma remota a un equipo host que ejecuta Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d5c0b-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="d5c0b-123">Si la conexión se realiza a un equipo host que ejecuta Windows Server 2008, la opción "dejar en el equipo remoto" cambia a "no reproducir").</span><span class="sxs-lookup"><span data-stu-id="d5c0b-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="d5c0b-124">**Audio \_ de MODO \_ ninguno 2** (la redirección de audio está habilitada y el modo es "no reproducir").</span><span class="sxs-lookup"><span data-stu-id="d5c0b-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="d5c0b-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d5c0b-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d5c0b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c0b-126">Requirements</span></span>



| <span data-ttu-id="d5c0b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c0b-127">Requirement</span></span> | <span data-ttu-id="d5c0b-128">Value</span><span class="sxs-lookup"><span data-stu-id="d5c0b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c0b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c0b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c0b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5c0b-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d5c0b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c0b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c0b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5c0b-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d5c0b-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d5c0b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5c0b-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c0b-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d5c0b-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5c0b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c0b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c0b-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d5c0b-137">IID</span><span class="sxs-lookup"><span data-stu-id="d5c0b-137">IID</span></span><br/>                      | <span data-ttu-id="d5c0b-138">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="d5c0b-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5c0b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c0b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c0b-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d5c0b-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d5c0b-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d5c0b-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d5c0b-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d5c0b-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d5c0b-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d5c0b-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 






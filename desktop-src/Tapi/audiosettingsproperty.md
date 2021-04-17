---
description: 'Los métodos ITAudioSettings:: GetRange, ITAudioSettings:: get y ITAudioSettings:: set usan la enumeración AudioSettingsProperty para indicar la propiedad de configuración de audio que se está solucionando.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumeración AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690492"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="a2844-103">Enumeración AudioSettingsProperty</span><span class="sxs-lookup"><span data-stu-id="a2844-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="a2844-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a2844-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2844-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="a2844-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a2844-106">Los métodos [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: get**](itaudiosettings-get.md)y [**ITAudioSettings:: set**](itaudiosettings-set.md) usan la enumeración **AudioSettingsProperty** para indicar la propiedad de configuración de audio que se está solucionando.</span><span class="sxs-lookup"><span data-stu-id="a2844-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2844-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2844-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="a2844-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a2844-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a2844-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**</span><span class="sxs-lookup"><span data-stu-id="a2844-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-110">Propiedad de configuración de la señal.</span><span class="sxs-lookup"><span data-stu-id="a2844-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**</span><span class="sxs-lookup"><span data-stu-id="a2844-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-112">Propiedad de umbral de latencia.</span><span class="sxs-lookup"><span data-stu-id="a2844-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volumen AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="a2844-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-114">Propiedad de volumen.</span><span class="sxs-lookup"><span data-stu-id="a2844-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Saldo de AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="a2844-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-116">Propiedad saldo.</span><span class="sxs-lookup"><span data-stu-id="a2844-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Sonoridad AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="a2844-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-118">Propiedad de sonoridad.</span><span class="sxs-lookup"><span data-stu-id="a2844-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ agudos**</span><span class="sxs-lookup"><span data-stu-id="a2844-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-120">Propiedad de agudos.</span><span class="sxs-lookup"><span data-stu-id="a2844-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ graves**</span><span class="sxs-lookup"><span data-stu-id="a2844-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-122">Propiedad Bass.</span><span class="sxs-lookup"><span data-stu-id="a2844-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="a2844-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="a2844-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="a2844-124">Propiedad monoaural.</span><span class="sxs-lookup"><span data-stu-id="a2844-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2844-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2844-125">Requirements</span></span>



| <span data-ttu-id="a2844-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2844-126">Requirement</span></span> | <span data-ttu-id="a2844-127">Value</span><span class="sxs-lookup"><span data-stu-id="a2844-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2844-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a2844-128">TAPI version</span></span><br/> | <span data-ttu-id="a2844-129">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a2844-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="a2844-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2844-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a2844-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2844-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2844-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2844-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2844-133">**ITAudioSettings::GetRange**</span><span class="sxs-lookup"><span data-stu-id="a2844-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="a2844-134">**ITAudioSettings:: get**</span><span class="sxs-lookup"><span data-stu-id="a2844-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="a2844-135">**ITAudioSettings:: set**</span><span class="sxs-lookup"><span data-stu-id="a2844-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 





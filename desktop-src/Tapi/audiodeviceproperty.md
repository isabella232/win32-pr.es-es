---
description: 'Los métodos ITAudioDeviceControl:: GetRange, ITAudioDeviceControl:: get y ITAudioDeviceControl:: set usan la enumeración AudioDeviceProperty para indicar la propiedad que se está solucionando.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumeración AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680324"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="8507c-103">Enumeración AudioDeviceProperty</span><span class="sxs-lookup"><span data-stu-id="8507c-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="8507c-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8507c-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8507c-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8507c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8507c-106">Los métodos [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: get**](itaudiodevicecontrol-get.md)y [**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md) usan la enumeración **AudioDeviceProperty** para indicar la propiedad que se está solucionando.</span><span class="sxs-lookup"><span data-stu-id="8507c-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8507c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8507c-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="8507c-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8507c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8507c-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**</span><span class="sxs-lookup"><span data-stu-id="8507c-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="8507c-110">Indica que se está configurando o recuperando el modo dúplex del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8507c-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="8507c-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**</span><span class="sxs-lookup"><span data-stu-id="8507c-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="8507c-112">Indica que se está configurando o recuperando el control de ganancia automática del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8507c-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="8507c-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**</span><span class="sxs-lookup"><span data-stu-id="8507c-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="8507c-114">Indica que se están configurando o recuperando las propiedades de cancelación del eco acústico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8507c-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8507c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8507c-115">Requirements</span></span>



| <span data-ttu-id="8507c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8507c-116">Requirement</span></span> | <span data-ttu-id="8507c-117">Value</span><span class="sxs-lookup"><span data-stu-id="8507c-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8507c-118">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8507c-118">TAPI version</span></span><br/> | <span data-ttu-id="8507c-119">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="8507c-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="8507c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8507c-120">Header</span></span><br/>       | <dl> <span data-ttu-id="8507c-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8507c-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8507c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8507c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8507c-123">**ITAudioDeviceControl::GetRange**</span><span class="sxs-lookup"><span data-stu-id="8507c-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="8507c-124">**ITAudioDeviceControl:: get**</span><span class="sxs-lookup"><span data-stu-id="8507c-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="8507c-125">**ITAudioDeviceControl:: set**</span><span class="sxs-lookup"><span data-stu-id="8507c-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 





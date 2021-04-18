---
description: 'Los métodos ITCallQualityControl:: GetRange, ITCallQualityControl:: get y ITCallQualityControl:: set usan la enumeración CallQualityProperty para indicar la propiedad de calidad de la llamada que se va a resolver.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumeración CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680403"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="59405-103">Enumeración CallQualityProperty</span><span class="sxs-lookup"><span data-stu-id="59405-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="59405-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="59405-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="59405-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="59405-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="59405-106">Los métodos [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: get**](itcallqualitycontrol-get.md)y [**ITCallQualityControl:: set**](itcallqualitycontrol-set.md) usan la enumeración **CallQualityProperty** para indicar la propiedad de calidad de la llamada que se va a resolver.</span><span class="sxs-lookup"><span data-stu-id="59405-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="59405-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59405-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="59405-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="59405-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="59405-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**</span><span class="sxs-lookup"><span data-stu-id="59405-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="59405-110">Intervalo de control.</span><span class="sxs-lookup"><span data-stu-id="59405-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="59405-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**</span><span class="sxs-lookup"><span data-stu-id="59405-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="59405-112">Velocidad de bits para la Conferencia.</span><span class="sxs-lookup"><span data-stu-id="59405-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="59405-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="59405-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="59405-114">Velocidad de bits de entrada máxima.</span><span class="sxs-lookup"><span data-stu-id="59405-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="59405-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="59405-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="59405-116">Velocidad de bits de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="59405-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="59405-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="59405-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="59405-118">Velocidad de bits de salida máxima.</span><span class="sxs-lookup"><span data-stu-id="59405-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="59405-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="59405-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="59405-120">Velocidad de bits de salida actual.</span><span class="sxs-lookup"><span data-stu-id="59405-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="59405-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**</span><span class="sxs-lookup"><span data-stu-id="59405-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="59405-122">Carga máxima de la CPU.</span><span class="sxs-lookup"><span data-stu-id="59405-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="59405-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**</span><span class="sxs-lookup"><span data-stu-id="59405-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="59405-124">Carga de CPU actual.</span><span class="sxs-lookup"><span data-stu-id="59405-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59405-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59405-125">Requirements</span></span>



| <span data-ttu-id="59405-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="59405-126">Requirement</span></span> | <span data-ttu-id="59405-127">Value</span><span class="sxs-lookup"><span data-stu-id="59405-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59405-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="59405-128">TAPI version</span></span><br/> | <span data-ttu-id="59405-129">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="59405-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="59405-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59405-130">Header</span></span><br/>       | <dl> <span data-ttu-id="59405-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="59405-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59405-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="59405-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59405-133">**ITCallQualityControl::GetRange**</span><span class="sxs-lookup"><span data-stu-id="59405-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="59405-134">**ITCallQualityControl:: get**</span><span class="sxs-lookup"><span data-stu-id="59405-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="59405-135">**ITCallQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="59405-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 





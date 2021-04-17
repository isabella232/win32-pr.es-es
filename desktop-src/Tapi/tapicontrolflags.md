---
description: Una serie de métodos utiliza la enumeración TAPIControlFlags para indicar si una propiedad determinada se controla de forma automática o manual.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumeración TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690803"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="520b5-103">Enumeración TAPIControlFlags</span><span class="sxs-lookup"><span data-stu-id="520b5-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="520b5-104">\[ Esta enumeración no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="520b5-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="520b5-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="520b5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="520b5-106">Una serie de métodos utiliza la enumeración **TAPIControlFlags** para indicar si una propiedad determinada se controla de forma automática o manual.</span><span class="sxs-lookup"><span data-stu-id="520b5-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="520b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="520b5-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="520b5-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="520b5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="520b5-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ marca \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="520b5-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="520b5-110">TAPI no tiene marcas de control para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="520b5-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="520b5-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl \_ marcas \_ automáticas**</span><span class="sxs-lookup"><span data-stu-id="520b5-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="520b5-112">La propiedad se controla automáticamente.</span><span class="sxs-lookup"><span data-stu-id="520b5-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="520b5-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manual de marcas TAPIControl \_**</span><span class="sxs-lookup"><span data-stu-id="520b5-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="520b5-114">La propiedad se controla manualmente.</span><span class="sxs-lookup"><span data-stu-id="520b5-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="520b5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520b5-115">Requirements</span></span>



| <span data-ttu-id="520b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="520b5-116">Requirement</span></span> | <span data-ttu-id="520b5-117">Value</span><span class="sxs-lookup"><span data-stu-id="520b5-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="520b5-118">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="520b5-118">TAPI version</span></span><br/> | <span data-ttu-id="520b5-119">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="520b5-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="520b5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="520b5-120">Header</span></span><br/>       | <dl> <span data-ttu-id="520b5-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="520b5-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520b5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="520b5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520b5-123">**ITAudioDeviceControl::GetRange**</span><span class="sxs-lookup"><span data-stu-id="520b5-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="520b5-124">**ITAudioDeviceControl:: get**</span><span class="sxs-lookup"><span data-stu-id="520b5-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="520b5-125">**ITAudioDeviceControl:: set**</span><span class="sxs-lookup"><span data-stu-id="520b5-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="520b5-126">**ITAudioSettings::GetRange**</span><span class="sxs-lookup"><span data-stu-id="520b5-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="520b5-127">**ITAudioSettings:: get**</span><span class="sxs-lookup"><span data-stu-id="520b5-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="520b5-128">**ITAudioSettings:: set**</span><span class="sxs-lookup"><span data-stu-id="520b5-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="520b5-129">**ITCallQualityControl::GetRange**</span><span class="sxs-lookup"><span data-stu-id="520b5-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="520b5-130">**ITCallQualityControl:: get**</span><span class="sxs-lookup"><span data-stu-id="520b5-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="520b5-131">**ITCallQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="520b5-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="520b5-132">**ITStreamQualityControl::GetRange**</span><span class="sxs-lookup"><span data-stu-id="520b5-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="520b5-133">**ITStreamQualityControl:: get**</span><span class="sxs-lookup"><span data-stu-id="520b5-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="520b5-134">**ITStreamQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="520b5-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 





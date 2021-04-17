---
description: El método get recupera el valor de una propiedad de dispositivo de audio determinada.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: 'ITAudioDeviceControl:: get (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4311dc18291fcfbbe533dbe17042e6ba19c1122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690923"
---
# <a name="itaudiodevicecontrolget-method"></a><span data-ttu-id="e788e-103">ITAudioDeviceControl:: get (método)</span><span class="sxs-lookup"><span data-stu-id="e788e-103">ITAudioDeviceControl::Get method</span></span>

<span data-ttu-id="e788e-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e788e-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e788e-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e788e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e788e-106">El método **Get** recupera el valor de una propiedad de [**dispositivo de audio**](audiodeviceproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="e788e-106">The **Get** method retrieves the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e788e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e788e-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="e788e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e788e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e788e-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e788e-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e788e-110">Miembro de la enumeración [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e788e-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="e788e-111">*plValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e788e-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e788e-112">Valor de la *propiedad* de entrada.</span><span class="sxs-lookup"><span data-stu-id="e788e-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="e788e-113">*plFlags* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e788e-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e788e-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controla el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="e788e-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e788e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e788e-115">Return value</span></span>

<span data-ttu-id="e788e-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="e788e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="e788e-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e788e-117">Return code</span></span>                                                                                   | <span data-ttu-id="e788e-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e788e-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e788e-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e788e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e788e-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e788e-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e788e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e788e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e788e-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e788e-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e788e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e788e-123">Requirements</span></span>



| <span data-ttu-id="e788e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e788e-124">Requirement</span></span> | <span data-ttu-id="e788e-125">Value</span><span class="sxs-lookup"><span data-stu-id="e788e-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e788e-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e788e-126">TAPI version</span></span><br/> | <span data-ttu-id="e788e-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="e788e-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="e788e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e788e-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e788e-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e788e-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e788e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e788e-130">Library</span></span><br/>      | <dl> <span data-ttu-id="e788e-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e788e-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e788e-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e788e-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="e788e-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e788e-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e788e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e788e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e788e-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="e788e-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="e788e-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="e788e-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="e788e-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="e788e-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 





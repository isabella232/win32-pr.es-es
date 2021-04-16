---
description: El método Set establece el valor de una propiedad de dispositivo de audio determinada.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'ITAudioDeviceControl:: set (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679154"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="92094-103">ITAudioDeviceControl:: set (método)</span><span class="sxs-lookup"><span data-stu-id="92094-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="92094-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="92094-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="92094-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="92094-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="92094-106">El método **set** establece el valor de una [**propiedad de dispositivo de audio**](audiodeviceproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="92094-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92094-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92094-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="92094-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92094-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92094-109">*Propiedad* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92094-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92094-110">Miembro de la enumeración [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="92094-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="92094-111">valor *l* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92094-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92094-112">Valor deseado para la propiedad.</span><span class="sxs-lookup"><span data-stu-id="92094-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="92094-113">*lFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="92094-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92094-114">Valor de la enumeración [**TAPIControlFlags**](tapicontrolflags.md) que indica cómo se controlará el valor de la *propiedad* .</span><span class="sxs-lookup"><span data-stu-id="92094-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92094-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92094-115">Return value</span></span>

<span data-ttu-id="92094-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="92094-116">This method can return one of these values.</span></span>



| <span data-ttu-id="92094-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="92094-117">Return code</span></span>                                                                                   | <span data-ttu-id="92094-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="92094-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="92094-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="92094-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="92094-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="92094-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="92094-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="92094-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="92094-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="92094-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92094-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92094-123">Requirements</span></span>



| <span data-ttu-id="92094-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="92094-124">Requirement</span></span> | <span data-ttu-id="92094-125">Value</span><span class="sxs-lookup"><span data-stu-id="92094-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92094-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="92094-126">TAPI version</span></span><br/> | <span data-ttu-id="92094-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="92094-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="92094-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92094-128">Header</span></span><br/>       | <dl> <span data-ttu-id="92094-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92094-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="92094-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92094-130">Library</span></span><br/>      | <dl> <span data-ttu-id="92094-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92094-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="92094-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92094-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="92094-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92094-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92094-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="92094-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92094-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="92094-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="92094-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="92094-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="92094-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="92094-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 





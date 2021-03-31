---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtiene el ancho de banda efectivo actual para el dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Método GetEffectiveBandwidth API de streaming de multimedia
- Método GetEffectiveBandwidth API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079723"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="66e8a-106">ActiveBasicDevice:: GetEffectiveBandwidth (método)</span><span class="sxs-lookup"><span data-stu-id="66e8a-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="66e8a-107">Obtiene el ancho de banda efectivo actual para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66e8a-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e8a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66e8a-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="66e8a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66e8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e8a-110">*transmitSpeed* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="66e8a-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="66e8a-111">Especifica si se recupera la velocidad de transmisión o se recupera la velocidad de recepción.</span><span class="sxs-lookup"><span data-stu-id="66e8a-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="66e8a-112">**true** para recuperar la velocidad de transmisión.</span><span class="sxs-lookup"><span data-stu-id="66e8a-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="66e8a-113">**false** para recuperar la velocidad de recepción.</span><span class="sxs-lookup"><span data-stu-id="66e8a-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="66e8a-114">*currentSpeed* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="66e8a-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66e8a-115">Recibe el ancho de banda efectivo actual.</span><span class="sxs-lookup"><span data-stu-id="66e8a-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e8a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66e8a-116">Return value</span></span>

<span data-ttu-id="66e8a-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="66e8a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66e8a-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66e8a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e8a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66e8a-119">Requirements</span></span>



| <span data-ttu-id="66e8a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="66e8a-120">Requirement</span></span> | <span data-ttu-id="66e8a-121">Value</span><span class="sxs-lookup"><span data-stu-id="66e8a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="66e8a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66e8a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66e8a-123">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="66e8a-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="66e8a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66e8a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66e8a-125">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66e8a-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66e8a-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66e8a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e8a-127"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e8a-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="66e8a-128">IDL</span><span class="sxs-lookup"><span data-stu-id="66e8a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66e8a-129"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66e8a-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="66e8a-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66e8a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66e8a-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66e8a-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e8a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="66e8a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="66e8a-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="66e8a-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 


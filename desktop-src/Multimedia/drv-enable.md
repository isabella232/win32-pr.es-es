---
title: Mensaje de DRV_ENABLE (mmsystem. h)
description: Habilita el controlador. El controlador debe inicializar las variables y ubicar los dispositivos con la interfaz de entrada y salida (e/s).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- Mensaje de DRV_ENABLE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997094"
---
# <a name="drv_enable-message"></a><span data-ttu-id="82625-105">DRV- \_ Habilitar mensaje</span><span class="sxs-lookup"><span data-stu-id="82625-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="82625-106">Habilita el controlador.</span><span class="sxs-lookup"><span data-stu-id="82625-106">Enables the driver.</span></span> <span data-ttu-id="82625-107">El controlador debe inicializar las variables y ubicar los dispositivos con la interfaz de entrada y salida (e/s).</span><span class="sxs-lookup"><span data-stu-id="82625-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="82625-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82625-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82625-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="82625-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="82625-110">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="82625-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82625-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82625-111">Return Value</span></span>

<span data-ttu-id="82625-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="82625-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82625-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82625-113">Remarks</span></span>

<span data-ttu-id="82625-114">No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="82625-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="82625-115">Los controladores se consideran habilitados desde el momento en que reciben este mensaje hasta que se deshabiliten mediante el mensaje [**DRV \_ Disable**](drv-disable.md) .</span><span class="sxs-lookup"><span data-stu-id="82625-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="82625-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82625-116">Requirements</span></span>



| <span data-ttu-id="82625-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="82625-117">Requirement</span></span> | <span data-ttu-id="82625-118">Value</span><span class="sxs-lookup"><span data-stu-id="82625-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82625-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82625-119">Minimum supported client</span></span><br/> | <span data-ttu-id="82625-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="82625-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="82625-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82625-121">Minimum supported server</span></span><br/> | <span data-ttu-id="82625-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="82625-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="82625-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82625-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="82625-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82625-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82625-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="82625-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82625-126">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="82625-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="82625-127">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="82625-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






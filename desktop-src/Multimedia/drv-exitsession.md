---
title: Mensaje de DRV_EXITSESSION (mmsystem. h)
description: Notifica al controlador que Windows se está preparando para salir. El controlador debe prepararse para la terminación.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- Mensaje de DRV_EXITSESSION de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493042"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="6bcd9-105">\_Mensaje EXITSESSION DRV</span><span class="sxs-lookup"><span data-stu-id="6bcd9-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="6bcd9-106">Notifica al controlador que Windows se está preparando para salir.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="6bcd9-107">El controlador debe prepararse para la terminación.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="6bcd9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bcd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bcd9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="6bcd9-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="6bcd9-110">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-110">Identifier of the installable driver.</span></span> <span data-ttu-id="6bcd9-111">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="6bcd9-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6bcd9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="6bcd9-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="6bcd9-113">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bcd9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bcd9-114">Return Value</span></span>

<span data-ttu-id="6bcd9-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6bcd9-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcd9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bcd9-116">Remarks</span></span>

<span data-ttu-id="6bcd9-117">No se usan los parámetros *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="6bcd9-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bcd9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bcd9-118">Requirements</span></span>



| <span data-ttu-id="6bcd9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bcd9-119">Requirement</span></span> | <span data-ttu-id="6bcd9-120">Value</span><span class="sxs-lookup"><span data-stu-id="6bcd9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bcd9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bcd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6bcd9-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6bcd9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6bcd9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6bcd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6bcd9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6bcd9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6bcd9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bcd9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bcd9-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bcd9-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bcd9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bcd9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bcd9-128">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="6bcd9-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="6bcd9-129">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="6bcd9-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






---
title: Mensaje de DRV_REMOVE (mmsystem. h)
description: Notifica al controlador que está a punto de quitarse del sistema. Cuando un controlador recibe este mensaje, debe quitar todas las secciones creadas en el registro.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- Mensaje de DRV_REMOVE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079753"
---
# <a name="drv_remove-message"></a><span data-ttu-id="c2dec-105">DRV \_ quitar mensaje</span><span class="sxs-lookup"><span data-stu-id="c2dec-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="c2dec-106">Notifica al controlador que está a punto de quitarse del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2dec-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="c2dec-107">Cuando un controlador recibe este mensaje, debe quitar todas las secciones creadas en el registro.</span><span class="sxs-lookup"><span data-stu-id="c2dec-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2dec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2dec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2dec-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="c2dec-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="c2dec-110">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="c2dec-110">Identifier of the installable driver.</span></span> <span data-ttu-id="c2dec-111">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="c2dec-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="c2dec-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="c2dec-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="c2dec-113">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="c2dec-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2dec-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2dec-114">Return Value</span></span>

<span data-ttu-id="c2dec-115">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c2dec-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2dec-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2dec-116">Remarks</span></span>

<span data-ttu-id="c2dec-117">No se usan los parámetros *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="c2dec-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2dec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2dec-118">Requirements</span></span>



| <span data-ttu-id="c2dec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2dec-119">Requirement</span></span> | <span data-ttu-id="c2dec-120">Value</span><span class="sxs-lookup"><span data-stu-id="c2dec-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dec-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2dec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c2dec-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c2dec-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2dec-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2dec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c2dec-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c2dec-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2dec-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2dec-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2dec-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2dec-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2dec-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2dec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dec-128">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="c2dec-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="c2dec-129">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="c2dec-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






---
title: Mensaje de DRV_POWER (mmsystem. h)
description: Notifica al controlador que se está activando o desactivando la energía del dispositivo.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- Mensaje de DRV_POWER de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997087"
---
# <a name="drv_power-message"></a><span data-ttu-id="d745a-104">DRV \_ mensaje de energía</span><span class="sxs-lookup"><span data-stu-id="d745a-104">DRV\_POWER message</span></span>

<span data-ttu-id="d745a-105">Notifica al controlador que se está activando o desactivando la energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d745a-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="d745a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d745a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d745a-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="d745a-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="d745a-108">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="d745a-108">Identifier of the installable driver.</span></span> <span data-ttu-id="d745a-109">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="d745a-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="d745a-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="d745a-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="d745a-111">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="d745a-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d745a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d745a-112">Return Value</span></span>

<span data-ttu-id="d745a-113">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d745a-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d745a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d745a-114">Remarks</span></span>

<span data-ttu-id="d745a-115">No se usan los parámetros *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="d745a-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d745a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d745a-116">Requirements</span></span>



| <span data-ttu-id="d745a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d745a-117">Requirement</span></span> | <span data-ttu-id="d745a-118">Value</span><span class="sxs-lookup"><span data-stu-id="d745a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d745a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d745a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d745a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d745a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d745a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d745a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d745a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d745a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d745a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d745a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d745a-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d745a-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d745a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d745a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d745a-126">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="d745a-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="d745a-127">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="d745a-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






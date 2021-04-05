---
title: Mensaje de DRV_FREE (mmsystem. h)
description: Notifica al controlador que se va a quitar de la memoria. El controlador debe liberar la memoria y otros recursos del sistema que haya asignado.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- Mensaje de DRV_FREE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997091"
---
# <a name="drv_free-message"></a><span data-ttu-id="fec66-105">DRV ( \_ mensaje gratuito)</span><span class="sxs-lookup"><span data-stu-id="fec66-105">DRV\_FREE message</span></span>

<span data-ttu-id="fec66-106">Notifica al controlador que se va a quitar de la memoria.</span><span class="sxs-lookup"><span data-stu-id="fec66-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="fec66-107">El controlador debe liberar la memoria y otros recursos del sistema que haya asignado.</span><span class="sxs-lookup"><span data-stu-id="fec66-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="fec66-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fec66-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec66-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="fec66-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="fec66-110">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="fec66-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec66-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fec66-111">Return Value</span></span>

<span data-ttu-id="fec66-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fec66-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec66-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fec66-113">Remarks</span></span>

<span data-ttu-id="fec66-114">No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="fec66-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="fec66-115">El mensaje de **\_ disponibilidad de DRV** es siempre el último mensaje que recibe un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fec66-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec66-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec66-116">Requirements</span></span>



| <span data-ttu-id="fec66-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec66-117">Requirement</span></span> | <span data-ttu-id="fec66-118">Value</span><span class="sxs-lookup"><span data-stu-id="fec66-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec66-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec66-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fec66-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fec66-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fec66-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec66-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fec66-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fec66-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fec66-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fec66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fec66-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fec66-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec66-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fec66-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec66-126">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="fec66-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="fec66-127">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="fec66-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






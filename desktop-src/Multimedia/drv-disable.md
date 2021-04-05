---
title: Mensaje de DRV_DISABLE (mmsystem. h)
description: Deshabilita el controlador. El controlador debe colocar el dispositivo correspondiente, si existe, en un estado inactivo y finalizar las funciones de devolución de llamada o los subprocesos.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Mensaje de DRV_DISABLE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997092"
---
# <a name="drv_disable-message"></a><span data-ttu-id="412c9-105">DRV \_ deshabilitar mensaje</span><span class="sxs-lookup"><span data-stu-id="412c9-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="412c9-106">Deshabilita el controlador.</span><span class="sxs-lookup"><span data-stu-id="412c9-106">Disables the driver.</span></span> <span data-ttu-id="412c9-107">El controlador debe colocar el dispositivo correspondiente, si existe, en un estado inactivo y finalizar las funciones de devolución de llamada o los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="412c9-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="412c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="412c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="412c9-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="412c9-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="412c9-110">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="412c9-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="412c9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="412c9-111">Return Value</span></span>

<span data-ttu-id="412c9-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="412c9-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="412c9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="412c9-113">Remarks</span></span>

<span data-ttu-id="412c9-114">No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="412c9-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="412c9-115">Después de deshabilitar el controlador, el sistema normalmente envía un mensaje [**DRV \_ Free**](drv-free.md) al controlador antes de quitar el controlador de la memoria.</span><span class="sxs-lookup"><span data-stu-id="412c9-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="412c9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="412c9-116">Requirements</span></span>



| <span data-ttu-id="412c9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="412c9-117">Requirement</span></span> | <span data-ttu-id="412c9-118">Value</span><span class="sxs-lookup"><span data-stu-id="412c9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="412c9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="412c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="412c9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="412c9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="412c9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="412c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="412c9-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="412c9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="412c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="412c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="412c9-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="412c9-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412c9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="412c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412c9-126">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="412c9-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="412c9-127">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="412c9-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






---
title: Mensaje de DRV_LOAD (mmsystem. h)
description: Notifica al controlador que se ha cargado. El controlador debe asegurarse de que el hardware y los controladores auxiliares que necesita para funcionar correctamente estén presentes.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- Mensaje de DRV_LOAD de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997089"
---
# <a name="drv_load-message"></a><span data-ttu-id="d5db3-105">DRV \_ cargar mensaje</span><span class="sxs-lookup"><span data-stu-id="d5db3-105">DRV\_LOAD message</span></span>

<span data-ttu-id="d5db3-106">Notifica al controlador que se ha cargado.</span><span class="sxs-lookup"><span data-stu-id="d5db3-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="d5db3-107">El controlador debe asegurarse de que el hardware y los controladores auxiliares que necesita para funcionar correctamente estén presentes.</span><span class="sxs-lookup"><span data-stu-id="d5db3-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5db3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5db3-108">Parameters</span></span>

<span data-ttu-id="d5db3-109">El parámetro *hdrvr* siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="d5db3-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="d5db3-110">No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="d5db3-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5db3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5db3-111">Return Value</span></span>

<span data-ttu-id="d5db3-112">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d5db3-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5db3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5db3-113">Remarks</span></span>

<span data-ttu-id="d5db3-114">El mensaje de **\_ carga DRV** es siempre el primer mensaje que recibe un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5db3-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5db3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5db3-115">Requirements</span></span>



| <span data-ttu-id="d5db3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5db3-116">Requirement</span></span> | <span data-ttu-id="d5db3-117">Value</span><span class="sxs-lookup"><span data-stu-id="d5db3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5db3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5db3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d5db3-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d5db3-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d5db3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5db3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d5db3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d5db3-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5db3-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5db3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5db3-123"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5db3-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5db3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5db3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5db3-125">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="d5db3-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="d5db3-126">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="d5db3-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






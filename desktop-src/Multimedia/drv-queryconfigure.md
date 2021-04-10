---
title: Mensaje de DRV_QUERYCONFIGURE (mmsystem. h)
description: Indica al controlador que especifique si admite la configuración personalizada.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- Mensaje de DRV_QUERYCONFIGURE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274544"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="6d8fe-104">\_Mensaje QUERYCONFIGURE DRV</span><span class="sxs-lookup"><span data-stu-id="6d8fe-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="6d8fe-105">Indica al controlador que especifique si admite la configuración personalizada.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d8fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d8fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d8fe-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="6d8fe-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="6d8fe-108">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-108">Identifier of the installable driver.</span></span> <span data-ttu-id="6d8fe-109">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="6d8fe-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6d8fe-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="6d8fe-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="6d8fe-111">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d8fe-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d8fe-112">Return Value</span></span>

<span data-ttu-id="6d8fe-113">Devuelve un valor distinto de cero si el controlador puede mostrar un cuadro de diálogo de configuración o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="6d8fe-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d8fe-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d8fe-114">Remarks</span></span>

<span data-ttu-id="6d8fe-115">No se usan los parámetros *lParam1* y *lParam2* .</span><span class="sxs-lookup"><span data-stu-id="6d8fe-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d8fe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d8fe-116">Requirements</span></span>



| <span data-ttu-id="6d8fe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d8fe-117">Requirement</span></span> | <span data-ttu-id="6d8fe-118">Value</span><span class="sxs-lookup"><span data-stu-id="6d8fe-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d8fe-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d8fe-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6d8fe-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6d8fe-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d8fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d8fe-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d8fe-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d8fe-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d8fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d8fe-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d8fe-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d8fe-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d8fe-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d8fe-126">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="6d8fe-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="6d8fe-127">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="6d8fe-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






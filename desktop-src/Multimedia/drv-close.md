---
title: Mensaje de DRV_CLOSE (mmsystem. h)
description: Indica al controlador que cierre la instancia de especificada. Si no hay ninguna otra instancia abierta, el controlador debe prepararse para la versión posterior de la memoria.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- Mensaje de DRV_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651420"
---
# <a name="drv_close-message"></a><span data-ttu-id="aa75b-105">DRV- \_ cerrar mensaje</span><span class="sxs-lookup"><span data-stu-id="aa75b-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="aa75b-106">Indica al controlador que cierre la instancia de especificada.</span><span class="sxs-lookup"><span data-stu-id="aa75b-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="aa75b-107">Si no hay ninguna otra instancia abierta, el controlador debe prepararse para la versión posterior de la memoria.</span><span class="sxs-lookup"><span data-stu-id="aa75b-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa75b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa75b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa75b-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="aa75b-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="aa75b-110">Identificador del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="aa75b-110">Identifier of the installable driver.</span></span> <span data-ttu-id="aa75b-111">Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="aa75b-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="aa75b-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="aa75b-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="aa75b-113">Identificador de la instancia del controlador instalable.</span><span class="sxs-lookup"><span data-stu-id="aa75b-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="aa75b-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="aa75b-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="aa75b-115">32: valor de bit especificado como parámetro *lParam1* en una llamada a la función **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="aa75b-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="aa75b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="aa75b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="aa75b-117">32: valor de bit especificado como parámetro *lParam2* en una llamada a la función **DriverClose** .</span><span class="sxs-lookup"><span data-stu-id="aa75b-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa75b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa75b-118">Return Value</span></span>

<span data-ttu-id="aa75b-119">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="aa75b-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa75b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa75b-120">Requirements</span></span>



| <span data-ttu-id="aa75b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa75b-121">Requirement</span></span> | <span data-ttu-id="aa75b-122">Value</span><span class="sxs-lookup"><span data-stu-id="aa75b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa75b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa75b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aa75b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa75b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aa75b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa75b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aa75b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa75b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aa75b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa75b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa75b-128"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa75b-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa75b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa75b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa75b-130">Controladores instalables</span><span class="sxs-lookup"><span data-stu-id="aa75b-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="aa75b-131">Mensajes de controlador instalables</span><span class="sxs-lookup"><span data-stu-id="aa75b-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 






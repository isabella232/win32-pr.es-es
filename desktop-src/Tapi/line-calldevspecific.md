---
description: El mensaje CALLDEVSPECIFIC de la línea de TSPI \_ se envía a la función de devolución de llamada LINEEVENT para notificar a TAPI los eventos específicos del dispositivo que se producen en una llamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Mensaje de LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680182"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="73098-103">Mensaje de línea \_ CALLDEVSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="73098-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="73098-104">El mensaje **\_ CALLDEVSPECIFIC** de la línea de TSPI se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI los eventos específicos del dispositivo que se producen en una llamada.</span><span class="sxs-lookup"><span data-stu-id="73098-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="73098-105">El significado del mensaje y la interpretación de los parámetros de *dwParam1* a través de *dwParam3* son específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73098-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="73098-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73098-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="73098-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-108">El identificador de objeto opaco TAPI para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="73098-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="73098-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="73098-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-110">Identificador de objeto opaco TAPI para el dispositivo de llamada.</span><span class="sxs-lookup"><span data-stu-id="73098-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="73098-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="73098-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-112">La línea de valor \_ CALLDEVSPECIFIC.</span><span class="sxs-lookup"><span data-stu-id="73098-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="73098-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="73098-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-114">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73098-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="73098-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="73098-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-116">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73098-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="73098-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="73098-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="73098-118">Específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73098-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73098-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73098-119">Remarks</span></span>

<span data-ttu-id="73098-120">Un proveedor de servicios usa el mensaje **line \_ CALLDEVSPECIFIC** junto con la función [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="73098-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="73098-121">Su significado es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73098-121">Its meaning is device specific.</span></span>

<span data-ttu-id="73098-122">TAPI envía el mensaje [**line \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) a las aplicaciones en respuesta a la recepción de este mensaje de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="73098-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="73098-123">Los parámetros *htLine* y *htCall* se traducen a la *HCall* adecuada como el parámetro *hDevice* en el nivel de TAPI.</span><span class="sxs-lookup"><span data-stu-id="73098-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="73098-124">Los parámetros *dwParam1*, *dwParam2* y *dwParam3* se pasan sin modificar.</span><span class="sxs-lookup"><span data-stu-id="73098-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="73098-125">No hay ningún mensaje directamente correspondiente en el nivel de TAPI, aunque este mensaje es muy similar a la [**línea \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73098-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="73098-126">En el nivel de TSPI, los mensajes específicos del dispositivo se dividen entre los eventos de informes en líneas y direcciones, y los eventos de informes en llamadas.</span><span class="sxs-lookup"><span data-stu-id="73098-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="73098-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73098-127">Requirements</span></span>



| <span data-ttu-id="73098-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="73098-128">Requirement</span></span> | <span data-ttu-id="73098-129">Value</span><span class="sxs-lookup"><span data-stu-id="73098-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="73098-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="73098-130">TAPI version</span></span><br/> | <span data-ttu-id="73098-131">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="73098-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="73098-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73098-132">Header</span></span><br/>       | <dl> <span data-ttu-id="73098-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="73098-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73098-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="73098-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="73098-135">[**LÍNEA \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73098-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="73098-136">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="73098-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="73098-137">**TSPI \_ lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="73098-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 


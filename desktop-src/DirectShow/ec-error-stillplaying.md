---
description: Error de un comando asincrónico para ejecutar el gráfico.
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: EC_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679055"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="24129-103">\_STILLPLAYING de error de EC \_</span><span class="sxs-lookup"><span data-stu-id="24129-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="24129-104">Error de un comando asincrónico para ejecutar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="24129-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="24129-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24129-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24129-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="24129-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="24129-107">(**HRESULT**) Código de error de la operación en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="24129-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="24129-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="24129-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="24129-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="24129-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="24129-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="24129-110">Default Action</span></span>

<span data-ttu-id="24129-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24129-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="24129-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24129-112">Remarks</span></span>

<span data-ttu-id="24129-113">Si Filter Graph Manager emite un comando de ejecución asincrónico que produce un error, envía este evento a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24129-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="24129-114">El gráfico permanece en estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="24129-114">The graph remains in a running state.</span></span> <span data-ttu-id="24129-115">El estado de los filtros subyacentes es indeterminado.</span><span class="sxs-lookup"><span data-stu-id="24129-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="24129-116">Es posible que algunos filtros se estén ejecutando y otros no.</span><span class="sxs-lookup"><span data-stu-id="24129-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="24129-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24129-117">Requirements</span></span>



| <span data-ttu-id="24129-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24129-118">Requirement</span></span> | <span data-ttu-id="24129-119">Value</span><span class="sxs-lookup"><span data-stu-id="24129-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24129-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24129-120">Header</span></span><br/> | <dl> <span data-ttu-id="24129-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="24129-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24129-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="24129-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24129-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="24129-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="24129-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="24129-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





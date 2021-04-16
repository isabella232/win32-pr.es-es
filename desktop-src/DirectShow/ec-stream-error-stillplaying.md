---
description: Se produjo un error en una secuencia, pero la secuencia todavía se está reproduciendo.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679445"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="76472-103">\_STILLPLAYING de \_ error de secuencia de EC \_</span><span class="sxs-lookup"><span data-stu-id="76472-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="76472-104">Se produjo un error en una secuencia, pero la secuencia todavía se está reproduciendo.</span><span class="sxs-lookup"><span data-stu-id="76472-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="76472-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76472-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76472-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="76472-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="76472-107">(**HRESULT**) Código de error de la operación en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="76472-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="76472-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="76472-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="76472-109">(**DWORD**) Código de error secundario.</span><span class="sxs-lookup"><span data-stu-id="76472-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="76472-110">Este valor suele ser cero.</span><span class="sxs-lookup"><span data-stu-id="76472-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="76472-111">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="76472-111">Default Action</span></span>

<span data-ttu-id="76472-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="76472-112">None.</span></span> <span data-ttu-id="76472-113">La aplicación debe decidir si desea detener el gráfico.</span><span class="sxs-lookup"><span data-stu-id="76472-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="76472-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76472-114">Requirements</span></span>



| <span data-ttu-id="76472-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76472-115">Requirement</span></span> | <span data-ttu-id="76472-116">Value</span><span class="sxs-lookup"><span data-stu-id="76472-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76472-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76472-117">Header</span></span><br/> | <dl> <span data-ttu-id="76472-118"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="76472-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76472-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="76472-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76472-120">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="76472-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="76472-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="76472-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





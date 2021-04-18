---
description: El gráfico está almacenando en búfer datos o ha dejado de almacenar en búfer los datos.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680264"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="ff630-103">\_datos de almacenamiento en búfer de EC \_</span><span class="sxs-lookup"><span data-stu-id="ff630-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="ff630-104">El gráfico está almacenando en búfer datos o ha dejado de almacenar en búfer los datos.</span><span class="sxs-lookup"><span data-stu-id="ff630-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff630-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff630-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff630-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ff630-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ff630-107">(**Bool**) **True** si el gráfico se está empezando a almacenar en búfer, o **false** si el gráfico ha detenido el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="ff630-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="ff630-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ff630-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ff630-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="ff630-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ff630-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="ff630-110">Default Action</span></span>

<span data-ttu-id="ff630-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ff630-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff630-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff630-112">Remarks</span></span>

<span data-ttu-id="ff630-113">Un filtro puede enviar este evento si necesita almacenar en búfer los datos de un origen externo.</span><span class="sxs-lookup"><span data-stu-id="ff630-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="ff630-114">(Por ejemplo, podría estar cargando datos de una red). La aplicación puede usar este evento para ajustar su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff630-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff630-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff630-115">Requirements</span></span>



| <span data-ttu-id="ff630-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff630-116">Requirement</span></span> | <span data-ttu-id="ff630-117">Value</span><span class="sxs-lookup"><span data-stu-id="ff630-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff630-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff630-118">Header</span></span><br/> | <dl> <span data-ttu-id="ff630-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff630-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff630-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff630-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff630-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="ff630-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ff630-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ff630-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





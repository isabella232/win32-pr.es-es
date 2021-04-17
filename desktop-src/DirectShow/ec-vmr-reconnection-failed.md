---
description: Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico del descodificador de nivel superior.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680233"
---
# <a name="ec_vmr_reconnection_failed"></a><span data-ttu-id="90001-103">\_error de \_ reconexión de VMR de EC \_</span><span class="sxs-lookup"><span data-stu-id="90001-103">EC\_VMR\_RECONNECTION\_FAILED</span></span>

<span data-ttu-id="90001-104">Enviado por VMR-7 y VMR-9 cuando no pudo aceptar una solicitud de cambio de formato dinámico del descodificador de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="90001-104">Sent by the VMR-7 and the VMR-9 when it was unable to accept a dynamic format change request from the upstream decoder.</span></span>

## <a name="parameters"></a><span data-ttu-id="90001-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90001-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90001-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="90001-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="90001-107">(**HRESULT**) Código de estado devuelto por [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada de VMR que no pudo reconectar.</span><span class="sxs-lookup"><span data-stu-id="90001-107">(**HRESULT**) Status code returned from [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the VMR's input pin that failed the reconnection.</span></span>

</dd> <dt>

<span data-ttu-id="90001-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="90001-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="90001-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="90001-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90001-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90001-110">Remarks</span></span>

<span data-ttu-id="90001-111">Este evento se reenvía a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="90001-111">This event is forwarded to applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="90001-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90001-112">Requirements</span></span>



| <span data-ttu-id="90001-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="90001-113">Requirement</span></span> | <span data-ttu-id="90001-114">Value</span><span class="sxs-lookup"><span data-stu-id="90001-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90001-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90001-115">Header</span></span><br/> | <dl> <span data-ttu-id="90001-116"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="90001-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90001-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="90001-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90001-118">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="90001-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="90001-119">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="90001-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





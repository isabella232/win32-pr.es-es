---
description: Se anuló una operación debido a un error.
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8465825b93207059e5f2ea5f054deb7c3fd5619f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680921"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="a1978-103">ERRORABORTEX de EC \_</span><span class="sxs-lookup"><span data-stu-id="a1978-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="a1978-104">Se anuló una operación debido a un error.</span><span class="sxs-lookup"><span data-stu-id="a1978-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1978-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1978-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1978-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a1978-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a1978-107">**(HRESULT)** Código de error de la operación en la que se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="a1978-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="a1978-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a1978-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a1978-109">**(BSTR)** Cadena que contiene información adicional sobre el error.</span><span class="sxs-lookup"><span data-stu-id="a1978-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a1978-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="a1978-110">Default Action</span></span>

<span data-ttu-id="a1978-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a1978-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1978-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1978-112">Remarks</span></span>

<span data-ttu-id="a1978-113">El filtro de [origen de Windows Media](windows-media-source-filter.md) heredado envía este evento.</span><span class="sxs-lookup"><span data-stu-id="a1978-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="a1978-114">Los nuevos filtros no deben enviar este evento.</span><span class="sxs-lookup"><span data-stu-id="a1978-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1978-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1978-115">Requirements</span></span>



| <span data-ttu-id="a1978-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1978-116">Requirement</span></span> | <span data-ttu-id="a1978-117">Value</span><span class="sxs-lookup"><span data-stu-id="a1978-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1978-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1978-118">Header</span></span><br/> | <dl> <span data-ttu-id="a1978-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1978-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1978-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1978-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1978-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="a1978-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a1978-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1978-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





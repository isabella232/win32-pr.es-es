---
description: 'EC_ERRORABORTEX: se anuló una operación debido a un error.'
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3bf1e1f24f9d5b07312f542c1ce4ea671f601d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094613"
---
# <a name="ec_errorabortex"></a><span data-ttu-id="5e01b-103">\_ERROR DE ECABORTEX</span><span class="sxs-lookup"><span data-stu-id="5e01b-103">EC\_ERRORABORTEX</span></span>

<span data-ttu-id="5e01b-104">Se anuló una operación debido a un error.</span><span class="sxs-lookup"><span data-stu-id="5e01b-104">An operation was aborted because of an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e01b-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e01b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e01b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5e01b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5e01b-107">**(HRESULT)** Código de error de la operación que ha generado un error.</span><span class="sxs-lookup"><span data-stu-id="5e01b-107">**(HRESULT)** Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e01b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5e01b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5e01b-109">**(BSTR)** Cadena que contiene información de error adicional.</span><span class="sxs-lookup"><span data-stu-id="5e01b-109">**(BSTR)** String that contains additional error information.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5e01b-110">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="5e01b-110">Default Action</span></span>

<span data-ttu-id="5e01b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5e01b-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e01b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e01b-112">Remarks</span></span>

<span data-ttu-id="5e01b-113">El filtro origen [de Windows Media](windows-media-source-filter.md) heredado envía este evento.</span><span class="sxs-lookup"><span data-stu-id="5e01b-113">The legacy [Windows Media Source](windows-media-source-filter.md) filter sends this event.</span></span> <span data-ttu-id="5e01b-114">Los nuevos filtros no deben enviar este evento.</span><span class="sxs-lookup"><span data-stu-id="5e01b-114">New filters should not send this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e01b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e01b-115">Requirements</span></span>



| <span data-ttu-id="5e01b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e01b-116">Requirement</span></span> | <span data-ttu-id="5e01b-117">Value</span><span class="sxs-lookup"><span data-stu-id="5e01b-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e01b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e01b-118">Header</span></span><br/> | <dl> <span data-ttu-id="5e01b-119"><dt>Dshow.h</dt></span><span class="sxs-lookup"><span data-stu-id="5e01b-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e01b-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5e01b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e01b-121">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="5e01b-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5e01b-122">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="5e01b-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





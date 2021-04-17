---
description: Indica que el nivel parental del contenido del DVD creado está a punto de cambiar.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f6e1dbcbcb285f33b6ea2b99c59c5c82dae0ae03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653496"
---
# <a name="ec_dvd_parental_level_change"></a><span data-ttu-id="2e107-103">\_cambio de \_ nivel parental de DVD de \_ EC \_</span><span class="sxs-lookup"><span data-stu-id="2e107-103">EC\_DVD\_PARENTAL\_LEVEL\_CHANGE</span></span>

<span data-ttu-id="2e107-104">Indica que el nivel parental del contenido del DVD creado está a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="2e107-104">Signals that the parental level of the authored DVD content is about to change.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e107-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e107-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e107-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2e107-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2e107-107">Valor largo que representa el nuevo nivel parental establecido en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="2e107-107">LONG value representing the new parental level set in the player.</span></span>

</dd> <dt>

<span data-ttu-id="2e107-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2e107-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2e107-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="2e107-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e107-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e107-110">Remarks</span></span>

<span data-ttu-id="2e107-111">El filtro del [navegador de DVD](dvd-navigator-filter.md) no admite cambios de nivel parental durante el streaming en respuesta a los comandos de SetTmpPML de un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="2e107-111">The [DVD Navigator](dvd-navigator-filter.md) filter does not support parental level changes during streaming in response to SetTmpPML commands on a DVD disc.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e107-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e107-112">Requirements</span></span>



| <span data-ttu-id="2e107-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e107-113">Requirement</span></span> | <span data-ttu-id="2e107-114">Value</span><span class="sxs-lookup"><span data-stu-id="2e107-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e107-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e107-115">Header</span></span><br/> | <dl> <span data-ttu-id="2e107-116"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e107-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e107-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e107-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e107-118">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="2e107-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2e107-119">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="2e107-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2e107-120">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e107-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





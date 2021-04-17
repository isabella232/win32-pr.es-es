---
description: Indica que el conjunto disponible de métodos de interfaz IDvdControl2 ha cambiado.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653493"
---
# <a name="ec_dvd_valid_uops_change"></a><span data-ttu-id="7bab4-103">\_cambio de \_ \_ UOPS válido de DVD \_ de EC</span><span class="sxs-lookup"><span data-stu-id="7bab4-103">EC\_DVD\_VALID\_UOPS\_CHANGE</span></span>

<span data-ttu-id="7bab4-104">Indica que el conjunto disponible de métodos de interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7bab4-104">Signals that the available set of [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface methods has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bab4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bab4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bab4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7bab4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7bab4-107">Valor **DWORD** que contiene una combinación de cero o más marcas de la enumeración de [**\_ \_ marcas UOP válidas**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) .</span><span class="sxs-lookup"><span data-stu-id="7bab4-107">**DWORD** value that contains a combination of zero or more flags from the [**VALID\_UOP\_FLAG**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) enumeration.</span></span> <span data-ttu-id="7bab4-108">Los bits indican qué comandos de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) se deshabilitaron explícitamente en el disco DVD.</span><span class="sxs-lookup"><span data-stu-id="7bab4-108">The bits indicate which [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) commands were explicitly disabled by the DVD disc.</span></span>

</dd> <dt>

<span data-ttu-id="7bab4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7bab4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7bab4-110">Cero.</span><span class="sxs-lookup"><span data-stu-id="7bab4-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bab4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bab4-111">Remarks</span></span>

<span data-ttu-id="7bab4-112">Este evento indica únicamente las operaciones que el contenido del disco DVD deshabilita explícitamente. No garantiza que sea válido para llamar a métodos que no estén deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="7bab4-112">This event indicates only which operations are explicitly disabled by the content on the DVD disc. It does not guarantee that it is valid to call methods that are not disabled.</span></span> <span data-ttu-id="7bab4-113">Por ejemplo, si no hay botones presentes, el método [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) no funcionará, aunque el método no esté deshabilitado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="7bab4-113">For example, if no buttons are present, the [**IDvdControl2::ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) method won't work, even though the method is not explicitly disabled.</span></span>

<span data-ttu-id="7bab4-114">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="7bab4-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bab4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bab4-115">Requirements</span></span>



| <span data-ttu-id="7bab4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bab4-116">Requirement</span></span> | <span data-ttu-id="7bab4-117">Value</span><span class="sxs-lookup"><span data-stu-id="7bab4-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bab4-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bab4-118">Header</span></span><br/> | <dl> <span data-ttu-id="7bab4-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bab4-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bab4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bab4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bab4-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="7bab4-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7bab4-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="7bab4-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7bab4-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="7bab4-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Las \_ constantes de marcador de bits LINEANSWERMODE describen cómo se ve afectada una llamada activa existente en un dispositivo de línea respondiendo a otra llamada de oferta en la misma línea.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Constantes de LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681092"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="cde63-103">Constantes de LINEANSWERMODE \_</span><span class="sxs-lookup"><span data-stu-id="cde63-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="cde63-104">Las constantes de marcador de bits **LINEANSWERMODE \_** describen cómo se ve afectada una llamada activa existente en un dispositivo de línea respondiendo a otra llamada de *oferta* en la misma línea.</span><span class="sxs-lookup"><span data-stu-id="cde63-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="cde63-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**\_quitar LINEANSWERMODE**</span><span class="sxs-lookup"><span data-stu-id="cde63-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cde63-106">La llamada activa se quitará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cde63-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cde63-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE \_**</span><span class="sxs-lookup"><span data-stu-id="cde63-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cde63-108">La llamada activa se colocará automáticamente en espera.</span><span class="sxs-lookup"><span data-stu-id="cde63-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cde63-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="cde63-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cde63-110">Responder a otra llamada en la misma línea no tiene ningún efecto en la llamada activa existente en la línea.</span><span class="sxs-lookup"><span data-stu-id="cde63-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cde63-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cde63-111">Remarks</span></span>

<span data-ttu-id="cde63-112">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="cde63-112">No extensibility.</span></span> <span data-ttu-id="cde63-113">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="cde63-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="cde63-114">Si una llamada entra en (se ofrece) en el momento en que otra llamada ya está activa, la nueva llamada se conecta a mediante la invocación de [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="cde63-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="cde63-115">El efecto que tiene en la llamada activa existente depende de las capacidades del dispositivo de la línea.</span><span class="sxs-lookup"><span data-stu-id="cde63-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="cde63-116">La primera llamada puede no verse afectada, se puede quitar automáticamente o puede colocarse automáticamente en espera.</span><span class="sxs-lookup"><span data-stu-id="cde63-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde63-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde63-117">Requirements</span></span>



| <span data-ttu-id="cde63-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde63-118">Requirement</span></span> | <span data-ttu-id="cde63-119">Value</span><span class="sxs-lookup"><span data-stu-id="cde63-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cde63-120">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cde63-120">TAPI version</span></span><br/> | <span data-ttu-id="cde63-121">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="cde63-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cde63-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cde63-122">Header</span></span><br/>       | <dl> <span data-ttu-id="cde63-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde63-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 





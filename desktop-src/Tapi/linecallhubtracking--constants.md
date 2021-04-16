---
description: Las \_ constantes de marcador de bits LINECALLHUBTRACKING describen el tipo de seguimiento de centro de llamadas proporcionado.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Constantes de LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679549"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="cd05e-103">Constantes de LINECALLHUBTRACKING \_</span><span class="sxs-lookup"><span data-stu-id="cd05e-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="cd05e-104">Las constantes de marcador de bits **LINECALLHUBTRACKING \_** describen el tipo de seguimiento de centro de llamadas proporcionado.</span><span class="sxs-lookup"><span data-stu-id="cd05e-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="cd05e-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**</span><span class="sxs-lookup"><span data-stu-id="cd05e-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd05e-106">El seguimiento del centro de llamadas se proporciona en el nivel de llamada.</span><span class="sxs-lookup"><span data-stu-id="cd05e-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd05e-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="cd05e-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd05e-108">No se proporciona seguimiento del centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="cd05e-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cd05e-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**</span><span class="sxs-lookup"><span data-stu-id="cd05e-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cd05e-110">Se realiza un seguimiento de los centros de llamadas en el nivel de proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="cd05e-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="cd05e-111">No se informan los cambios de llamada por llamada.</span><span class="sxs-lookup"><span data-stu-id="cd05e-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd05e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd05e-112">Remarks</span></span>

<span data-ttu-id="cd05e-113">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="cd05e-113">No extensibility.</span></span> <span data-ttu-id="cd05e-114">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="cd05e-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="cd05e-115">Cuando se producen cambios en esta estructura de datos, se envía un mensaje de [**línea \_ CALLINFO**](line-callinfo.md) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cd05e-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="cd05e-116">Los parámetros de este mensaje son un identificador de la llamada y una indicación del elemento de información que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="cd05e-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="cd05e-117">La estructura de datos [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica qué tipo de seguimiento se proporciona.</span><span class="sxs-lookup"><span data-stu-id="cd05e-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd05e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd05e-118">Requirements</span></span>



| <span data-ttu-id="cd05e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd05e-119">Requirement</span></span> | <span data-ttu-id="cd05e-120">Value</span><span class="sxs-lookup"><span data-stu-id="cd05e-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cd05e-121">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="cd05e-121">TAPI version</span></span><br/> | <span data-ttu-id="cd05e-122">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="cd05e-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="cd05e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd05e-123">Header</span></span><br/>       | <dl> <span data-ttu-id="cd05e-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd05e-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd05e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd05e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd05e-126">**LÍNEA \_ CALLINFO**</span><span class="sxs-lookup"><span data-stu-id="cd05e-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="cd05e-127">**LINECALLHUBTRACKINGINFO**</span><span class="sxs-lookup"><span data-stu-id="cd05e-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="cd05e-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="cd05e-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 





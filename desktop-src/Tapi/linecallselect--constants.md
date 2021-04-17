---
description: Las \_ constantes de marcador de bits LINECALLSELECT describen qué llamadas se van a seleccionar.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes de LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681088"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="e3ddd-103">Constantes de LINECALLSELECT \_</span><span class="sxs-lookup"><span data-stu-id="e3ddd-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="e3ddd-104">Las constantes de marcador de bits **LINECALLSELECT \_** describen qué llamadas se van a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="e3ddd-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**Dirección de LINECALLSELECT \_**</span><span class="sxs-lookup"><span data-stu-id="e3ddd-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ddd-106">Selecciona la llamada en la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3ddd-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_llamada a LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="e3ddd-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ddd-108">Selecciona las llamadas relacionadas a la llamada especificada.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="e3ddd-109">Por ejemplo, las entidades de una llamada de conferencia.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3ddd-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**</span><span class="sxs-lookup"><span data-stu-id="e3ddd-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ddd-111">Selecciona las llamadas relacionadas al identificador de llamada especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="e3ddd-112">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3ddd-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**</span><span class="sxs-lookup"><span data-stu-id="e3ddd-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ddd-114">Selecciona llamadas en el identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="e3ddd-115">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="e3ddd-116">Las aplicaciones deben considerar el uso de la \_ constante de línea LINECALLSELECT en lugar de esta.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3ddd-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_línea LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="e3ddd-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ddd-118">Selecciona llamadas en el dispositivo de línea especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3ddd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3ddd-119">Remarks</span></span>

<span data-ttu-id="e3ddd-120">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-120">No extensibility.</span></span> <span data-ttu-id="e3ddd-121">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="e3ddd-122">Esta constante se usa en [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) y para especificar una selección (ámbito) de las llamadas que se solicitan.</span><span class="sxs-lookup"><span data-stu-id="e3ddd-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ddd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3ddd-123">Requirements</span></span>



| <span data-ttu-id="e3ddd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ddd-124">Requirement</span></span> | <span data-ttu-id="e3ddd-125">Value</span><span class="sxs-lookup"><span data-stu-id="e3ddd-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3ddd-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="e3ddd-126">TAPI version</span></span><br/> | <span data-ttu-id="e3ddd-127">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="e3ddd-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e3ddd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3ddd-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e3ddd-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ddd-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 





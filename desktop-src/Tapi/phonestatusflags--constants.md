---
description: Las \_ constantes de marcador de bits PHONESTATUSFLAGS describen una variedad de información de estado de dispositivo de teléfono.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes de PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679229"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="c764b-103">Constantes de PHONESTATUSFLAGS \_</span><span class="sxs-lookup"><span data-stu-id="c764b-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="c764b-104">Las constantes de marcador de bits **PHONESTATUSFLAGS \_** describen una variedad de información de estado de dispositivo de teléfono.</span><span class="sxs-lookup"><span data-stu-id="c764b-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="c764b-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="c764b-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c764b-106">Especifica si el teléfono está conectado actualmente a TAPI.</span><span class="sxs-lookup"><span data-stu-id="c764b-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="c764b-107">**True** si está conectado; en caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="c764b-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c764b-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspendido**</span><span class="sxs-lookup"><span data-stu-id="c764b-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c764b-109">Especifica si la manipulación de TAPI del dispositivo telefónico está suspendida.</span><span class="sxs-lookup"><span data-stu-id="c764b-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="c764b-110">**True** si se suspende, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c764b-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="c764b-111">El uso de una aplicación de un dispositivo telefónico se puede suspender temporalmente cuando el conmutador desea manipular el teléfono de forma que no pueda tolerar interferencias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c764b-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c764b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c764b-112">Remarks</span></span>

<span data-ttu-id="c764b-113">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="c764b-113">No extensibility.</span></span> <span data-ttu-id="c764b-114">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="c764b-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c764b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c764b-115">Requirements</span></span>



| <span data-ttu-id="c764b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c764b-116">Requirement</span></span> | <span data-ttu-id="c764b-117">Value</span><span class="sxs-lookup"><span data-stu-id="c764b-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c764b-118">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="c764b-118">TAPI version</span></span><br/> | <span data-ttu-id="c764b-119">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c764b-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c764b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c764b-120">Header</span></span><br/>       | <dl> <span data-ttu-id="c764b-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c764b-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 





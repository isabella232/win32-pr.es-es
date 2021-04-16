---
description: Las \_ constantes de marcador de bits LINETERMMODE describen distintos tipos de eventos en una línea telefónica que se pueden enrutar a un dispositivo terminal.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Constantes de LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679404"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="19ab4-103">Constantes de LINETERMMODE \_</span><span class="sxs-lookup"><span data-stu-id="19ab4-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="19ab4-104">Las constantes de marcador de bits **LINETERMMODE \_** describen distintos tipos de eventos en una línea telefónica que se pueden enrutar a un dispositivo terminal.</span><span class="sxs-lookup"><span data-stu-id="19ab4-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="19ab4-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**botones de LINETERMMODE \_**</span><span class="sxs-lookup"><span data-stu-id="19ab4-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-106">Se trata de eventos de pulsación de botones enviados desde el terminal a la línea.</span><span class="sxs-lookup"><span data-stu-id="19ab4-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE \_ Mostrar**</span><span class="sxs-lookup"><span data-stu-id="19ab4-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-108">Esta es la información que se envía desde la línea al terminal.</span><span class="sxs-lookup"><span data-stu-id="19ab4-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ conmutador**</span><span class="sxs-lookup"><span data-stu-id="19ab4-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-110">Se trata de eventos conmutador enviados desde el terminal a la línea.</span><span class="sxs-lookup"><span data-stu-id="19ab4-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lámparas LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="19ab4-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-112">Estos son los eventos de lámpara enviados desde la línea al terminal.</span><span class="sxs-lookup"><span data-stu-id="19ab4-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="19ab4-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-114">Este es el flujo multimedia bidireccional asociado a una llamada en la línea y el terminal.</span><span class="sxs-lookup"><span data-stu-id="19ab4-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="19ab4-115">Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada no se puede controlar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="19ab4-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**</span><span class="sxs-lookup"><span data-stu-id="19ab4-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-117">Esta es la secuencia de medios unidireccionales de la línea al terminal asociada a una llamada en la línea.</span><span class="sxs-lookup"><span data-stu-id="19ab4-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="19ab4-118">Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada puede controlarse de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="19ab4-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**</span><span class="sxs-lookup"><span data-stu-id="19ab4-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-120">Esta es la secuencia de medios unidireccionales desde el terminal hasta la línea asociada a una llamada en la línea.</span><span class="sxs-lookup"><span data-stu-id="19ab4-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="19ab4-121">Use este valor cuando el enrutamiento de ambos canales unidireccionales de una secuencia multimedia de una llamada puede controlarse de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="19ab4-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19ab4-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**\_timbre LINETERMMODE**</span><span class="sxs-lookup"><span data-stu-id="19ab4-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19ab4-123">Esta es la información de control de timbre enviada desde el conmutador al terminal.</span><span class="sxs-lookup"><span data-stu-id="19ab4-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19ab4-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19ab4-124">Remarks</span></span>

<span data-ttu-id="19ab4-125">Sin extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="19ab4-125">No extensibility.</span></span> <span data-ttu-id="19ab4-126">Todos los 32 bits están reservados.</span><span class="sxs-lookup"><span data-stu-id="19ab4-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="19ab4-127">Estas constantes describen las clases de secuencias de control e información que se pueden enrutar directamente entre un dispositivo de línea y un dispositivo de terminal (como un conjunto de teléfonos).</span><span class="sxs-lookup"><span data-stu-id="19ab4-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="19ab4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19ab4-128">Requirements</span></span>



| <span data-ttu-id="19ab4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="19ab4-129">Requirement</span></span> | <span data-ttu-id="19ab4-130">Value</span><span class="sxs-lookup"><span data-stu-id="19ab4-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="19ab4-131">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="19ab4-131">TAPI version</span></span><br/> | <span data-ttu-id="19ab4-132">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="19ab4-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="19ab4-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19ab4-133">Header</span></span><br/>       | <dl> <span data-ttu-id="19ab4-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ab4-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 





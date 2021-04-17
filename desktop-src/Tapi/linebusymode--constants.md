---
description: Las \_ constantes de marcador de bits LINEBUSYMODE describen diferentes señales de ocupación que el conmutador o la red pueden generar. Estas señales ocupadas suelen indicar que se está usando un recurso diferente necesario para realizar una llamada.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Constantes de LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681090"
---
# <a name="linebusymode_-constants"></a><span data-ttu-id="bd3de-104">Constantes de LINEBUSYMODE \_</span><span class="sxs-lookup"><span data-stu-id="bd3de-104">LINEBUSYMODE\_ Constants</span></span>

<span data-ttu-id="bd3de-105">Las constantes de marcador de bits **LINEBUSYMODE \_** describen diferentes señales de ocupación que el conmutador o la red pueden generar.</span><span class="sxs-lookup"><span data-stu-id="bd3de-105">The **LINEBUSYMODE\_** bit-flag constants describe different busy signals that the switch or network can generate.</span></span> <span data-ttu-id="bd3de-106">Estas señales ocupadas suelen indicar que se está usando un recurso diferente necesario para realizar una llamada.</span><span class="sxs-lookup"><span data-stu-id="bd3de-106">These busy signals typically indicate that a different resource that is required to make a call is currently in use.</span></span>

<dl> <dt>

<span data-ttu-id="bd3de-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_estación LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="bd3de-107"><span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**LINEBUSYMODE\_STATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bd3de-108">La señal ocupado indica que la estación de la entidad a la que se ha llamado está ocupada.</span><span class="sxs-lookup"><span data-stu-id="bd3de-108">The busy signal indicates that the called party's station is busy.</span></span> <span data-ttu-id="bd3de-109">Normalmente, se señala con un tono ocupado *normal* .</span><span class="sxs-lookup"><span data-stu-id="bd3de-109">This is usually signaled with a *normal* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bd3de-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_tronco LINEBUSYMODE**</span><span class="sxs-lookup"><span data-stu-id="bd3de-110"><span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bd3de-111">La señal ocupado indica que un tronco o circuito está ocupado.</span><span class="sxs-lookup"><span data-stu-id="bd3de-111">The busy signal indicates that a trunk or circuit is busy.</span></span> <span data-ttu-id="bd3de-112">Normalmente, se señala con un tono de uso *rápido* .</span><span class="sxs-lookup"><span data-stu-id="bd3de-112">This is usually signaled with a *fast* busy tone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bd3de-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="bd3de-113"><span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bd3de-114">Actualmente, el modo específico de la señal ocupado es desconocido, pero se puede conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="bd3de-114">The busy signal's specific mode is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bd3de-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="bd3de-115"><span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bd3de-116">El modo específico de la señal ocupado no está disponible y no se conocerá.</span><span class="sxs-lookup"><span data-stu-id="bd3de-116">The busy signal's specific mode is unavailable and will not become known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd3de-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd3de-117">Remarks</span></span>

<span data-ttu-id="bd3de-118">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd3de-118">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="bd3de-119">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="bd3de-119">The low-order 16 bits are reserved.</span></span>

> [!Note]  
> <span data-ttu-id="bd3de-120">Las señales ocupadas se pueden enviar como tonos inbandes o mensajes fuera de banda.</span><span class="sxs-lookup"><span data-stu-id="bd3de-120">Busy signals can be sent as inband tones or out-of-band messages.</span></span> <span data-ttu-id="bd3de-121">TAPI no realiza suposiciones sobre el mecanismo de señalización específico.</span><span class="sxs-lookup"><span data-stu-id="bd3de-121">TAPI makes no assumption about the specific signaling mechanism.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd3de-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3de-122">Requirements</span></span>



| <span data-ttu-id="bd3de-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd3de-123">Requirement</span></span> | <span data-ttu-id="bd3de-124">Value</span><span class="sxs-lookup"><span data-stu-id="bd3de-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bd3de-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="bd3de-125">TAPI version</span></span><br/> | <span data-ttu-id="bd3de-126">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="bd3de-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bd3de-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd3de-127">Header</span></span><br/>       | <dl> <span data-ttu-id="bd3de-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd3de-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 





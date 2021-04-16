---
description: Las \_ constantes de marcador de bits LINESPECIALINFO describen las señales de información especial que la red puede usar para notificar diversas operaciones de informes y de observación de la red.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Constantes de LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679405"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="4fc65-103">Constantes de LINESPECIALINFO \_</span><span class="sxs-lookup"><span data-stu-id="4fc65-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="4fc65-104">Las constantes de marcador de bits **LINESPECIALINFO \_** describen las señales de información especial que la red puede usar para notificar diversas operaciones de informes y de observación de la red.</span><span class="sxs-lookup"><span data-stu-id="4fc65-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="4fc65-105">Se trata de secuencias de tono codificadas especiales que se transmiten al principio de los anuncios grabados de aviso de red.</span><span class="sxs-lookup"><span data-stu-id="4fc65-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="4fc65-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**</span><span class="sxs-lookup"><span data-stu-id="4fc65-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fc65-107">Este tono de información especial precede a un número libre, AIS, un cambio de número de Centrex y una estación de no trabajo, código de acceso no marcado o marcado como mensaje de operador de interceptación manual (categoría de irregularidades del cliente).</span><span class="sxs-lookup"><span data-stu-id="4fc65-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="4fc65-108">LINESPECIALINFO \_ CUSTIRREG también se muestra cuando se rechaza la información de facturación y cuando la dirección marcada se bloquea en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="4fc65-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc65-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuito**</span><span class="sxs-lookup"><span data-stu-id="4fc65-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fc65-110">Este tono de información especial precede a un circuito no o un anuncio de emergencia (categoría bloqueo de tronco).</span><span class="sxs-lookup"><span data-stu-id="4fc65-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc65-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**reordenación de LINESPECIALINFO \_**</span><span class="sxs-lookup"><span data-stu-id="4fc65-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fc65-112">Este tono de información especial precede a un anuncio de reordenación (categoría de irregularidad del equipo).</span><span class="sxs-lookup"><span data-stu-id="4fc65-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="4fc65-113">\_También se muestra el reorden de LINESPECIALINFO cuando el teléfono se mantiene OffHook demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="4fc65-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc65-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="4fc65-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fc65-115">Los detalles sobre el tono de información especial no están disponibles y no serán conocidos.</span><span class="sxs-lookup"><span data-stu-id="4fc65-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4fc65-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="4fc65-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="4fc65-117">Actualmente, se desconocen los detalles del tono de información especial, pero se pueden conocer más adelante.</span><span class="sxs-lookup"><span data-stu-id="4fc65-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fc65-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fc65-118">Remarks</span></span>

<span data-ttu-id="4fc65-119">Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fc65-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="4fc65-120">Los 16 bits de orden inferior están reservados.</span><span class="sxs-lookup"><span data-stu-id="4fc65-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="4fc65-121">Los tonos de información especiales se definen para los mensajes de consulta y no se utilizan normalmente para fines de facturación o de supervisión.</span><span class="sxs-lookup"><span data-stu-id="4fc65-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc65-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc65-122">Requirements</span></span>



| <span data-ttu-id="4fc65-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc65-123">Requirement</span></span> | <span data-ttu-id="4fc65-124">Value</span><span class="sxs-lookup"><span data-stu-id="4fc65-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4fc65-125">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="4fc65-125">TAPI version</span></span><br/> | <span data-ttu-id="4fc65-126">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4fc65-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="4fc65-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fc65-127">Header</span></span><br/>       | <dl> <span data-ttu-id="4fc65-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fc65-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 





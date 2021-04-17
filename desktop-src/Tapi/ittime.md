---
description: La interfaz ITTime es una interfaz específica del proveedor para un objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Interfaz ITTime (Sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679372"
---
# <a name="ittime-interface"></a><span data-ttu-id="5b411-103">Interfaz ITTime</span><span class="sxs-lookup"><span data-stu-id="5b411-103">ITTime interface</span></span>

<span data-ttu-id="5b411-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b411-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5b411-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5b411-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5b411-106">La interfaz **ITTime** es una interfaz específica del proveedor para un objeto de BLOB de conferencia del Protocolo de descriptor de sesión (SDP).</span><span class="sxs-lookup"><span data-stu-id="5b411-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="5b411-107">Proporciona acceso a un conjunto de tiempos de activación para la sesión.</span><span class="sxs-lookup"><span data-stu-id="5b411-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="5b411-108">Los métodos [**IEnumTime:: Next**](ienumtime-next.md) y [**ITTimeCollection:: Create**](ittimecollection-create.md) crean la interfaz **ITTime** .</span><span class="sxs-lookup"><span data-stu-id="5b411-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5b411-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b411-109">Members</span></span>

<span data-ttu-id="5b411-110">La interfaz **ITTime** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5b411-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5b411-111">**ITTime** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5b411-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="5b411-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b411-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5b411-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b411-113">Methods</span></span>

<span data-ttu-id="5b411-114">La interfaz **ITTime** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5b411-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="5b411-115">Método</span><span class="sxs-lookup"><span data-stu-id="5b411-115">Method</span></span>                                         | <span data-ttu-id="5b411-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b411-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="5b411-117">**obtener \_ startTime**</span><span class="sxs-lookup"><span data-stu-id="5b411-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="5b411-118">Obtiene el valor de hora de inicio del NTP de 32 bits (Protocolo de tiempo de red).</span><span class="sxs-lookup"><span data-stu-id="5b411-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="5b411-119">**obtener \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="5b411-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="5b411-120">Obtiene el valor de hora de finalización de NTP.</span><span class="sxs-lookup"><span data-stu-id="5b411-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="5b411-121">**Put \_ startTime**</span><span class="sxs-lookup"><span data-stu-id="5b411-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="5b411-122">Establece el valor de hora de inicio de NTP de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5b411-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="5b411-123">**Put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="5b411-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="5b411-124">Establece el valor de hora de finalización de NTP.</span><span class="sxs-lookup"><span data-stu-id="5b411-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="5b411-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b411-125">Requirements</span></span>



| <span data-ttu-id="5b411-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b411-126">Requirement</span></span> | <span data-ttu-id="5b411-127">Value</span><span class="sxs-lookup"><span data-stu-id="5b411-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b411-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5b411-128">TAPI version</span></span><br/> | <span data-ttu-id="5b411-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5b411-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5b411-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b411-130">Header</span></span><br/>       | <dl> <span data-ttu-id="5b411-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b411-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b411-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b411-132">Library</span></span><br/>      | <dl> <span data-ttu-id="5b411-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b411-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5b411-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b411-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="5b411-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b411-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 


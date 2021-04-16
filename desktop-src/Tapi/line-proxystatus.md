---
description: El \_ mensaje line PROXYSTATUS se envía cuando los proxies disponibles cambian en una línea que la aplicación tiene abierta actualmente.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Mensaje de LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680251"
---
# <a name="line_proxystatus-message"></a><span data-ttu-id="40f44-103">Mensaje de línea \_ PROXYSTATUS</span><span class="sxs-lookup"><span data-stu-id="40f44-103">LINE\_PROXYSTATUS message</span></span>

<span data-ttu-id="40f44-104">El mensaje **line \_ PROXYSTATUS** se envía cuando los proxies disponibles cambian en una línea que la aplicación tiene abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="40f44-104">The **LINE\_PROXYSTATUS** message is sent when the available proxies change on a line that the application currently has open.</span></span>

<span data-ttu-id="40f44-105">TAPISRV genera este mensaje durante una función [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) mediante LINEPROXYSTATUS \_ Open y LINEPROXYSTATUS \_ ALLOPENFORACD o una función [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) mediante LINEPROXYSTATUS \_ Close (todas las [**\_ constantes de LINEPROXYSTATUS**](lineproxystatus--constants.md)).</span><span class="sxs-lookup"><span data-stu-id="40f44-105">TAPISRV generates this message during a [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) function using LINEPROXYSTATUS\_OPEN and LINEPROXYSTATUS\_ALLOPENFORACD or a [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) function using LINEPROXYSTATUS\_CLOSE (all [**LINEPROXYSTATUS\_ Constants**](lineproxystatus--constants.md)).</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="40f44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f44-107">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="40f44-107">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="40f44-108">Identificador de la aplicación para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="40f44-108">The application's handle to the line device.</span></span> <span data-ttu-id="40f44-109">Esto se relaciona con el controlador del agente.</span><span class="sxs-lookup"><span data-stu-id="40f44-109">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="40f44-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="40f44-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="40f44-111">Instancia de devolución de llamada proporcionada al abrir la línea.</span><span class="sxs-lookup"><span data-stu-id="40f44-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="40f44-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="40f44-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="40f44-113">Especifica el estado de la cola que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="40f44-113">Specifies the queue status that has changed.</span></span> <span data-ttu-id="40f44-114">Puede ser una o varias de las [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="40f44-114">Can be one or more of the [**LINEPROXYSTATUS\_ constants**](lineproxystatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="40f44-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="40f44-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="40f44-116">Si *dwParam1* se establece en LINEPROXYSTATUS \_ Open o LINEPROXYSTATUS \_ Close, *dwParam2* indica el tipo de solicitud de proxy relacionado, que es uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="40f44-116">If *dwParam1* is set to LINEPROXYSTATUS\_OPEN or LINEPROXYSTATUS\_CLOSE, *dwParam2* indicates the related proxy request type, which is one of the following:</span></span>

-   <span data-ttu-id="40f44-117">LINEPROXYREQUEST \_ SETAGENTGROUP</span><span class="sxs-lookup"><span data-stu-id="40f44-117">LINEPROXYREQUEST\_SETAGENTGROUP</span></span>
-   <span data-ttu-id="40f44-118">LINEPROXYREQUEST \_ SETAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="40f44-118">LINEPROXYREQUEST\_SETAGENTSTATE</span></span>
-   <span data-ttu-id="40f44-119">LINEPROXYREQUEST \_ SETAGENTACTIVITY</span><span class="sxs-lookup"><span data-stu-id="40f44-119">LINEPROXYREQUEST\_SETAGENTACTIVITY</span></span>
-   <span data-ttu-id="40f44-120">LINEPROXYREQUEST \_ GETAGENTCAPS</span><span class="sxs-lookup"><span data-stu-id="40f44-120">LINEPROXYREQUEST\_GETAGENTCAPS</span></span>
-   <span data-ttu-id="40f44-121">LINEPROXYREQUEST \_ GETAGENTSTATUS</span><span class="sxs-lookup"><span data-stu-id="40f44-121">LINEPROXYREQUEST\_GETAGENTSTATUS</span></span>
-   <span data-ttu-id="40f44-122">LINEPROXYREQUEST \_ AGENTSPECIFIC</span><span class="sxs-lookup"><span data-stu-id="40f44-122">LINEPROXYREQUEST\_AGENTSPECIFIC</span></span>
-   <span data-ttu-id="40f44-123">LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST</span><span class="sxs-lookup"><span data-stu-id="40f44-123">LINEPROXYREQUEST\_GETAGENTACTIVITYLIST</span></span>
-   <span data-ttu-id="40f44-124">LINEPROXYREQUEST \_ GETAGENTGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="40f44-124">LINEPROXYREQUEST\_GETAGENTGROUPLIST</span></span>
-   <span data-ttu-id="40f44-125">LINEPROXYREQUEST \_ CREATEAGENT</span><span class="sxs-lookup"><span data-stu-id="40f44-125">LINEPROXYREQUEST\_CREATEAGENT</span></span>
-   <span data-ttu-id="40f44-126">LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="40f44-126">LINEPROXYREQUEST\_SETAGENTMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="40f44-127">LINEPROXYREQUEST \_ GETAGENTINFO</span><span class="sxs-lookup"><span data-stu-id="40f44-127">LINEPROXYREQUEST\_GETAGENTINFO</span></span>
-   <span data-ttu-id="40f44-128">LINEPROXYREQUEST \_ CREATEAGENTSESSION</span><span class="sxs-lookup"><span data-stu-id="40f44-128">LINEPROXYREQUEST\_CREATEAGENTSESSION</span></span>
-   <span data-ttu-id="40f44-129">LINEPROXYREQUEST \_ GETAGENTSESSIONLIST</span><span class="sxs-lookup"><span data-stu-id="40f44-129">LINEPROXYREQUEST\_GETAGENTSESSIONLIST</span></span>
-   <span data-ttu-id="40f44-130">LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="40f44-130">LINEPROXYREQUEST\_SETAGENTSESSIONSTATE</span></span>
-   <span data-ttu-id="40f44-131">LINEPROXYREQUEST \_ GETAGENTSESSIONINFO</span><span class="sxs-lookup"><span data-stu-id="40f44-131">LINEPROXYREQUEST\_GETAGENTSESSIONINFO</span></span>
-   <span data-ttu-id="40f44-132">LINEPROXYREQUEST \_ GETQUEUELIST</span><span class="sxs-lookup"><span data-stu-id="40f44-132">LINEPROXYREQUEST\_GETQUEUELIST</span></span>
-   <span data-ttu-id="40f44-133">LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD</span><span class="sxs-lookup"><span data-stu-id="40f44-133">LINEPROXYREQUEST\_SETQUEUEMEASUREMENTPERIOD</span></span>
-   <span data-ttu-id="40f44-134">LINEPROXYREQUEST \_ GETQUEUEINFO</span><span class="sxs-lookup"><span data-stu-id="40f44-134">LINEPROXYREQUEST\_GETQUEUEINFO</span></span>
-   <span data-ttu-id="40f44-135">LINEPROXYREQUEST \_ GETGROUPLIST</span><span class="sxs-lookup"><span data-stu-id="40f44-135">LINEPROXYREQUEST\_GETGROUPLIST</span></span>
-   <span data-ttu-id="40f44-136">LINEPROXYREQUEST \_ SETAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="40f44-136">LINEPROXYREQUEST\_SETAGENTSTATEEX</span></span>

<span data-ttu-id="40f44-137">De lo contrario, *dwParam2* se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="40f44-137">Otherwise, *dwParam2* is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="40f44-138">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="40f44-138">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="40f44-139">Reservado.</span><span class="sxs-lookup"><span data-stu-id="40f44-139">Reserved.</span></span> <span data-ttu-id="40f44-140">Establecer en cero.</span><span class="sxs-lookup"><span data-stu-id="40f44-140">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40f44-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40f44-141">Requirements</span></span>



| <span data-ttu-id="40f44-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f44-142">Requirement</span></span> | <span data-ttu-id="40f44-143">Value</span><span class="sxs-lookup"><span data-stu-id="40f44-143">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="40f44-144">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="40f44-144">TAPI version</span></span><br/> | <span data-ttu-id="40f44-145">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="40f44-145">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="40f44-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40f44-146">Header</span></span><br/>       | <dl> <span data-ttu-id="40f44-147"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f44-147"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f44-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="40f44-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f44-149">**lineOpen**</span><span class="sxs-lookup"><span data-stu-id="40f44-149">**lineOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[<span data-ttu-id="40f44-150">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="40f44-150">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="40f44-151">**LÍNEA \_ PROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="40f44-151">**LINE\_PROXYREQUEST**</span></span>](line-proxyrequest.md)
</dt> <dt>

[<span data-ttu-id="40f44-152">**Constantes de LINEPROXYREQUEST \_**</span><span class="sxs-lookup"><span data-stu-id="40f44-152">**LINEPROXYREQUEST\_ Constants**</span></span>](lineproxyrequest--constants.md)
</dt> </dl>

 

 





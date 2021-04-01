---
title: Función RtmDequeueRouteChangeMessage (RTM. h)
description: La función RtmDequeueRouteChangeMessage devuelve el siguiente mensaje Route-Change en la cola asociada al cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- RtmDequeueRouteChangeMessage función RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150522"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="3c134-104">RtmDequeueRouteChangeMessage función)</span><span class="sxs-lookup"><span data-stu-id="3c134-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="3c134-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c134-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="3c134-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="3c134-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="3c134-107">La función **RtmDequeueRouteChangeMessage** devuelve el siguiente mensaje Route-Change en la cola asociada al cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="3c134-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c134-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c134-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="3c134-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c134-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c134-110">*ClientHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c134-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c134-111">Identificador que identifica el cliente para el que se realiza la operación.</span><span class="sxs-lookup"><span data-stu-id="3c134-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="3c134-112">Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="3c134-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c134-113">*Marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c134-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c134-114">Puntero a una variable **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3c134-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="3c134-115">El valor de esta variable se establece en el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="3c134-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="3c134-116">El valor especifica el tipo del mensaje de cambio y la información que se devolvió en los búferes proporcionados.</span><span class="sxs-lookup"><span data-stu-id="3c134-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="3c134-117">Este parámetro es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="3c134-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="3c134-118">Marcas</span><span class="sxs-lookup"><span data-stu-id="3c134-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="3c134-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3c134-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="3c134-120"><dt>**\_ruta RTM \_ agregada**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="3c134-121">La primera ruta se agregó para una red de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="3c134-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="3c134-122">El parámetro *CurBestRoute* apunta a la información de la ruta agregada.</span><span class="sxs-lookup"><span data-stu-id="3c134-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="3c134-123"><dt>**\_ruta RTM \_ eliminada**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="3c134-124">La única ruta disponible para una red de destino determinada se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="3c134-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="3c134-125">El parámetro *PrevBestRoute* apunta a la información de la ruta eliminada.</span><span class="sxs-lookup"><span data-stu-id="3c134-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="3c134-126"><dt>**\_ruta RTM \_ modificada**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="3c134-127">Se cambió al menos uno de los parámetros significativos para una mejor ruta a una red de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="3c134-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="3c134-128">Los parámetros significativos son:</span><span class="sxs-lookup"><span data-stu-id="3c134-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="3c134-129">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="3c134-129">Protocol identifier</span></span><br/> <span data-ttu-id="3c134-130">Índice de interfaz</span><span class="sxs-lookup"><span data-stu-id="3c134-130">Interface index</span></span><br/> <span data-ttu-id="3c134-131">Dirección de próximo salto</span><span class="sxs-lookup"><span data-stu-id="3c134-131">Next-hop address</span></span><br/> <span data-ttu-id="3c134-132">Datos específicos de la familia de protocolos (incluidas las métricas de ruta)</span><span class="sxs-lookup"><span data-stu-id="3c134-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="3c134-133">El parámetro *PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio.</span><span class="sxs-lookup"><span data-stu-id="3c134-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="3c134-134">El parámetro *CurBestRoute* apunta a la información de ruta actual (es decir, después de cambiar).</span><span class="sxs-lookup"><span data-stu-id="3c134-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="3c134-135">*CurBestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c134-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c134-136">Puntero a una estructura que recibe la información de la mejor ruta actual (si existe).</span><span class="sxs-lookup"><span data-stu-id="3c134-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="3c134-137">El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="3c134-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="3c134-138">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c134-138">This parameter is optional.</span></span> <span data-ttu-id="3c134-139">Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.</span><span class="sxs-lookup"><span data-stu-id="3c134-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="3c134-140">*PrevBestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3c134-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c134-141">Puntero a una estructura que recibe la información de la mejor ruta anterior, si existe.</span><span class="sxs-lookup"><span data-stu-id="3c134-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="3c134-142">El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="3c134-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="3c134-143">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c134-143">This parameter is optional.</span></span> <span data-ttu-id="3c134-144">Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta anterior.</span><span class="sxs-lookup"><span data-stu-id="3c134-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c134-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c134-145">Return value</span></span>

<span data-ttu-id="3c134-146">El valor devuelto es uno de los siguientes códigos.</span><span class="sxs-lookup"><span data-stu-id="3c134-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="3c134-147">Value</span><span class="sxs-lookup"><span data-stu-id="3c134-147">Value</span></span>                                                                                                       | <span data-ttu-id="3c134-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c134-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c134-149"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="3c134-150">Este mensaje era el último mensaje de la cola del cliente.</span><span class="sxs-lookup"><span data-stu-id="3c134-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="3c134-151">Se restablece el objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="3c134-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="3c134-152"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="3c134-153">El parámetro *ClientHandle* no es un identificador válido o, en el registro, el cliente no proporcionó un objeto de evento para la notificación de cambio de mensaje (vea [**RtmRegisterClient**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="3c134-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="3c134-154"><dt>**\_más \_ mensajes de error**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="3c134-155">La cola del cliente contiene mensajes adicionales.</span><span class="sxs-lookup"><span data-stu-id="3c134-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="3c134-156">El cliente debe volver a llamar a **RtmDequeueRouteChangeMessage** tan pronto como sea posible para permitir que el administrador de tablas de enrutamiento libere los recursos asociados a los mensajes pendientes.</span><span class="sxs-lookup"><span data-stu-id="3c134-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="3c134-157"><dt>**\_no hay \_ mensajes de error**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="3c134-158">La cola del cliente no contiene ningún mensaje; no se solicitó la llamada.</span><span class="sxs-lookup"><span data-stu-id="3c134-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="3c134-159">Se restablece el evento.</span><span class="sxs-lookup"><span data-stu-id="3c134-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="3c134-160"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="3c134-161">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3c134-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="3c134-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c134-162">Requirements</span></span>



| <span data-ttu-id="3c134-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c134-163">Requirement</span></span> | <span data-ttu-id="3c134-164">Value</span><span class="sxs-lookup"><span data-stu-id="3c134-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c134-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c134-165">Minimum supported client</span></span><br/> | <span data-ttu-id="3c134-166">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3c134-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3c134-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c134-167">Minimum supported server</span></span><br/> | <span data-ttu-id="3c134-168">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c134-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c134-169">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3c134-169">End of server support</span></span><br/>    | <span data-ttu-id="3c134-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c134-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="3c134-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c134-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c134-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c134-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c134-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c134-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c134-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c134-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c134-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c134-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c134-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c134-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c134-178">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="3c134-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="3c134-179">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="3c134-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="3c134-180">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="3c134-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 






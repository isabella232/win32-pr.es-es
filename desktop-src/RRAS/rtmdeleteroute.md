---
title: Función RtmDeleteRoute (RTM. h)
description: La función RtmDeleteRoute elimina una entrada de ruta.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- RtmDeleteRoute función RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996618"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="15827-104">RtmDeleteRoute función)</span><span class="sxs-lookup"><span data-stu-id="15827-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="15827-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15827-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="15827-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="15827-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="15827-107">La función **RtmDeleteRoute** elimina una entrada de ruta.</span><span class="sxs-lookup"><span data-stu-id="15827-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="15827-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15827-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="15827-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15827-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15827-110">*ClientHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="15827-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15827-111">Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento de la ruta agregada o actualizada.</span><span class="sxs-lookup"><span data-stu-id="15827-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="15827-112">Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="15827-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="15827-113">*Ruta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="15827-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15827-114">Puntero a una estructura específica de la familia de protocolos que especifica la ruta nueva o actualizada.</span><span class="sxs-lookup"><span data-stu-id="15827-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="15827-115">El administrador de tablas de enrutamiento usa los campos siguientes para actualizar la tabla de enrutamiento:</span><span class="sxs-lookup"><span data-stu-id="15827-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="15827-116">Value</span><span class="sxs-lookup"><span data-stu-id="15827-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="15827-117">Significado</span><span class="sxs-lookup"><span data-stu-id="15827-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="15827-118"><dt>**\_Red RR**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="15827-119">Especifica el número de red de destino.</span><span class="sxs-lookup"><span data-stu-id="15827-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="15827-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="15827-121">Especifica el índice de la interfaz a través de la cual se recibió la ruta.</span><span class="sxs-lookup"><span data-stu-id="15827-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="15827-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="15827-123">Especifica la dirección de red del enrutador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="15827-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="15827-124">*Marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="15827-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15827-125">Puntero a un conjunto de marcas que indican el tipo del mensaje de cambio y qué información se colocó en los búferes proporcionados.</span><span class="sxs-lookup"><span data-stu-id="15827-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="15827-126">Este parámetro es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="15827-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="15827-127">Marcas</span><span class="sxs-lookup"><span data-stu-id="15827-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="15827-128">Significado</span><span class="sxs-lookup"><span data-stu-id="15827-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="15827-129"><dt>**RTM \_ sin \_ cambios**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="15827-130">La eliminación de la ruta no afectó a la mejor ruta a ninguna red de destino.</span><span class="sxs-lookup"><span data-stu-id="15827-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="15827-131">En otras palabras, otra entrada representa una ruta a la misma red de destino y tiene una métrica inferior.</span><span class="sxs-lookup"><span data-stu-id="15827-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="15827-132"><dt>**\_ruta RTM \_ eliminada**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="15827-133">La ruta eliminada era la única ruta disponible para una red de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="15827-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="15827-134"><dt>**\_ruta RTM \_ modificada**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="15827-135">Una vez eliminada esta ruta, otra ruta se convirtió en la mejor ruta a una red de destino determinada.</span><span class="sxs-lookup"><span data-stu-id="15827-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="15827-136">*CurBestRoute* apunta a la información de la nueva ruta más adecuada.</span><span class="sxs-lookup"><span data-stu-id="15827-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="15827-137">*CurBestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="15827-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15827-138">Puntero a una estructura que recibe la información de la mejor ruta actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="15827-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="15827-139">El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="15827-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="15827-140">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="15827-140">This parameter is optional.</span></span> <span data-ttu-id="15827-141">Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.</span><span class="sxs-lookup"><span data-stu-id="15827-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15827-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15827-142">Return value</span></span>

<span data-ttu-id="15827-143">Si la función se ejecuta correctamente, el valor devuelto **no es un \_ error**.</span><span class="sxs-lookup"><span data-stu-id="15827-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="15827-144">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="15827-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="15827-145">Value</span><span class="sxs-lookup"><span data-stu-id="15827-145">Value</span></span>                                                                                                       | <span data-ttu-id="15827-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="15827-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="15827-147"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="15827-148">El parámetro de identificador de cliente no es un identificador válido.</span><span class="sxs-lookup"><span data-stu-id="15827-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="15827-149"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="15827-150">La estructura de ruta señalada por el parámetro *Route* contiene un valor de miembro.</span><span class="sxs-lookup"><span data-stu-id="15827-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="15827-151"><dt>**ERROR no se trata de una \_ \_ \_ ruta**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="15827-152">No hay ninguna entrada en la tabla de enrutamiento que coincida con los parámetros de la ruta especificada.</span><span class="sxs-lookup"><span data-stu-id="15827-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="15827-153"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15827-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="15827-154">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="15827-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="15827-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15827-155">Remarks</span></span>

<span data-ttu-id="15827-156">La función genera un mensaje de cambio de ruta si la mejor ruta a una red de destino ha cambiado como resultado de la eliminación.</span><span class="sxs-lookup"><span data-stu-id="15827-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="15827-157">Sin embargo, el mensaje de cambio de ruta no se envía al cliente que realiza esta llamada.</span><span class="sxs-lookup"><span data-stu-id="15827-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="15827-158">En su lugar, esta función devuelve directamente la información relevante a ese cliente.</span><span class="sxs-lookup"><span data-stu-id="15827-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="15827-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15827-159">Requirements</span></span>



| <span data-ttu-id="15827-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="15827-160">Requirement</span></span> | <span data-ttu-id="15827-161">Value</span><span class="sxs-lookup"><span data-stu-id="15827-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15827-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15827-162">Minimum supported client</span></span><br/> | <span data-ttu-id="15827-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="15827-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="15827-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15827-164">Minimum supported server</span></span><br/> | <span data-ttu-id="15827-165">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="15827-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15827-166">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="15827-166">End of server support</span></span><br/>    | <span data-ttu-id="15827-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="15827-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="15827-168">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15827-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="15827-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="15827-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="15827-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15827-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="15827-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15827-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="15827-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15827-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15827-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15827-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15827-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="15827-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15827-175">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="15827-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="15827-176">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="15827-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="15827-177">**RtmAddRoute**</span><span class="sxs-lookup"><span data-stu-id="15827-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="15827-178">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="15827-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 






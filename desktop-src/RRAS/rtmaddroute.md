---
title: Función RtmAddRoute (RTM. h)
description: La función RtmAddRoute agrega una entrada de ruta o actualiza una entrada de ruta existente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- RtmAddRoute función RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676834"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="e7594-104">RtmAddRoute función)</span><span class="sxs-lookup"><span data-stu-id="e7594-104">RtmAddRoute function</span></span>

<span data-ttu-id="e7594-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e7594-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e7594-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="e7594-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e7594-107">La función **RtmAddRoute** agrega una entrada de ruta o actualiza una entrada de ruta existente.</span><span class="sxs-lookup"><span data-stu-id="e7594-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7594-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7594-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="e7594-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7594-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7594-110">*ClientHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7594-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-111">Identificador que identifica al cliente y, por tanto, el protocolo de enrutamiento, que agregó o actualizó la ruta.</span><span class="sxs-lookup"><span data-stu-id="e7594-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="e7594-112">Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="e7594-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7594-113">*Ruta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e7594-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-114">Puntero a una estructura específica de la familia de protocolos que especifica la ruta nueva o actualizada.</span><span class="sxs-lookup"><span data-stu-id="e7594-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="e7594-115">El administrador de tablas de enrutamiento usa los campos siguientes para actualizar la tabla de enrutamiento:</span><span class="sxs-lookup"><span data-stu-id="e7594-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="e7594-116">Value</span><span class="sxs-lookup"><span data-stu-id="e7594-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="e7594-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e7594-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="e7594-118"><dt>**\_Red RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="e7594-119">Especifica el número de red de destino.</span><span class="sxs-lookup"><span data-stu-id="e7594-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="e7594-120"><dt>**RR \_ InterfaceID**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="e7594-121">Especifica el índice de la interfaz a través de la cual se recibió la ruta.</span><span class="sxs-lookup"><span data-stu-id="e7594-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="e7594-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="e7594-123">Especifica la dirección del enrutador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="e7594-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="e7594-124"><dt>**RR \_ FamilySpecificData**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="e7594-125">Especifica datos que son específicos de la familia de protocolos.</span><span class="sxs-lookup"><span data-stu-id="e7594-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="e7594-126">Aunque los datos son transparentes para el administrador de tablas de enrutamiento, se tienen en cuenta cuando se comparan las rutas para determinar si ha cambiado la información de ruta.</span><span class="sxs-lookup"><span data-stu-id="e7594-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="e7594-127">Los datos también se usan para establecer valores de métricas que son independientes del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="e7594-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="e7594-128">Por consiguiente, estos datos se usan para determinar la mejor ruta para la red de destino.</span><span class="sxs-lookup"><span data-stu-id="e7594-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="e7594-129"><dt>**RR \_ ProtocolSpecificData**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="e7594-130">Especifica los datos específicos del Protocolo de enrutamiento que proporcionó la ruta.</span><span class="sxs-lookup"><span data-stu-id="e7594-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="e7594-131"><dt>**Marca de tiempo de RR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="e7594-132">Especifica la hora actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="e7594-132">Specifies the current system time.</span></span> <span data-ttu-id="e7594-133">Este campo lo establece el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="e7594-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="e7594-134">*TimeToLive* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7594-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-135">Especifica el número de segundos que la ruta especificada debe mantenerse en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="e7594-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="e7594-136">Si este parámetro se establece en Infinite, la ruta se mantiene hasta que se elimina explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e7594-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="e7594-137">El límite actual de *timeToLive* es de 2147483 segundos (24 + días).</span><span class="sxs-lookup"><span data-stu-id="e7594-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="e7594-138">*Marcas* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7594-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-139">Puntero a una variable **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e7594-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="e7594-140">El valor de esta variable se establece en el administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="e7594-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="e7594-141">El valor indica el tipo de cambio y la información que se devolvió en los búferes proporcionados.</span><span class="sxs-lookup"><span data-stu-id="e7594-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="e7594-142">Este parámetro es uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7594-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="e7594-143">Marcas</span><span class="sxs-lookup"><span data-stu-id="e7594-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="e7594-144">Significado</span><span class="sxs-lookup"><span data-stu-id="e7594-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="e7594-145"><dt>**RTM \_ sin \_ cambios**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="e7594-146">La adición o actualización no cambió ninguno de los parámetros de ruta significativos, o bien la entrada de ruta afectada no es la mejor ruta entre las entradas de la red de destino.</span><span class="sxs-lookup"><span data-stu-id="e7594-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="e7594-147"><dt>**\_ruta RTM \_ agregada**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="e7594-148">La ruta se agregó para la red de destino.</span><span class="sxs-lookup"><span data-stu-id="e7594-148">The route was added for the destination network.</span></span> <span data-ttu-id="e7594-149">El parámetro *CurBestRoute* apunta a la información de la ruta agregada.</span><span class="sxs-lookup"><span data-stu-id="e7594-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="e7594-150"><dt>**\_ruta RTM \_ modificada**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="e7594-151">Se cambió al menos uno de los parámetros significativos para la mejor ruta a la red de destino.</span><span class="sxs-lookup"><span data-stu-id="e7594-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="e7594-152">Los parámetros significativos son:</span><span class="sxs-lookup"><span data-stu-id="e7594-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="e7594-153">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="e7594-153">Protocol identifier</span></span><br/> <span data-ttu-id="e7594-154">Índice de interfaz</span><span class="sxs-lookup"><span data-stu-id="e7594-154">Interface index</span></span><br/> <span data-ttu-id="e7594-155">Dirección de próximo salto</span><span class="sxs-lookup"><span data-stu-id="e7594-155">Next-hop address</span></span><br/> <span data-ttu-id="e7594-156">Datos específicos de la familia de protocolos (incluidas las métricas de ruta)</span><span class="sxs-lookup"><span data-stu-id="e7594-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="e7594-157">El parámetro *PrevBestRoute* apunta a la información de ruta tal como estaba antes del cambio.</span><span class="sxs-lookup"><span data-stu-id="e7594-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="e7594-158">El parámetro *CurBestRoute* apunta a la información de ruta actual (es decir, después de cambiar).</span><span class="sxs-lookup"><span data-stu-id="e7594-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="e7594-159">*CurBestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7594-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-160">Puntero a una estructura que recibe la información de la mejor ruta actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="e7594-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="e7594-161">El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="e7594-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="e7594-162">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="e7594-162">This parameter is optional.</span></span> <span data-ttu-id="e7594-163">Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta actual.</span><span class="sxs-lookup"><span data-stu-id="e7594-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="e7594-164">*PrevBestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7594-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7594-165">Puntero a una estructura que recibe la información de la mejor ruta anterior, si existe.</span><span class="sxs-lookup"><span data-stu-id="e7594-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="e7594-166">El tipo de la estructura es específico de la familia de protocolos, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="e7594-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="e7594-167">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="e7594-167">This parameter is optional.</span></span> <span data-ttu-id="e7594-168">Si el autor de la llamada especifica **null** para este parámetro, no se devuelve la información de la mejor ruta anterior.</span><span class="sxs-lookup"><span data-stu-id="e7594-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7594-169">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7594-169">Return value</span></span>

<span data-ttu-id="e7594-170">El valor devuelto es uno de los siguientes códigos.</span><span class="sxs-lookup"><span data-stu-id="e7594-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="e7594-171">Value</span><span class="sxs-lookup"><span data-stu-id="e7594-171">Value</span></span>                                                                                                       | <span data-ttu-id="e7594-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7594-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7594-173"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="e7594-174">La ruta se agregó o actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e7594-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="e7594-175"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="e7594-176">El parámetro de identificador de cliente no es un identificador válido.</span><span class="sxs-lookup"><span data-stu-id="e7594-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="e7594-177"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="e7594-178">La estructura de ruta contiene un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e7594-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="e7594-179"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="e7594-180">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="e7594-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e7594-181"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="e7594-182">No hay memoria suficiente para asignar la entrada de ruta.</span><span class="sxs-lookup"><span data-stu-id="e7594-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e7594-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7594-183">Remarks</span></span>

<span data-ttu-id="e7594-184">La función genera un mensaje de cambio de ruta si la mejor ruta a una red de destino ha cambiado como resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="e7594-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="e7594-185">Sin embargo, el mensaje de cambio de ruta no se envía al cliente que realiza esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e7594-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="e7594-186">En su lugar, esta función devuelve directamente información relevante a ese cliente a través de los parámetros *Flags*, *CurBestRoute* y *PrevBestRoute* .</span><span class="sxs-lookup"><span data-stu-id="e7594-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7594-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7594-187">Requirements</span></span>



| <span data-ttu-id="e7594-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7594-188">Requirement</span></span> | <span data-ttu-id="e7594-189">Value</span><span class="sxs-lookup"><span data-stu-id="e7594-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7594-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7594-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e7594-191">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e7594-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e7594-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7594-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e7594-193">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7594-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7594-194">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e7594-194">End of server support</span></span><br/>    | <span data-ttu-id="e7594-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7594-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="e7594-196">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7594-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7594-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7594-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7594-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7594-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7594-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7594-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7594-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7594-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7594-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7594-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7594-203">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="e7594-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e7594-204">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="e7594-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="e7594-205">**RtmDeleteRoute**</span><span class="sxs-lookup"><span data-stu-id="e7594-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="e7594-206">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="e7594-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 






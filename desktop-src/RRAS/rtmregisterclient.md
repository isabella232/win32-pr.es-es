---
title: Función RtmRegisterClient (RTM. h)
description: La función RtmRegisterClient registra un cliente como un controlador del protocolo especificado. Establece un mecanismo de notificación de cambio de ruta para el cliente y establece las opciones de protocolo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- RtmRegisterClient función RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803482"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="3c2ba-105">RtmRegisterClient función)</span><span class="sxs-lookup"><span data-stu-id="3c2ba-105">RtmRegisterClient function</span></span>

<span data-ttu-id="3c2ba-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="3c2ba-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="3c2ba-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="3c2ba-108">La función **RtmRegisterClient** registra un cliente como un controlador del protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="3c2ba-109">Establece un mecanismo de notificación de cambio de ruta para el cliente y establece las opciones de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2ba-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c2ba-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="3c2ba-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c2ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2ba-112">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c2ba-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ba-113">Especifica la familia de protocolos del Protocolo de enrutamiento que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="3c2ba-114">*RoutingProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c2ba-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ba-115">Especifica el identificador del Protocolo de enrutamiento, el mismo que se usa al registrar con el administrador de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="3c2ba-116">Vea [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="3c2ba-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="3c2ba-117">*ChangeEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c2ba-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ba-118">Especifica que ha cambiado la mejor ruta a una red de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="3c2ba-119">El administrador de tablas de enrutamiento señala este evento después de un cambio en la mejor ruta a cualquier red de la tabla.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="3c2ba-120">Consulte [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) para obtener más información acerca de la notificación de cambio de ruta.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="3c2ba-121">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-121">This parameter is optional.</span></span> <span data-ttu-id="3c2ba-122">Si el autor de la llamada especifica **null** para este parámetro, el administrador de tabla de enrutamiento no notifica al cliente los cambios en el mejor estado de la ruta.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="3c2ba-123">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3c2ba-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ba-124">Especifica varias opciones para el control especial del Protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="3c2ba-125">Actualmente se admite el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-125">The following value is currently supported.</span></span>



| <span data-ttu-id="3c2ba-126">Marcas</span><span class="sxs-lookup"><span data-stu-id="3c2ba-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="3c2ba-127">Significado</span><span class="sxs-lookup"><span data-stu-id="3c2ba-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="3c2ba-128"><dt>**\_Protocolo RTM \_ , \_ ruta única**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="3c2ba-129">El administrador de tablas de enrutamiento solo mantiene una ruta por red de destino para el protocolo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="3c2ba-130">En otras palabras, el administrador de tablas de enrutamiento reemplaza las entradas de ruta que tienen los mismos números de red de destino en lugar de agregar otras nuevas.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2ba-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c2ba-131">Return value</span></span>

<span data-ttu-id="3c2ba-132">Valor de **identificador** que identifica el cliente en llamadas posteriores al administrador de tabla de enrutamiento, si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="3c2ba-133">Un identificador **nulo** indica que el administrador de tabla de enrutamiento no pudo registrar el cliente.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="3c2ba-134">Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener la razón del error.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="3c2ba-135">Value</span><span class="sxs-lookup"><span data-stu-id="3c2ba-135">Value</span></span>                                                                                                         | <span data-ttu-id="3c2ba-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c2ba-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c2ba-137"><dt>**el \_ cliente de error \_ ya \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="3c2ba-138">Otro cliente ya se ha registrado para controlar el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="3c2ba-139"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="3c2ba-140">La familia de protocolos especificada no es compatible o el parámetro *Flags* no es válido.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="3c2ba-141"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="3c2ba-142">Recursos insuficientes para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3c2ba-143"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="3c2ba-144">Memoria insuficiente para asignar estructuras de datos para el cliente.</span><span class="sxs-lookup"><span data-stu-id="3c2ba-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="3c2ba-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c2ba-145">Requirements</span></span>



| <span data-ttu-id="3c2ba-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c2ba-146">Requirement</span></span> | <span data-ttu-id="3c2ba-147">Value</span><span class="sxs-lookup"><span data-stu-id="3c2ba-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ba-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c2ba-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ba-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3c2ba-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3c2ba-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c2ba-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ba-151">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c2ba-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c2ba-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3c2ba-152">End of server support</span></span><br/>    | <span data-ttu-id="3c2ba-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3c2ba-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="3c2ba-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c2ba-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2ba-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c2ba-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c2ba-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c2ba-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c2ba-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ba-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ba-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ba-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2ba-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c2ba-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2ba-161">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="3c2ba-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="3c2ba-162">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="3c2ba-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="3c2ba-163">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="3c2ba-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="3c2ba-164">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="3c2ba-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="3c2ba-165">Identificadores de la familia del protocolo RTMv1</span><span class="sxs-lookup"><span data-stu-id="3c2ba-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="3c2ba-166">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="3c2ba-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="3c2ba-167">**RtmDeregisterClient**</span><span class="sxs-lookup"><span data-stu-id="3c2ba-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 


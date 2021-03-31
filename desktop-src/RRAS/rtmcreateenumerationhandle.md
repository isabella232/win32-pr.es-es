---
title: Función RtmCreateEnumerationHandle (RTM. h)
description: La función RtmCreateEnumerationHandle devuelve un identificador que se utiliza con RtmEnumerateGetNextRoute para examinar todas las rutas, o un subconjunto de rutas, conocido por el administrador de tabla de enrutamiento.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- RtmCreateEnumerationHandle función RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150011"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="5643c-104">RtmCreateEnumerationHandle función)</span><span class="sxs-lookup"><span data-stu-id="5643c-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="5643c-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5643c-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5643c-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="5643c-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5643c-107">La función **RtmCreateEnumerationHandle** devuelve un identificador que se utiliza con [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) para examinar todas las rutas, o un subconjunto de rutas, conocido por el administrador de tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="5643c-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="5643c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5643c-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="5643c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5643c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5643c-110">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5643c-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5643c-111">Especifica la familia de protocolos de las rutas que se van a enumerar.</span><span class="sxs-lookup"><span data-stu-id="5643c-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="5643c-112">*EnumerationFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5643c-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5643c-113">Especifica las rutas que se deben enumerar.</span><span class="sxs-lookup"><span data-stu-id="5643c-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="5643c-114">Este parámetro limita el conjunto de rutas devueltas por la API de enumeración a un subconjunto definido por los siguientes marcadores y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="5643c-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="5643c-115">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5643c-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="5643c-116">EnumerationFlags</span><span class="sxs-lookup"><span data-stu-id="5643c-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="5643c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="5643c-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="5643c-118"><dt>**RTM \_ solo \_ esta \_ red**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="5643c-119">Enumerar solo las rutas que tienen el mismo número de red que el \_ miembro de red RR de la estructura a la que apunta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="5643c-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="5643c-120"><dt>**RTM \_ solo \_ esta \_ interfaz**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="5643c-121">Enumerar solo las rutas obtenidas a través de la interfaz especificada por el \_ campo RR InterfaceID de la estructura a la que apunta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="5643c-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="5643c-122"><dt>**RTM \_ solo \_ este \_ Protocolo**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="5643c-123">Enumerar solo las rutas agregadas por el protocolo de enrutamiento especificado por el \_ campo RR RoutingProtocol de la estructura a la que apunta CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="5643c-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="5643c-124"><dt>**\_solo las \_ mejores \_ rutas de RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="5643c-125">Enumerar solo las mejores rutas a cada una de las redes del conjunto.</span><span class="sxs-lookup"><span data-stu-id="5643c-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="5643c-126">*CriteriaRoute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5643c-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5643c-127">Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="5643c-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="5643c-128">Los valores de miembro de esta estructura corresponden a las marcas especificadas por el parámetro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="5643c-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5643c-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5643c-129">Return value</span></span>

<span data-ttu-id="5643c-130">Si la función se ejecuta correctamente, el valor devuelto es un **identificador** que se va a usar con llamadas de enumeración posteriores.</span><span class="sxs-lookup"><span data-stu-id="5643c-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="5643c-131">Si se produce un error en la función o no existe ninguna ruta con los criterios especificados, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="5643c-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="5643c-132">Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5643c-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="5643c-133">Value</span><span class="sxs-lookup"><span data-stu-id="5643c-133">Value</span></span>                                                                                                       | <span data-ttu-id="5643c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="5643c-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5643c-135"><dt>**ERROR \_ sin \_ rutas**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="5643c-136">No hay ninguna ruta que tenga los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="5643c-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5643c-137"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="5643c-138">Uno o varios de los parámetros de entrada no son válidos (por ejemplo, una familia de protocolos desconocida, marcas de enumeración no válidas).</span><span class="sxs-lookup"><span data-stu-id="5643c-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="5643c-139"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="5643c-140">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5643c-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="5643c-141"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="5643c-142">No hay memoria suficiente para asignar el identificador.</span><span class="sxs-lookup"><span data-stu-id="5643c-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="5643c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5643c-143">Requirements</span></span>



| <span data-ttu-id="5643c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5643c-144">Requirement</span></span> | <span data-ttu-id="5643c-145">Value</span><span class="sxs-lookup"><span data-stu-id="5643c-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5643c-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5643c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5643c-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5643c-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="5643c-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5643c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5643c-149">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5643c-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5643c-150">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5643c-150">End of server support</span></span><br/>    | <span data-ttu-id="5643c-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5643c-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="5643c-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5643c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="5643c-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="5643c-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5643c-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="5643c-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="5643c-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5643c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5643c-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5643c-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5643c-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="5643c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5643c-159">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="5643c-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5643c-160">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="5643c-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="5643c-161">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="5643c-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="5643c-162">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="5643c-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="5643c-163">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="5643c-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="5643c-164">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="5643c-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="5643c-165">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="5643c-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 


---
title: Función RtmGetNextRoute (RTM. h)
description: La función RtmGetNextRoute devuelve la siguiente ruta del subconjunto especificado de rutas de la tabla.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute función RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534474"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="6075c-104">RtmGetNextRoute función)</span><span class="sxs-lookup"><span data-stu-id="6075c-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="6075c-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6075c-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="6075c-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="6075c-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="6075c-107">La función **RtmGetNextRoute** devuelve la siguiente ruta del subconjunto especificado de rutas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6075c-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="6075c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6075c-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="6075c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6075c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6075c-110">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6075c-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6075c-111">Especifica la familia de rutas del protocolo que se va a recuperar, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="6075c-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="6075c-112">*EnumerationFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6075c-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6075c-113">Especifica las rutas que se deben enumerar.</span><span class="sxs-lookup"><span data-stu-id="6075c-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="6075c-114">Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las siguientes marcas y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="6075c-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="6075c-115">Las marcas son las mismas que las que se usan en [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="6075c-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="6075c-116">*Ruta* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="6075c-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6075c-117">En la entrada, la *ruta* apunta a una estructura específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="6075c-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="6075c-118">La función de llamada proporciona valores de miembro para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="6075c-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="6075c-119">Estos valores, junto con el parámetro *EnumerationFlags* , especifican el conjunto del que se van a devolver las rutas.</span><span class="sxs-lookup"><span data-stu-id="6075c-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="6075c-120">En la salida, la *ruta* apunta a una estructura que recibe la primera ruta que coincidía con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="6075c-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6075c-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6075c-121">Return value</span></span>

<span data-ttu-id="6075c-122">Si la función se ejecuta correctamente, el valor devuelto **no es un \_ error**.</span><span class="sxs-lookup"><span data-stu-id="6075c-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="6075c-123">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="6075c-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="6075c-124">Value</span><span class="sxs-lookup"><span data-stu-id="6075c-124">Value</span></span>                                                                                                       | <span data-ttu-id="6075c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6075c-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6075c-126"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="6075c-127">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="6075c-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="6075c-128"><dt>**ERROR \_ sin \_ rutas**</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="6075c-129">No hay ninguna ruta que coincida con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="6075c-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="6075c-130"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="6075c-131">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="6075c-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6075c-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6075c-132">Remarks</span></span>

<span data-ttu-id="6075c-133">Las rutas se devuelven en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="6075c-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="6075c-134">Número de red</span><span class="sxs-lookup"><span data-stu-id="6075c-134">Network number</span></span>
2.  <span data-ttu-id="6075c-135">Protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="6075c-135">Routing protocol</span></span>
3.  <span data-ttu-id="6075c-136">Identificador de interfaz</span><span class="sxs-lookup"><span data-stu-id="6075c-136">Interface identifier</span></span>
4.  <span data-ttu-id="6075c-137">Dirección de próximo salto</span><span class="sxs-lookup"><span data-stu-id="6075c-137">Next-hop address</span></span>

<span data-ttu-id="6075c-138">Esta función es menos eficaz que las funciones de identificador de enumeración correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6075c-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6075c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6075c-139">Requirements</span></span>



| <span data-ttu-id="6075c-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6075c-140">Requirement</span></span> | <span data-ttu-id="6075c-141">Value</span><span class="sxs-lookup"><span data-stu-id="6075c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6075c-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6075c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6075c-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6075c-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="6075c-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6075c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6075c-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6075c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6075c-146">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6075c-146">End of server support</span></span><br/>    | <span data-ttu-id="6075c-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6075c-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="6075c-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6075c-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="6075c-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="6075c-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6075c-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="6075c-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="6075c-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6075c-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6075c-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6075c-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6075c-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="6075c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6075c-155">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="6075c-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="6075c-156">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="6075c-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="6075c-157">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="6075c-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="6075c-158">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="6075c-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="6075c-159">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="6075c-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="6075c-160">**RtmGetFirstRoute**</span><span class="sxs-lookup"><span data-stu-id="6075c-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 






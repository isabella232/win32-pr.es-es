---
title: Función RtmGetFirstRoute (RTM. h)
description: La función RtmGetFirstRoute devuelve la primera ruta del subconjunto especificado de rutas de la tabla.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- RtmGetFirstRoute función RAS
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150521"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="bb25b-104">RtmGetFirstRoute función)</span><span class="sxs-lookup"><span data-stu-id="bb25b-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="bb25b-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb25b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bb25b-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="bb25b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bb25b-107">La función **RtmGetFirstRoute** devuelve la primera ruta del subconjunto especificado de rutas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bb25b-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb25b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb25b-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="bb25b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb25b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb25b-110">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb25b-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb25b-111">Especifica la familia de rutas del protocolo que se va a recuperar, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="bb25b-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="bb25b-112">*EnumerationFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb25b-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb25b-113">Especifica que limita el conjunto de rutas eliminadas a un subconjunto definido por estas marcas y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="bb25b-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="bb25b-114">Las marcas son las mismas que las que se usan en [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="bb25b-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb25b-115">*Ruta* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb25b-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb25b-116">En la entrada, la *ruta* apunta a una estructura específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="bb25b-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="bb25b-117">La función de llamada proporciona valores de miembro para esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bb25b-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="bb25b-118">Estos valores, junto con el parámetro *EnumerationFlags* , especifican el conjunto del que se van a devolver las rutas.</span><span class="sxs-lookup"><span data-stu-id="bb25b-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="bb25b-119">Salida, *ruta* apunta a la primera ruta que coincidía con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="bb25b-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb25b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb25b-120">Return value</span></span>

<span data-ttu-id="bb25b-121">Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.</span><span class="sxs-lookup"><span data-stu-id="bb25b-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="bb25b-122">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="bb25b-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="bb25b-123">Value</span><span class="sxs-lookup"><span data-stu-id="bb25b-123">Value</span></span>                                                                                                       | <span data-ttu-id="bb25b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb25b-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb25b-125"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="bb25b-126">Uno de los parámetros no es válido.</span><span class="sxs-lookup"><span data-stu-id="bb25b-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="bb25b-127"><dt>**ERROR \_ sin \_ rutas**</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="bb25b-128">No hay ninguna ruta que coincida con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="bb25b-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="bb25b-129"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="bb25b-130">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bb25b-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb25b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb25b-131">Remarks</span></span>

<span data-ttu-id="bb25b-132">Las rutas se devuelven en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb25b-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="bb25b-133">Número de red</span><span class="sxs-lookup"><span data-stu-id="bb25b-133">Network number</span></span>
2.  <span data-ttu-id="bb25b-134">Protocolo de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bb25b-134">Routing protocol</span></span>
3.  <span data-ttu-id="bb25b-135">Identificador de interfaz</span><span class="sxs-lookup"><span data-stu-id="bb25b-135">Interface identifier</span></span>
4.  <span data-ttu-id="bb25b-136">Dirección de próximo salto</span><span class="sxs-lookup"><span data-stu-id="bb25b-136">Next-hop address</span></span>

<span data-ttu-id="bb25b-137">Esta función es menos eficaz que la función de identificador de enumeración correspondiente, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="bb25b-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb25b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb25b-138">Requirements</span></span>



| <span data-ttu-id="bb25b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb25b-139">Requirement</span></span> | <span data-ttu-id="bb25b-140">Value</span><span class="sxs-lookup"><span data-stu-id="bb25b-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb25b-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb25b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bb25b-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bb25b-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="bb25b-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb25b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bb25b-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb25b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb25b-145">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bb25b-145">End of server support</span></span><br/>    | <span data-ttu-id="bb25b-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb25b-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="bb25b-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb25b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb25b-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb25b-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb25b-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb25b-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb25b-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb25b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb25b-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb25b-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb25b-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb25b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb25b-154">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bb25b-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bb25b-155">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bb25b-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="bb25b-156">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="bb25b-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="bb25b-157">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="bb25b-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="bb25b-158">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="bb25b-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="bb25b-159">**RtmGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="bb25b-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 






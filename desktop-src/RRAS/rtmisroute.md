---
title: Función RtmIsRoute (RTM. h)
description: La función RtmIsRoute determina si existen una o varias rutas a una red de destino especificada. Si es así, la función devuelve información para la mejor ruta a esa red.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- RtmIsRoute función RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492113"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="4dc84-105">RtmIsRoute función)</span><span class="sxs-lookup"><span data-stu-id="4dc84-105">RtmIsRoute function</span></span>

<span data-ttu-id="4dc84-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4dc84-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="4dc84-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="4dc84-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="4dc84-108">La función **RtmIsRoute** determina si existen una o varias rutas a una red de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="4dc84-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="4dc84-109">Si es así, la función devuelve información para la mejor ruta a esa red.</span><span class="sxs-lookup"><span data-stu-id="4dc84-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dc84-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dc84-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="4dc84-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dc84-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc84-112">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4dc84-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dc84-113">Especifica el tipo de estructura de datos al que apunta el parámetro de *red* , por ejemplo, [**\_ red IP**](ip-network.md), [**\_ red IPX**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="4dc84-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="4dc84-114">*Red* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4dc84-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dc84-115">Puntero a una estructura que especifica los datos de número de red específicos de la familia de protocolos.</span><span class="sxs-lookup"><span data-stu-id="4dc84-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="4dc84-116">Estos datos identifican la red para la que el autor de la llamada busca información de ruta.</span><span class="sxs-lookup"><span data-stu-id="4dc84-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="4dc84-117">*BestRoute* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4dc84-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dc84-118">Puntero a una estructura específica de la familia de protocolos que recibe la mejor información de ruta actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="4dc84-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc84-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4dc84-119">Return value</span></span>

<span data-ttu-id="4dc84-120">El valor devuelto es uno de los siguientes códigos.</span><span class="sxs-lookup"><span data-stu-id="4dc84-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="4dc84-121">Value</span><span class="sxs-lookup"><span data-stu-id="4dc84-121">Value</span></span>                                                                                                       | <span data-ttu-id="4dc84-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4dc84-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4dc84-123"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="4dc84-124">Existe al menos una ruta a la red especificada.</span><span class="sxs-lookup"><span data-stu-id="4dc84-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="4dc84-125">La mejor ruta se devuelve en la estructura a la que apunta el parámetro *BestRoute* .</span><span class="sxs-lookup"><span data-stu-id="4dc84-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="4dc84-126"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="4dc84-127">No hay ninguna ruta a la red especificada o se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="4dc84-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="4dc84-128">Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información:</span><span class="sxs-lookup"><span data-stu-id="4dc84-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="4dc84-129"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="4dc84-130">La operación se realizó correctamente, pero no hay ninguna ruta a la red especificada.</span><span class="sxs-lookup"><span data-stu-id="4dc84-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="4dc84-131"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="4dc84-132">El valor del parámetro *ProtocolFamily* no se corresponde con ninguna familia de protocolos instalada.</span><span class="sxs-lookup"><span data-stu-id="4dc84-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="4dc84-133"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="4dc84-134">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4dc84-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="4dc84-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4dc84-135">Requirements</span></span>



| <span data-ttu-id="4dc84-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dc84-136">Requirement</span></span> | <span data-ttu-id="4dc84-137">Value</span><span class="sxs-lookup"><span data-stu-id="4dc84-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc84-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc84-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc84-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4dc84-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4dc84-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4dc84-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc84-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4dc84-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4dc84-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4dc84-142">End of server support</span></span><br/>    | <span data-ttu-id="4dc84-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4dc84-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="4dc84-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4dc84-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc84-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="4dc84-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4dc84-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="4dc84-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="4dc84-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4dc84-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dc84-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dc84-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4dc84-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dc84-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dc84-151">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4dc84-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="4dc84-152">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="4dc84-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="4dc84-153">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="4dc84-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="4dc84-154">**\_red IP**</span><span class="sxs-lookup"><span data-stu-id="4dc84-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="4dc84-155">**\_red IPX**</span><span class="sxs-lookup"><span data-stu-id="4dc84-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="4dc84-156">Identificadores de la familia del protocolo RTMv1</span><span class="sxs-lookup"><span data-stu-id="4dc84-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 


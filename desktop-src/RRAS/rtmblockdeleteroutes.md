---
title: Función RtmBlockDeleteRoutes (RTM. h)
description: La función RtmBlockDeleteRoutes elimina todas las rutas del subconjunto especificado de rutas de la tabla.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes función RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491404"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="bb60a-104">RtmBlockDeleteRoutes función)</span><span class="sxs-lookup"><span data-stu-id="bb60a-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="bb60a-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb60a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bb60a-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="bb60a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bb60a-107">La función **RtmBlockDeleteRoutes** elimina todas las rutas del subconjunto especificado de rutas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="bb60a-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb60a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb60a-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="bb60a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb60a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb60a-110">*ClientHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb60a-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb60a-111">Identificador que identifica el cliente y, por tanto, el protocolo de enrutamiento, de las rutas que se van a eliminar.</span><span class="sxs-lookup"><span data-stu-id="bb60a-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="bb60a-112">*EnumerationFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb60a-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb60a-113">Especifica las rutas que se deben enumerar.</span><span class="sxs-lookup"><span data-stu-id="bb60a-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="bb60a-114">Este parámetro limita el conjunto de rutas eliminadas a un subconjunto definido por las siguientes marcas y los valores de los miembros correspondientes de la estructura a la que apunta el parámetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="bb60a-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="bb60a-115">Las marcas son las mismas que las que se usan en [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , salvo que la versión RTM \_ solo \_ \_ es redundante para **RtmBlockDeleteRoutes**.</span><span class="sxs-lookup"><span data-stu-id="bb60a-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="bb60a-116">La designación de la mejor ruta se ajusta a medida que se eliminan las rutas, por lo que la función elimina finalmente todas las rutas del subconjunto.</span><span class="sxs-lookup"><span data-stu-id="bb60a-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="bb60a-117">*CriteriaRoute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb60a-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb60a-118">Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="bb60a-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="bb60a-119">Los valores de miembro de esta estructura corresponden a las marcas especificadas por el parámetro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="bb60a-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb60a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb60a-120">Return value</span></span>

<span data-ttu-id="bb60a-121">Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.</span><span class="sxs-lookup"><span data-stu-id="bb60a-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="bb60a-122">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="bb60a-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="bb60a-123">Value</span><span class="sxs-lookup"><span data-stu-id="bb60a-123">Value</span></span>                                                                                                       | <span data-ttu-id="bb60a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb60a-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb60a-125"><dt>**ERROR \_ sin \_ rutas**</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="bb60a-126">No hay ninguna ruta que tenga los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="bb60a-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="bb60a-127"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="bb60a-128">El parámetro *ClientHandle* no es válido.</span><span class="sxs-lookup"><span data-stu-id="bb60a-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="bb60a-129"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="bb60a-130">Uno o varios de los parámetros de entrada no son válidos; por ejemplo, las marcas de enumeración no son válidas.</span><span class="sxs-lookup"><span data-stu-id="bb60a-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="bb60a-131"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="bb60a-132">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bb60a-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bb60a-133"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="bb60a-134">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="bb60a-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="bb60a-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb60a-135">Remarks</span></span>

<span data-ttu-id="bb60a-136">La función genera los mensajes de notificación adecuados a todos los clientes registrados, incluido el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="bb60a-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb60a-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb60a-137">Requirements</span></span>



| <span data-ttu-id="bb60a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb60a-138">Requirement</span></span> | <span data-ttu-id="bb60a-139">Value</span><span class="sxs-lookup"><span data-stu-id="bb60a-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb60a-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb60a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bb60a-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bb60a-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="bb60a-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb60a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bb60a-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bb60a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb60a-144">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="bb60a-144">End of server support</span></span><br/>    | <span data-ttu-id="bb60a-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb60a-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="bb60a-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb60a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb60a-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb60a-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb60a-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb60a-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="bb60a-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb60a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb60a-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb60a-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb60a-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb60a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb60a-153">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bb60a-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bb60a-154">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="bb60a-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="bb60a-155">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="bb60a-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="bb60a-156">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="bb60a-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 






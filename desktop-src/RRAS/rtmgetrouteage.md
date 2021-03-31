---
title: Función RtmGetRouteAge (RTM. h)
description: La función RtmGetRouteAge devuelve la antigüedad de una ruta. La antigüedad es el tiempo, en segundos, desde que se creó o actualizó por última vez.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- RtmGetRouteAge función RAS
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802786"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="2e675-105">RtmGetRouteAge función)</span><span class="sxs-lookup"><span data-stu-id="2e675-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="2e675-106">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2e675-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="2e675-107">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="2e675-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="2e675-108">La función **RtmGetRouteAge** devuelve la antigüedad de una ruta.</span><span class="sxs-lookup"><span data-stu-id="2e675-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="2e675-109">La antigüedad es el tiempo, en segundos, desde que se creó o actualizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="2e675-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e675-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e675-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="2e675-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e675-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e675-112">*Ruta* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="2e675-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e675-113">Puntero a una estructura específica de la familia de protocolos que especifica los datos de ruta obtenidos recientemente del administrador de tablas de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="2e675-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e675-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e675-114">Return value</span></span>

<span data-ttu-id="2e675-115">El valor devuelto es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e675-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="2e675-116">Value</span><span class="sxs-lookup"><span data-stu-id="2e675-116">Value</span></span>                                                                                   | <span data-ttu-id="2e675-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e675-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e675-118"><dt>**Ruta**</dt></span><span class="sxs-lookup"><span data-stu-id="2e675-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="2e675-119">El tiempo en segundos transcurrido desde que se creó o actualizó por última vez una ruta.</span><span class="sxs-lookup"><span data-stu-id="2e675-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="2e675-120"><dt>**DEFINIDO**</dt></span><span class="sxs-lookup"><span data-stu-id="2e675-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="2e675-121">El contenido de la estructura de ruta no es válido.</span><span class="sxs-lookup"><span data-stu-id="2e675-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="2e675-122">En este caso, una llamada a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un \_ parámetro de error no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="2e675-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e675-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e675-123">Remarks</span></span>

<span data-ttu-id="2e675-124">La antigüedad de la ruta se calcula a partir del \_ miembro de marca de tiempo RR de la estructura a la que apunta el parámetro *Route* .</span><span class="sxs-lookup"><span data-stu-id="2e675-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="2e675-125">El administrador de tablas de enrutamiento establece el valor de este miembro cuando se agrega o se actualiza una ruta.</span><span class="sxs-lookup"><span data-stu-id="2e675-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e675-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e675-126">Requirements</span></span>



| <span data-ttu-id="2e675-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e675-127">Requirement</span></span> | <span data-ttu-id="2e675-128">Value</span><span class="sxs-lookup"><span data-stu-id="2e675-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e675-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e675-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e675-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e675-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="2e675-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e675-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e675-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e675-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2e675-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2e675-133">End of server support</span></span><br/>    | <span data-ttu-id="2e675-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e675-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="2e675-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e675-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e675-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e675-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e675-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e675-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="2e675-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e675-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="2e675-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e675-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e675-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e675-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e675-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e675-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e675-142">Referencia de la versión 1 del administrador de tablas de enrutamiento \_</span><span class="sxs-lookup"><span data-stu-id="2e675-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="2e675-143">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="2e675-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="2e675-144">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="2e675-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="2e675-145">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="2e675-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="2e675-146">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="2e675-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 


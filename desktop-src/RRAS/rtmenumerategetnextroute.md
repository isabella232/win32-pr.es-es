---
title: Función RtmEnumerateGetNextRoute (RTM. h)
description: La función RtmEnumerateGetNextRoute devuelve la entrada de ruta siguiente en la enumeración iniciada por una llamada a RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- RtmEnumerateGetNextRoute función RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676833"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="a2a7a-104">RtmEnumerateGetNextRoute función)</span><span class="sxs-lookup"><span data-stu-id="a2a7a-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="a2a7a-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a2a7a-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="a2a7a-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a2a7a-107">La función **RtmEnumerateGetNextRoute** devuelve la entrada de ruta siguiente en la enumeración iniciada por una llamada a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="a2a7a-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2a7a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2a7a-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="a2a7a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2a7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2a7a-110">*EnumerationHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a2a7a-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a7a-111">Identificador que identifica la enumeración y especifica su ámbito.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="a2a7a-112">Obtenga este identificador llamando a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="a2a7a-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2a7a-113">*Ruta* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a2a7a-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2a7a-114">Puntero a una estructura de ruta específica de la familia de protocolos (ruta de [**\_ IP \_ RTM**](rtm-ip-route.md) o [**\_ \_ ruta IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="a2a7a-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="a2a7a-115">Esta estructura recibirá la siguiente ruta en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2a7a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2a7a-116">Return value</span></span>

<span data-ttu-id="a2a7a-117">Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="a2a7a-118">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="a2a7a-119">Value</span><span class="sxs-lookup"><span data-stu-id="a2a7a-119">Value</span></span>                                                                                                       | <span data-ttu-id="a2a7a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2a7a-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2a7a-121"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="a2a7a-122">El parámetro *EnumerationHandle* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="a2a7a-123"><dt>**ERROR: \_ no hay \_ más \_ rutas**</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="a2a7a-124">No hay más rutas en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="a2a7a-125"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="a2a7a-126">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2a7a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2a7a-127">Remarks</span></span>

<span data-ttu-id="a2a7a-128">Aunque las rutas no se devuelven en ningún orden concreto, cada ruta en la enumeración se devuelve una sola vez.</span><span class="sxs-lookup"><span data-stu-id="a2a7a-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2a7a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2a7a-129">Requirements</span></span>



| <span data-ttu-id="a2a7a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2a7a-130">Requirement</span></span> | <span data-ttu-id="a2a7a-131">Value</span><span class="sxs-lookup"><span data-stu-id="a2a7a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2a7a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2a7a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a2a7a-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a2a7a-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a2a7a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a2a7a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a2a7a-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a2a7a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a2a7a-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a2a7a-136">End of server support</span></span><br/>    | <span data-ttu-id="a2a7a-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2a7a-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="a2a7a-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2a7a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2a7a-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2a7a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2a7a-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2a7a-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2a7a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a2a7a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2a7a-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2a7a-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2a7a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2a7a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2a7a-145">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="a2a7a-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a2a7a-146">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="a2a7a-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="a2a7a-147">**\_ruta IP de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="a2a7a-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="a2a7a-148">**\_ruta IPX de RTM \_**</span><span class="sxs-lookup"><span data-stu-id="a2a7a-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="a2a7a-149">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="a2a7a-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="a2a7a-150">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="a2a7a-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 






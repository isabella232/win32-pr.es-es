---
title: Función RtmGetNetworkCount (RTM. h)
description: La función RtmGetNetworkCount recupera el número de redes a las que el administrador de tabla de enrutamiento tiene rutas.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- RtmGetNetworkCount función RAS
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802209"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="8d07d-104">RtmGetNetworkCount función)</span><span class="sxs-lookup"><span data-stu-id="8d07d-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="8d07d-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8d07d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="8d07d-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="8d07d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="8d07d-107">La función **RtmGetNetworkCount** recupera el número de redes a las que el administrador de tabla de enrutamiento tiene rutas.</span><span class="sxs-lookup"><span data-stu-id="8d07d-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d07d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d07d-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="8d07d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8d07d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d07d-110">*ProtocolFamily* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8d07d-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d07d-111">Especifica para qué tipo de red se va a obtener información de ruta, por ejemplo, IP o IPX.</span><span class="sxs-lookup"><span data-stu-id="8d07d-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d07d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d07d-112">Return value</span></span>

<span data-ttu-id="8d07d-113">Si la función se ejecuta correctamente, el valor devuelto es el recuento de redes, el número de redes conocidas para los protocolos de enrutamiento de la familia de protocolos especificada.</span><span class="sxs-lookup"><span data-stu-id="8d07d-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="8d07d-114">Si el valor devuelto es cero, no hay ninguna ruta disponible o se produjo un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="8d07d-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="8d07d-115">Llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8d07d-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="8d07d-116">Value</span><span class="sxs-lookup"><span data-stu-id="8d07d-116">Value</span></span>                                                                                                    | <span data-ttu-id="8d07d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d07d-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d07d-118"><dt>**SIN \_ errores**</dt></span><span class="sxs-lookup"><span data-stu-id="8d07d-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="8d07d-119">La operación se realizó correctamente, pero no hay ninguna ruta disponible.</span><span class="sxs-lookup"><span data-stu-id="8d07d-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="8d07d-120"><dt>**ERROR \_ de \_ parámetro no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="8d07d-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="8d07d-121">El valor del parámetro *ProtocolFamily* no se corresponde con ninguna familia de protocolos instalada.</span><span class="sxs-lookup"><span data-stu-id="8d07d-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8d07d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d07d-122">Requirements</span></span>



| <span data-ttu-id="8d07d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d07d-123">Requirement</span></span> | <span data-ttu-id="8d07d-124">Value</span><span class="sxs-lookup"><span data-stu-id="8d07d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d07d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d07d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8d07d-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8d07d-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8d07d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8d07d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8d07d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d07d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8d07d-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8d07d-129">End of server support</span></span><br/>    | <span data-ttu-id="8d07d-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d07d-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="8d07d-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d07d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d07d-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d07d-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d07d-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d07d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d07d-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d07d-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d07d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8d07d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d07d-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d07d-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d07d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8d07d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d07d-138">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8d07d-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="8d07d-139">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="8d07d-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="8d07d-140">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="8d07d-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="8d07d-141">Identificadores de la familia del protocolo RTMv1</span><span class="sxs-lookup"><span data-stu-id="8d07d-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 


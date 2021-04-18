---
title: Función RtmDeregisterClient (RTM. h)
description: La función RtmDeregisterClient anula el registro del cliente y libera los recursos asociados con el cliente.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- RtmDeregisterClient función RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422302"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="c41fc-104">RtmDeregisterClient función)</span><span class="sxs-lookup"><span data-stu-id="c41fc-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="c41fc-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c41fc-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c41fc-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="c41fc-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c41fc-107">La función **RtmDeregisterClient** anula el registro del cliente y libera los recursos asociados con el cliente.</span><span class="sxs-lookup"><span data-stu-id="c41fc-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41fc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c41fc-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="c41fc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c41fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41fc-110">*ClientHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c41fc-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41fc-111">Identificador que identifica el cliente cuyo registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="c41fc-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="c41fc-112">Obtenga este identificador llamando a [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="c41fc-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41fc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c41fc-113">Return value</span></span>

<span data-ttu-id="c41fc-114">Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.</span><span class="sxs-lookup"><span data-stu-id="c41fc-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="c41fc-115">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="c41fc-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="c41fc-116">Value</span><span class="sxs-lookup"><span data-stu-id="c41fc-116">Value</span></span>                                                                                                       | <span data-ttu-id="c41fc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c41fc-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="c41fc-118"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="c41fc-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="c41fc-119">El parámetro *ClientHandle* no es un identificador válido.</span><span class="sxs-lookup"><span data-stu-id="c41fc-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="c41fc-120"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c41fc-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="c41fc-121">Recursos insuficientes para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c41fc-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="c41fc-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c41fc-122">Remarks</span></span>

<span data-ttu-id="c41fc-123">Esta función quita todas las rutas agregadas por el cliente.</span><span class="sxs-lookup"><span data-stu-id="c41fc-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="c41fc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c41fc-124">Requirements</span></span>



| <span data-ttu-id="c41fc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c41fc-125">Requirement</span></span> | <span data-ttu-id="c41fc-126">Value</span><span class="sxs-lookup"><span data-stu-id="c41fc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c41fc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c41fc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c41fc-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c41fc-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c41fc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c41fc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c41fc-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c41fc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c41fc-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c41fc-131">End of server support</span></span><br/>    | <span data-ttu-id="c41fc-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c41fc-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c41fc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c41fc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c41fc-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c41fc-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c41fc-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c41fc-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c41fc-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c41fc-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c41fc-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c41fc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c41fc-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c41fc-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c41fc-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c41fc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41fc-140">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="c41fc-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c41fc-141">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="c41fc-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c41fc-142">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="c41fc-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 






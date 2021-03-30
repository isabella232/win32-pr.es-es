---
title: Función AllocConnections (NapUtil. h)
description: Asigna memoria para un número especificado de estructuras de conexión.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- AllocConnections función NAP
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804075"
---
# <a name="allocconnections-function"></a><span data-ttu-id="b3757-104">AllocConnections función)</span><span class="sxs-lookup"><span data-stu-id="b3757-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="b3757-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3757-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b3757-106">La función **AllocConnections** asigna memoria para un número especificado de estructuras de [**conexión**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="b3757-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3757-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3757-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="b3757-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3757-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3757-109">*conexiones* \[ de in, out\]</span><span class="sxs-lookup"><span data-stu-id="b3757-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3757-110">Puntero a una matriz de estructuras de [**conexiones**](connections-struct.md) recién asignadas.</span><span class="sxs-lookup"><span data-stu-id="b3757-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="b3757-111">*connectionsCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b3757-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3757-112">El número de estructuras que se van a asignar a *las conexiones*.</span><span class="sxs-lookup"><span data-stu-id="b3757-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3757-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3757-113">Return value</span></span>



| <span data-ttu-id="b3757-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b3757-114">Return code</span></span>                                                                                   | <span data-ttu-id="b3757-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3757-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3757-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b3757-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b3757-117">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3757-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="b3757-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b3757-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b3757-119">Se pasó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="b3757-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b3757-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b3757-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b3757-121">El sistema no tiene memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="b3757-121">The system is out of virtual memory.</span></span> <span data-ttu-id="b3757-122">No se pudo realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="b3757-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b3757-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3757-123">Remarks</span></span>

<span data-ttu-id="b3757-124">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="b3757-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="b3757-125">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="b3757-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="b3757-126">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="b3757-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="b3757-127">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="b3757-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="b3757-128">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="b3757-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3757-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3757-129">Requirements</span></span>



| <span data-ttu-id="b3757-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3757-130">Requirement</span></span> | <span data-ttu-id="b3757-131">Value</span><span class="sxs-lookup"><span data-stu-id="b3757-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b3757-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3757-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b3757-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3757-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b3757-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3757-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b3757-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3757-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b3757-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3757-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3757-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3757-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="b3757-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b3757-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3757-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3757-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3757-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3757-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3757-141">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="b3757-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 






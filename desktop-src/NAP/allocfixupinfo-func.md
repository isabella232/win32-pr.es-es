---
title: Función AllocFixupInfo (NapUtil. h)
description: Asigna memoria para una estructura FixupInfo del tamaño especificado.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- AllocFixupInfo función NAP
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905050"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="d6931-104">AllocFixupInfo función)</span><span class="sxs-lookup"><span data-stu-id="d6931-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="d6931-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d6931-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d6931-106">La función **AllocFixupInfo** asigna memoria para una estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) del tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="d6931-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6931-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6931-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="d6931-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6931-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6931-109">*fixupInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d6931-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6931-110">Puntero a la dirección de una estructura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) recién asignada.</span><span class="sxs-lookup"><span data-stu-id="d6931-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6931-111">*countResultCodes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6931-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6931-112">El número de códigos de resultado que se asignan a *fixupInfo*.</span><span class="sxs-lookup"><span data-stu-id="d6931-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6931-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6931-113">Return value</span></span>



| <span data-ttu-id="d6931-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d6931-114">Return code</span></span>                                                                                   | <span data-ttu-id="d6931-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6931-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6931-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d6931-117">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6931-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="d6931-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d6931-119">Se pasó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="d6931-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d6931-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d6931-121">El sistema no tiene memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="d6931-121">The system is out of virtual memory.</span></span> <span data-ttu-id="d6931-122">No se pudo realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="d6931-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6931-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6931-123">Remarks</span></span>

<span data-ttu-id="d6931-124">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="d6931-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="d6931-125">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="d6931-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="d6931-126">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d6931-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="d6931-127">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d6931-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="d6931-128">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="d6931-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6931-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6931-129">Requirements</span></span>



| <span data-ttu-id="d6931-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6931-130">Requirement</span></span> | <span data-ttu-id="d6931-131">Value</span><span class="sxs-lookup"><span data-stu-id="d6931-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d6931-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6931-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d6931-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d6931-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d6931-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6931-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d6931-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6931-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d6931-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6931-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6931-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="d6931-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6931-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6931-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6931-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6931-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6931-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6931-141">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="d6931-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 






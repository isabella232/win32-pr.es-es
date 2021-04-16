---
title: Función AllocCountedString (NapUtil. h)
description: Asigna memoria para una cadena terminada en NULL y la devuelve en una estructura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- AllocCountedString función NAP
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676585"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="1d9a5-104">AllocCountedString función)</span><span class="sxs-lookup"><span data-stu-id="1d9a5-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="1d9a5-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1d9a5-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1d9a5-106">La función **AllocCountedString** asigna memoria para una cadena terminada en NULL y la devuelve en una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="1d9a5-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9a5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d9a5-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="1d9a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d9a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9a5-109">*countedString* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a5-110">Puntero a la dirección de una estructura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) recién asignada.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1d9a5-111">*cadena* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d9a5-112">Un puntero a la cadena terminada en null que se va a devolver en *countedString*.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d9a5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d9a5-113">Return value</span></span>



| <span data-ttu-id="1d9a5-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1d9a5-114">Return code</span></span>                                                                                   | <span data-ttu-id="1d9a5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d9a5-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d9a5-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1d9a5-117">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="1d9a5-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1d9a5-119">Se pasó un argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1d9a5-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1d9a5-121">El sistema no tiene memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-121">The system is out of virtual memory.</span></span> <span data-ttu-id="1d9a5-122">No se pudo realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d9a5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d9a5-123">Remarks</span></span>

<span data-ttu-id="1d9a5-124">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="1d9a5-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="1d9a5-125">El autor de la llamada asigna y libera los parámetros **in** .</span><span class="sxs-lookup"><span data-stu-id="1d9a5-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="1d9a5-126">El destinatario asigna los parámetros **out** y el llamador los libera mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="1d9a5-127">Los parámetros **in/out** son asignados por el autor de la llamada, liberados y reasignados por el destinatario y, en última instancia, liberados por el llamador, mediante **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="1d9a5-128">Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="1d9a5-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d9a5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d9a5-129">Requirements</span></span>



| <span data-ttu-id="1d9a5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d9a5-130">Requirement</span></span> | <span data-ttu-id="1d9a5-131">Value</span><span class="sxs-lookup"><span data-stu-id="1d9a5-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9a5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d9a5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9a5-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1d9a5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d9a5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9a5-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d9a5-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1d9a5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d9a5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d9a5-137"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="1d9a5-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1d9a5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9a5-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d9a5-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d9a5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d9a5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9a5-141">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="1d9a5-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 






---
description: Devuelve la asignación de conjunto de CPU explícita del subproceso especificado, si se ha establecido una asignación mediante la API de SetThreadSelectedCpuSets. Si no se establece ninguna asignación explícita, RequiredIdCount se establece en 0 y la función devuelve TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Función GetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082650"
---
# <a name="getthreadselectedcpusets-function"></a><span data-ttu-id="06c56-104">GetThreadSelectedCpuSets función)</span><span class="sxs-lookup"><span data-stu-id="06c56-104">GetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="06c56-105">Devuelve la asignación de conjunto de CPU explícita del subproceso especificado, si se ha establecido una asignación mediante la API de [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) .</span><span class="sxs-lookup"><span data-stu-id="06c56-105">Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) API.</span></span> <span data-ttu-id="06c56-106">Si no se establece ninguna asignación explícita, **RequiredIdCount** se establece en 0 y la función devuelve true.</span><span class="sxs-lookup"><span data-stu-id="06c56-106">If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06c56-107">Syntax</span></span>


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="06c56-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06c56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c56-109">*Subproceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06c56-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c56-110">Especifica el subproceso para el que se van a consultar los conjuntos de CPU seleccionados.</span><span class="sxs-lookup"><span data-stu-id="06c56-110">Specifies the thread for which to query the selected CPU Sets.</span></span> <span data-ttu-id="06c56-111">Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de subproceso \_ .</span><span class="sxs-lookup"><span data-stu-id="06c56-111">This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="06c56-112">El valor devuelto por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) también se puede especificar aquí.</span><span class="sxs-lookup"><span data-stu-id="06c56-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="06c56-113">*CpuSetIds* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="06c56-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06c56-114">Especifica un búfer opcional para recuperar la lista de identificadores de conjuntos de CPU.</span><span class="sxs-lookup"><span data-stu-id="06c56-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="06c56-115">*CpuSetIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="06c56-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c56-116">Especifica la capacidad del búfer especificado en **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="06c56-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="06c56-117">Si el búfer es NULL, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="06c56-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="06c56-118">*RequiredIdCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="06c56-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06c56-119">Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU seleccionados para el subproceso.</span><span class="sxs-lookup"><span data-stu-id="06c56-119">Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets.</span></span> <span data-ttu-id="06c56-120">Especifica el número de identificadores rellenados en el búfer si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="06c56-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c56-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06c56-121">Return value</span></span>

<span data-ttu-id="06c56-122">Esta API devuelve TRUE en caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="06c56-122">This API returns TRUE on success.</span></span> <span data-ttu-id="06c56-123">Si el búfer no es suficientemente grande, el valor de **GetLastError** es error de \_ búfer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="06c56-123">If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="06c56-124">No se puede producir un error en esta API cuando se pasan parámetros válidos y el búfer de retorno es suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="06c56-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c56-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c56-125">Requirements</span></span>



| <span data-ttu-id="06c56-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c56-126">Requirement</span></span> | <span data-ttu-id="06c56-127">Value</span><span class="sxs-lookup"><span data-stu-id="06c56-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c56-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06c56-128">Minimum supported client</span></span><br/> | <span data-ttu-id="06c56-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="06c56-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="06c56-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06c56-130">Minimum supported server</span></span><br/> | <span data-ttu-id="06c56-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="06c56-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="06c56-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06c56-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c56-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c56-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="06c56-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06c56-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="06c56-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c56-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="06c56-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06c56-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c56-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c56-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 


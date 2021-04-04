---
description: Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado. Esta asignación invalida la asignación predeterminada del proceso, si se ha establecido uno.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Función SetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909677"
---
# <a name="setthreadselectedcpusets-function"></a><span data-ttu-id="35c09-104">SetThreadSelectedCpuSets función)</span><span class="sxs-lookup"><span data-stu-id="35c09-104">SetThreadSelectedCpuSets function</span></span>

<span data-ttu-id="35c09-105">Establece la asignación de conjuntos de CPU seleccionados para el subproceso especificado.</span><span class="sxs-lookup"><span data-stu-id="35c09-105">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="35c09-106">Esta asignación invalida la asignación predeterminada del proceso, si se ha establecido uno.</span><span class="sxs-lookup"><span data-stu-id="35c09-106">This assignment overrides the process default assignment, if one is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c09-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35c09-107">Syntax</span></span>


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="35c09-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35c09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35c09-109">*Subproceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35c09-109">*Thread* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c09-110">Especifica el subproceso en el que se va a establecer la asignación de conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="35c09-110">Specifies the thread on which to set the CPU Set assignment.</span></span> <span data-ttu-id="35c09-111">Este identificador debe tener el \_ derecho de \_ acceso de información limitada del subproceso \_ .</span><span class="sxs-lookup"><span data-stu-id="35c09-111">This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="35c09-112">También se puede usar el valor devuelto por [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) .</span><span class="sxs-lookup"><span data-stu-id="35c09-112">The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.</span></span>

</dd> <dt>

<span data-ttu-id="35c09-113">*CpuSetIds* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35c09-113">*CpuSetIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c09-114">Especifica la lista de identificadores de conjuntos de CPU que se establecerá como conjunto de CPU seleccionado de subproceso.</span><span class="sxs-lookup"><span data-stu-id="35c09-114">Specifies the list of CPU Set IDs to set as the thread selected CPU set.</span></span> <span data-ttu-id="35c09-115">Si es NULL, la API borra cualquier asignación y revierte para procesar la asignación predeterminada si se establece una.</span><span class="sxs-lookup"><span data-stu-id="35c09-115">If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.</span></span>

</dd> <dt>

<span data-ttu-id="35c09-116">*CpuSetIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35c09-116">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c09-117">Especifica el número de identificadores de la lista que se han pasado en el argumento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="35c09-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="35c09-118">Si ese valor es NULL, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="35c09-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35c09-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35c09-119">Return value</span></span>

<span data-ttu-id="35c09-120">No se puede producir un error en esta función cuando se pasan parámetros válidos.</span><span class="sxs-lookup"><span data-stu-id="35c09-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c09-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35c09-121">Requirements</span></span>



| <span data-ttu-id="35c09-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c09-122">Requirement</span></span> | <span data-ttu-id="35c09-123">Value</span><span class="sxs-lookup"><span data-stu-id="35c09-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c09-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35c09-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35c09-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="35c09-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="35c09-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35c09-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35c09-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="35c09-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="35c09-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35c09-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35c09-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35c09-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="35c09-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35c09-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="35c09-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="35c09-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="35c09-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35c09-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c09-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c09-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 

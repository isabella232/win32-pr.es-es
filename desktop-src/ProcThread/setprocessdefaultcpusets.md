---
description: Establece la asignación de conjuntos de CPU predeterminada para los subprocesos en el proceso especificado. Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante SetThreadSelectedCpuSets, heredarán automáticamente los conjuntos especificados por SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Función SetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677831"
---
# <a name="setprocessdefaultcpusets-function"></a><span data-ttu-id="6421d-104">SetProcessDefaultCpuSets función)</span><span class="sxs-lookup"><span data-stu-id="6421d-104">SetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="6421d-105">Establece la asignación de conjuntos de CPU predeterminada para los subprocesos en el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="6421d-105">Sets the default CPU Sets assignment for threads in the specified process.</span></span> <span data-ttu-id="6421d-106">Los subprocesos que se crean, que no tienen conjuntos de CPU establecidos explícitamente mediante [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), heredarán automáticamente los conjuntos especificados por **SetProcessDefaultCpuSets** .</span><span class="sxs-lookup"><span data-stu-id="6421d-106">Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="6421d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6421d-107">Syntax</span></span>


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a><span data-ttu-id="6421d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6421d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6421d-109">*Proceso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6421d-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6421d-110">Especifica el proceso para el que se van a establecer los conjuntos de CPU predeterminados.</span><span class="sxs-lookup"><span data-stu-id="6421d-110">Specifies the process for which to set the default CPU Sets.</span></span> <span data-ttu-id="6421d-111">Este identificador debe tener el \_ derecho de \_ acceso de información limitada del proceso \_ .</span><span class="sxs-lookup"><span data-stu-id="6421d-111">This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="6421d-112">El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.</span><span class="sxs-lookup"><span data-stu-id="6421d-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="6421d-113">*CpuSetIds* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6421d-113">*CpuSetIds* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6421d-114">Especifica la lista de identificadores de conjuntos de CPU que se establecerá como el conjunto de CPU predeterminado del proceso.</span><span class="sxs-lookup"><span data-stu-id="6421d-114">Specifies the list of CPU Set IDs to set as the process default CPU set.</span></span> <span data-ttu-id="6421d-115">Si es NULL, el **SetProcessDefaultCpuSets** borra cualquier asignación.</span><span class="sxs-lookup"><span data-stu-id="6421d-115">If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.</span></span>

</dd> <dt>

<span data-ttu-id="6421d-116">*CpuSetIdCound* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6421d-116">*CpuSetIdCound* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6421d-117">Especifica el número de identificadores de la lista que se han pasado en el argumento **CpuSetIds** .</span><span class="sxs-lookup"><span data-stu-id="6421d-117">Specifies the number of IDs in the list passed in the **CpuSetIds** argument.</span></span> <span data-ttu-id="6421d-118">Si ese valor es NULL, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="6421d-118">If that value is NULL, this should be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6421d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6421d-119">Return value</span></span>

<span data-ttu-id="6421d-120">No se puede producir un error en esta función cuando se pasan parámetros válidos.</span><span class="sxs-lookup"><span data-stu-id="6421d-120">This function cannot fail when passed valid parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6421d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6421d-121">Requirements</span></span>



| <span data-ttu-id="6421d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6421d-122">Requirement</span></span> | <span data-ttu-id="6421d-123">Value</span><span class="sxs-lookup"><span data-stu-id="6421d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6421d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6421d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6421d-125">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="6421d-125">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="6421d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6421d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6421d-127">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="6421d-127">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="6421d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6421d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6421d-129"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-129"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="6421d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6421d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6421d-131"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-131"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="6421d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6421d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6421d-133"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-133"><dt>Kernel32.dll</dt></span></span> </dl>       |



 

 

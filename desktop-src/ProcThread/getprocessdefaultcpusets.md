---
description: Recupera la lista de conjuntos de CPU en el conjunto predeterminado de procesos establecido por SetProcessDefaultCpuSets. Si no se establecen conjuntos de CPU predeterminados para un proceso determinado, el valor de RequiredIdCount se establece en 0 y la función se ejecuta correctamente.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Función GetProcessDefaultCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677861"
---
# <a name="getprocessdefaultcpusets-function"></a><span data-ttu-id="963f0-104">GetProcessDefaultCpuSets función)</span><span class="sxs-lookup"><span data-stu-id="963f0-104">GetProcessDefaultCpuSets function</span></span>

<span data-ttu-id="963f0-105">Recupera la lista de conjuntos de CPU en el conjunto predeterminado de procesos establecido por [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span><span class="sxs-lookup"><span data-stu-id="963f0-105">Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md).</span></span> <span data-ttu-id="963f0-106">Si no se establecen conjuntos de CPU predeterminados para un proceso determinado, el valor de **RequiredIdCount** se establece en 0 y la función se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="963f0-106">If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.</span></span>

## <a name="syntax"></a><span data-ttu-id="963f0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="963f0-107">Syntax</span></span>


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a><span data-ttu-id="963f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="963f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963f0-109">*Proceso* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="963f0-109">*Process* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963f0-110">Especifica un identificador de proceso para el proceso que se va a consultar.</span><span class="sxs-lookup"><span data-stu-id="963f0-110">Specifies a process handle for the process to query.</span></span> <span data-ttu-id="963f0-111">Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de proceso \_ .</span><span class="sxs-lookup"><span data-stu-id="963f0-111">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="963f0-112">El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.</span><span class="sxs-lookup"><span data-stu-id="963f0-112">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="963f0-113">*CpuSetIds* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="963f0-113">*CpuSetIds* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="963f0-114">Especifica un búfer opcional para recuperar la lista de identificadores de conjuntos de CPU.</span><span class="sxs-lookup"><span data-stu-id="963f0-114">Specifies an optional buffer to retrieve the list of CPU Set identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="963f0-115">*CpuSetIdCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="963f0-115">*CpuSetIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="963f0-116">Especifica la capacidad del búfer especificado en **CpuSetIds**.</span><span class="sxs-lookup"><span data-stu-id="963f0-116">Specifies the capacity of the buffer specified in **CpuSetIds**.</span></span> <span data-ttu-id="963f0-117">Si el búfer es NULL, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="963f0-117">If the buffer is NULL, this must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="963f0-118">*RequiredIdCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="963f0-118">*RequiredIdCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="963f0-119">Especifica la capacidad necesaria del búfer para contener toda la lista de conjuntos de CPU predeterminados del proceso.</span><span class="sxs-lookup"><span data-stu-id="963f0-119">Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets.</span></span> <span data-ttu-id="963f0-120">Especifica el número de identificadores rellenados en el búfer si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="963f0-120">On successful return, this specifies the number of IDs filled into the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963f0-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="963f0-121">Return value</span></span>

<span data-ttu-id="963f0-122">Esta API devuelve TRUE en caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="963f0-122">This API returns TRUE on success.</span></span> <span data-ttu-id="963f0-123">Si el búfer no es suficientemente grande, la API devuelve FALSE y el valor de **GetLastError** es error de \_ búfer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="963f0-123">If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="963f0-124">No se puede producir un error en esta API cuando se pasan parámetros válidos y el búfer de retorno es suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="963f0-124">This API cannot fail when passed valid parameters and the return buffer is large enough.</span></span>

## <a name="requirements"></a><span data-ttu-id="963f0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="963f0-125">Requirements</span></span>



| <span data-ttu-id="963f0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="963f0-126">Requirement</span></span> | <span data-ttu-id="963f0-127">Value</span><span class="sxs-lookup"><span data-stu-id="963f0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="963f0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="963f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="963f0-129">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="963f0-129">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="963f0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="963f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="963f0-131">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="963f0-131">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="963f0-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="963f0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="963f0-133"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="963f0-133"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="963f0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="963f0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="963f0-135"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="963f0-135"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="963f0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="963f0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="963f0-137"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="963f0-137"><dt>Kernel32.dll</dt></span></span> </dl>       |



 


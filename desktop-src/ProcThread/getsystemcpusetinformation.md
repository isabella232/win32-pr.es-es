---
description: Permite a una aplicación consultar los conjuntos de CPU disponibles en el sistema y su estado actual.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Función GetSystemCpuSetInformation (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276823"
---
# <a name="getsystemcpusetinformation-function"></a><span data-ttu-id="e0add-103">GetSystemCpuSetInformation función)</span><span class="sxs-lookup"><span data-stu-id="e0add-103">GetSystemCpuSetInformation function</span></span>

<span data-ttu-id="e0add-104">Permite a una aplicación consultar los conjuntos de CPU disponibles en el sistema y su estado actual.</span><span class="sxs-lookup"><span data-stu-id="e0add-104">Allows an application to query the available CPU Sets on the system, and their current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0add-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0add-105">Syntax</span></span>


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e0add-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0add-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0add-107">*Información* \[ de out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e0add-107">*Information* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0add-108">Puntero a una estructura [**de \_ \_ \_ información de conjunto de CPU del sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) que recibe los datos del conjunto de CPU.</span><span class="sxs-lookup"><span data-stu-id="e0add-108">A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data.</span></span> <span data-ttu-id="e0add-109">Pase NULL con una longitud de búfer de 0 para determinar el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="e0add-109">Pass NULL with a buffer length of 0 to determine the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="e0add-110">*BufferLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0add-110">*BufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0add-111">La longitud, en bytes, del búfer de salida pasada como argumento de la información.</span><span class="sxs-lookup"><span data-stu-id="e0add-111">The length, in bytes, of the output buffer passed as the Information argument.</span></span>

</dd> <dt>

<span data-ttu-id="e0add-112">*ReturnedLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e0add-112">*ReturnedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0add-113">La longitud, en bytes, de los datos válidos en el búfer de salida si el búfer es suficientemente grande o el tamaño necesario del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e0add-113">The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer.</span></span> <span data-ttu-id="e0add-114">Si no existe ningún conjunto de CPU, este valor será 0.</span><span class="sxs-lookup"><span data-stu-id="e0add-114">If no CPU Sets exist, this value will be 0.</span></span>

</dd> <dt>

<span data-ttu-id="e0add-115">*Proceso* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="e0add-115">*Process* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0add-116">Un identificador opcional para un proceso.</span><span class="sxs-lookup"><span data-stu-id="e0add-116">An optional handle to a process.</span></span> <span data-ttu-id="e0add-117">Este proceso se usa para determinar el valor de la marca **AllocatedToTargetProcess** en la estructura de información de conjunto de CPU del sistema \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e0add-117">This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure.</span></span> <span data-ttu-id="e0add-118">Si se asigna un conjunto de CPU al proceso especificado, se establece la marca.</span><span class="sxs-lookup"><span data-stu-id="e0add-118">If a CPU Set is allocated to the specified process, the flag is set.</span></span> <span data-ttu-id="e0add-119">De lo contrario, está claro.</span><span class="sxs-lookup"><span data-stu-id="e0add-119">Otherwise, it is clear.</span></span> <span data-ttu-id="e0add-120">Este identificador debe tener el \_ derecho de \_ acceso de información limitada de consulta de proceso \_ .</span><span class="sxs-lookup"><span data-stu-id="e0add-120">This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right.</span></span> <span data-ttu-id="e0add-121">El valor devuelto por [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) también se puede especificar aquí.</span><span class="sxs-lookup"><span data-stu-id="e0add-121">The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.</span></span>

</dd> <dt>

<span data-ttu-id="e0add-122">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="e0add-122">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="e0add-123">Reserved, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="e0add-123">Reserved, must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0add-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0add-124">Return value</span></span>

<span data-ttu-id="e0add-125">Si la API se ejecuta correctamente, devuelve TRUE.</span><span class="sxs-lookup"><span data-stu-id="e0add-125">If the API succeeds it returns TRUE.</span></span> <span data-ttu-id="e0add-126">Si se produce un error, la razón del error está disponible a través de **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="e0add-126">If it fails, the error reason is available through **GetLastError**.</span></span> <span data-ttu-id="e0add-127">Si el búfer de información era NULL o no es lo suficientemente grande, se devuelve el búfer de ERROR de código \_ insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="e0add-127">If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned.</span></span> <span data-ttu-id="e0add-128">No se puede producir un error en esta API cuando se pasan parámetros válidos y un búfer lo suficientemente grande como para contener todos los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="e0add-128">This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0add-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0add-129">Requirements</span></span>



| <span data-ttu-id="e0add-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0add-130">Requirement</span></span> | <span data-ttu-id="e0add-131">Value</span><span class="sxs-lookup"><span data-stu-id="e0add-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0add-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0add-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e0add-133">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 10 \|\]</span><span class="sxs-lookup"><span data-stu-id="e0add-133">Windows 10 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="e0add-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0add-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e0add-135">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2016 \|\]</span><span class="sxs-lookup"><span data-stu-id="e0add-135">Windows Server 2016 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="e0add-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0add-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0add-137"><dt>Processthreadsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0add-137"><dt>Processthreadsapi.h</dt></span></span> </dl> |
| <span data-ttu-id="e0add-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0add-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e0add-139"><dt>Windows. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0add-139"><dt>Windows.h</dt></span></span> </dl>          |
| <span data-ttu-id="e0add-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0add-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0add-141"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0add-141"><dt>Kernel32.dll</dt></span></span> </dl>       |



 


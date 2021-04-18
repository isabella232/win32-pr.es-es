---
description: Recupera la información del sistema especificada.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: ZwQuerySystemInformation función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQuerySystemInformation
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 2e516b12e5109470c1ddb86ea6a665ca29f138b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671025"
---
# <a name="zwquerysysteminformation-function"></a><span data-ttu-id="eb841-103">ZwQuerySystemInformation función)</span><span class="sxs-lookup"><span data-stu-id="eb841-103">ZwQuerySystemInformation function</span></span>

<span data-ttu-id="eb841-104">\[**ZwQuerySystemInformation** ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="eb841-104">\[**ZwQuerySystemInformation** is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eb841-105">En su lugar, use las funciones alternativas que se enumeran en este tema.\]</span><span class="sxs-lookup"><span data-stu-id="eb841-105">Instead, use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="eb841-106">Recupera la información del sistema especificada.</span><span class="sxs-lookup"><span data-stu-id="eb841-106">Retrieves the specified system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb841-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb841-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="eb841-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb841-109">*SystemInformationClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eb841-109">*SystemInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb841-110">Tipo de información del sistema que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="eb841-110">The type of system information to be retrieved.</span></span> <span data-ttu-id="eb841-111">Este parámetro puede ser uno de los siguientes valores del tipo de enumeración **\_ \_ clase de información del sistema** .</span><span class="sxs-lookup"><span data-stu-id="eb841-111">This parameter can be one of the following values from the **SYSTEM\_INFORMATION\_CLASS** enumeration type.</span></span>

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span data-ttu-id="eb841-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-112"><span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-113">Número de procesadores del sistema en una estructura de **\_ \_ información básica del sistema** .</span><span class="sxs-lookup"><span data-stu-id="eb841-113">The number of processors in the system in a **SYSTEM\_BASIC\_INFORMATION** structure.</span></span> <span data-ttu-id="eb841-114">En su lugar, use la función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .</span><span class="sxs-lookup"><span data-stu-id="eb841-114">Use the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function instead.</span></span>

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span data-ttu-id="eb841-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-115"><span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-116">Una estructura **de \_ \_ información de rendimiento del sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-116">An opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-117">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="eb841-117">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span data-ttu-id="eb841-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-118"><span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-119">Estructura de **\_ \_ información TIMEOFDAY del sistema** opaca que se puede usar para generar un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-119">An opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-120">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="eb841-120">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span data-ttu-id="eb841-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-121"><span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-122">Una matriz de estructuras de **\_ \_ información de proceso del sistema** , una para cada proceso que se ejecuta en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-122">An array of **SYSTEM\_PROCESS\_INFORMATION** structures, one for each process running in the system.</span></span>

<span data-ttu-id="eb841-123">Estas estructuras contienen información sobre el uso de recursos de cada proceso, incluido el número de identificadores utilizados por el proceso, el uso de archivo de página máximo y el número de páginas de memoria que el proceso ha asignado.</span><span class="sxs-lookup"><span data-stu-id="eb841-123">These structures contain information about the resource usage of each process, including the number of handles used by the process, the peak page-file usage, and the number of memory pages that the process has allocated.</span></span>

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span data-ttu-id="eb841-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-124"><span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-125">Una matriz de estructuras de **\_ información de \_ rendimiento \_ de procesador del sistema** , una para cada procesador instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-125">An array of **SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION** structures, one for each processor installed in the system.</span></span>

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span data-ttu-id="eb841-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-126"><span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-127">Estructura de **\_ \_ información de interrupción opaca del sistema** que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-127">An opaque **SYSTEM\_INTERRUPT\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-128">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="eb841-128">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span data-ttu-id="eb841-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-129"><span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-130">Estructura de **\_ \_ información de excepción de sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-130">An opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-131">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="eb841-131">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span data-ttu-id="eb841-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-132"><span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-133">Estructura **de \_ \_ \_ información de cuota del registro del sistema** .</span><span class="sxs-lookup"><span data-stu-id="eb841-133">A **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure.</span></span>

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span data-ttu-id="eb841-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span><span class="sxs-lookup"><span data-stu-id="eb841-134"><span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-135">Estructura de **\_ \_ información de direcciones de sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-135">An opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure that can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-136">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="eb841-136">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb841-137">*SystemInformation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb841-137">*SystemInformation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb841-138">Un puntero a un búfer que recibe la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb841-138">A pointer to a buffer that receives the requested information.</span></span> <span data-ttu-id="eb841-139">El tamaño y la estructura de esta información varía en función del valor del parámetro *SystemInformationClass* , como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb841-139">The size and structure of this information varies depending on the value of the *SystemInformationClass* parameter, as indicated in the following table.</span></span>

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span data-ttu-id="eb841-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_información básica del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-140"><span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**SYSTEM\_BASIC\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-141">Cuando el parámetro *SystemInformationClass* es **SystemBasicInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ información básica del sistema** con el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-141">When the *SystemInformationClass* parameter is **SystemBasicInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

<span data-ttu-id="eb841-142">El miembro **NumberOfProcessors** contiene el número de procesadores presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-142">The **NumberOfProcessors** member contains the number of processors present in the system.</span></span> <span data-ttu-id="eb841-143">En su lugar, use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="eb841-143">Use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) instead to retrieve this information.</span></span>

<span data-ttu-id="eb841-144">Los demás miembros de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-144">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span data-ttu-id="eb841-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_información de rendimiento del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-145"><span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**SYSTEM\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-146">Cuando el parámetro *SystemInformationClass* es **SystemPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de rendimiento del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-146">When the *SystemInformationClass* parameter is **SystemPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_PERFORMANCE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-147">Para este propósito, la estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-147">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="eb841-148">Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-148">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="eb841-149">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.</span><span class="sxs-lookup"><span data-stu-id="eb841-149">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span data-ttu-id="eb841-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_información de TIMEOFDAY del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-150"><span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**SYSTEM\_TIMEOFDAY\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-151">Cuando el parámetro *SystemInformationClass* es **SystemTimeOfDayInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información TIMEOFDAY del sistema** opaca que se usará para generar un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-151">When the *SystemInformationClass* parameter is **SystemTimeOfDayInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_TIMEOFDAY\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-152">Para este propósito, la estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-152">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

<span data-ttu-id="eb841-153">Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-153">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="eb841-154">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.</span><span class="sxs-lookup"><span data-stu-id="eb841-154">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span data-ttu-id="eb841-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_información del proceso del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-155"><span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**SYSTEM\_PROCESS\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-156">Cuando el parámetro *SystemInformationClass* es **SystemProcessInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de **\_ \_ información de proceso del sistema** como procesos en ejecución en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-156">When the *SystemInformationClass* parameter is **SystemProcessInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processes running in the system.</span></span> <span data-ttu-id="eb841-157">Cada estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-157">Each structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_PROCESS_INFORMATION {
    ULONG NextEntryOffset;
    ULONG NumberOfThreads;
    BYTE Reserved1[48];
    PVOID Reserved2[3];
    HANDLE UniqueProcessId;
    PVOID Reserved3;
    ULONG HandleCount;
    BYTE Reserved4[4];
    PVOID Reserved5[11];
    SIZE_T PeakPagefileUsage;
    SIZE_T PrivatePageCount;
    LARGE_INTEGER Reserved6[6];
} SYSTEM_PROCESS_INFORMATION;
```

<span data-ttu-id="eb841-158">El miembro **NumberOfThreads** contiene el número total de subprocesos que se están ejecutando actualmente en el proceso.</span><span class="sxs-lookup"><span data-stu-id="eb841-158">The **NumberOfThreads** member contains the total number of currently running threads in the process.</span></span>

<span data-ttu-id="eb841-159">El miembro **HandleCount** contiene el número total de identificadores que utiliza el proceso en cuestión; en su lugar, use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="eb841-159">The **HandleCount** member contains the total number of handles being used by the process in question; use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) to retrieve this information instead.</span></span>

<span data-ttu-id="eb841-160">El miembro **PeakPagefileUsage** contiene el número máximo de bytes de almacenamiento de archivo de paginación utilizado por el proceso y el miembro **PrivatePageCount** contiene el número de páginas de memoria asignadas para el uso de este proceso.</span><span class="sxs-lookup"><span data-stu-id="eb841-160">The **PeakPagefileUsage** member contains the maximum number of bytes of page-file storage used by the process, and the **PrivatePageCount** member contains the number of memory pages allocated for the use of this process.</span></span>

<span data-ttu-id="eb841-161">También puede recuperar esta información mediante la función [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) o la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) .</span><span class="sxs-lookup"><span data-stu-id="eb841-161">You can also retrieve this information using either the [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) function or the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span>

<span data-ttu-id="eb841-162">Los demás miembros de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-162">The other members of the structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span data-ttu-id="eb841-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_información de \_ rendimiento del procesador del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-163"><span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**SYSTEM\_PROCESSOR\_PERFORMANCE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-164">Cuando el parámetro *SystemInformationClass* es **SystemProcessorPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de **\_ \_ información de proceso del sistema** como procesadores (CPU) instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-164">When the *SystemInformationClass* parameter is **SystemProcessorPerformanceInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many **SYSTEM\_PROCESS\_INFORMATION** structures as there are processors (CPUs) installed in the system.</span></span> <span data-ttu-id="eb841-165">Cada estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-165">Each structure has the following layout:</span></span>

``` syntax
typedef struct
_SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION {
    LARGE_INTEGER IdleTime;
    LARGE_INTEGER KernelTime;
    LARGE_INTEGER UserTime;
    LARGE_INTEGER Reserved1[2];
    ULONG Reserved2;
} SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION;
```

<span data-ttu-id="eb841-166">El miembro **tiempodeinactividad** contiene la cantidad de tiempo que el sistema ha estado inactivo, en 1/100 $ de un nanosegundo.</span><span class="sxs-lookup"><span data-stu-id="eb841-166">The **IdleTime** member contains the amount of time that the system has been idle, in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="eb841-167">El miembro **KernelTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutarse en modo kernel (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 $ de un nanosegundo.</span><span class="sxs-lookup"><span data-stu-id="eb841-167">The **KernelTime** member contains the amount of time that the system has spent executing in Kernel mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="eb841-168">El miembro **UserTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutarse en modo de usuario (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 $ de un nanosegundo.</span><span class="sxs-lookup"><span data-stu-id="eb841-168">The **UserTime** member contains the amount of time that the system has spent executing in User mode (including all threads in all processes, on all processors), in 1/100ths of a nanosecond.</span></span>

<span data-ttu-id="eb841-169">En su lugar, use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="eb841-169">Use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) instead to retrieve this information.</span></span>

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span data-ttu-id="eb841-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_información de interrupción del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-170"><span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**SYSTEM\_INTERRUPT\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-171">Cuando el parámetro *SystemInformationClass* es **SystemInterruptInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de información de interrupción opacas **del sistema \_ \_** como procesadores (CPU) instalados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-171">When the *SystemInformationClass* parameter is **SystemInterruptInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an array that contains as many opaque **SYSTEM\_INTERRUPT\_INFORMATION** structures as there are processors (CPUs) installed on the system.</span></span> <span data-ttu-id="eb841-172">Cada estructura, o la matriz en su conjunto, se puede usar para generar un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-172">Each structure, or the array as a whole, can be used to generate an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-173">Para este propósito, la estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-173">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

<span data-ttu-id="eb841-174">Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-174">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="eb841-175">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.</span><span class="sxs-lookup"><span data-stu-id="eb841-175">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span data-ttu-id="eb841-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_información de excepción del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-176"><span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**SYSTEM\_EXCEPTION\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-177">Cuando el parámetro *SystemInformationClass* es **SystemExceptionInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de excepción del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-177">When the *SystemInformationClass* parameter is **SystemExceptionInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_EXCEPTION\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-178">Para este propósito, la estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-178">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

<span data-ttu-id="eb841-179">Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-179">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="eb841-180">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.</span><span class="sxs-lookup"><span data-stu-id="eb841-180">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span data-ttu-id="eb841-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_información de \_ cuota del registro del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-181"><span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**SYSTEM\_REGISTRY\_QUOTA\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-182">Cuando el parámetro *SystemInformationClass* es **SystemRegistryQuotaInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ \_ información de cuota del registro del sistema** con el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-182">When the *SystemInformationClass* parameter is **SystemRegistryQuotaInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold a single **SYSTEM\_REGISTRY\_QUOTA\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

<span data-ttu-id="eb841-183">El miembro **RegistryQuotaAllowed** contiene el tamaño máximo, en bytes, que el registro puede alcanzar en este sistema.</span><span class="sxs-lookup"><span data-stu-id="eb841-183">The **RegistryQuotaAllowed** member contains the maximum size, in bytes, that the Registry can attain on this system.</span></span>

<span data-ttu-id="eb841-184">El miembro **RegistryQuotaUsed** contiene el tamaño actual del registro, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb841-184">The **RegistryQuotaUsed** member contains the current size of the Registry, in bytes.</span></span>

<span data-ttu-id="eb841-185">En su lugar, use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="eb841-185">Use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) instead to retrieve this information.</span></span>

<span data-ttu-id="eb841-186">El otro miembro de la estructura está reservado para uso interno por parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-186">The other member of the structure is reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span data-ttu-id="eb841-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_información de traducción del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="eb841-187"><span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**SYSTEM\_LOOKASIDE\_INFORMATION**</span></span>


</dt> <dd>

<span data-ttu-id="eb841-188">Cuando el parámetro *SystemInformationClass* es **SystemLookasideInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de traducción del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios.</span><span class="sxs-lookup"><span data-stu-id="eb841-188">When the *SystemInformationClass* parameter is **SystemLookasideInformation**, the buffer pointed to by the *SystemInformation* parameter should be large enough to hold an opaque **SYSTEM\_LOOKASIDE\_INFORMATION** structure for use in generating an unpredictable seed for a random number generator.</span></span> <span data-ttu-id="eb841-189">Para este propósito, la estructura tiene el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="eb841-189">For this purpose, the structure has the following layout:</span></span>

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

<span data-ttu-id="eb841-190">Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-190">Individual members of the structure are reserved for internal use by the operating system.</span></span>

<span data-ttu-id="eb841-191">En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.</span><span class="sxs-lookup"><span data-stu-id="eb841-191">Use the [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) function instead to generate cryptographically random data.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="eb841-192">*SystemInformationLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eb841-192">*SystemInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb841-193">Tamaño del búfer al que apunta el parámetro *SystemInformation* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb841-193">The size of the buffer pointed to by the *SystemInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eb841-194">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eb841-194">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb841-195">Un puntero opcional a una ubicación donde la función escribe el tamaño real de la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb841-195">An optional pointer to a location where the function writes the actual size of the information requested.</span></span> <span data-ttu-id="eb841-196">Si el tamaño es menor o igual que el parámetro *SystemInformationLength* , la función copia la información en el búfer *SystemInformation* ; de lo contrario, devuelve un código de error NTSTATUS y devuelve en *ReturnLength* el tamaño del búfer necesario para recibir la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb841-196">If that size is less than or equal to the *SystemInformationLength* parameter, the function copies the information into the *SystemInformation* buffer; otherwise, it returns an NTSTATUS error code and returns in *ReturnLength* the size of buffer required to receive the requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb841-197">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb841-197">Return value</span></span>

<span data-ttu-id="eb841-198">Devuelve un código de error o correcto de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="eb841-198">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="eb841-199">Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el DDK y se describen en la documentación de DDK.</span><span class="sxs-lookup"><span data-stu-id="eb841-199">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb841-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb841-200">Remarks</span></span>

<span data-ttu-id="eb841-201">La función **ZwQuerySystemInformation** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.</span><span class="sxs-lookup"><span data-stu-id="eb841-201">The **ZwQuerySystemInformation** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="eb841-202">Para mantener la compatibilidad de la aplicación, es mejor usar en su lugar las funciones alternativas mencionadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="eb841-202">To maintain the compatibility of your application, it is better to use the alternate functions previously mentioned instead.</span></span>

<span data-ttu-id="eb841-203">Si usa **ZwQuerySystemInformation**, acceda a la función a través [de la vinculación dinámica en tiempo de ejecución](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span><span class="sxs-lookup"><span data-stu-id="eb841-203">If you do use **ZwQuerySystemInformation**, access the function through [run-time dynamic linking](/windows/desktop/Dlls/using-run-time-dynamic-linking).</span></span> <span data-ttu-id="eb841-204">Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eb841-204">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="eb841-205">Sin embargo, es posible que los cambios en la firma no se puedan detectar.</span><span class="sxs-lookup"><span data-stu-id="eb841-205">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="eb841-206">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="eb841-206">This function has no associated import library.</span></span> <span data-ttu-id="eb841-207">Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="eb841-207">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb841-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb841-208">Requirements</span></span>



| <span data-ttu-id="eb841-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb841-209">Requirement</span></span> | <span data-ttu-id="eb841-210">Value</span><span class="sxs-lookup"><span data-stu-id="eb841-210">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eb841-211">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb841-211">DLL</span></span><br/> | <dl> <span data-ttu-id="eb841-212"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb841-212"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb841-213">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb841-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb841-214">**GetSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="eb841-214">**GetSystemInfo**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[<span data-ttu-id="eb841-215">**GetProcessHandleCount**</span><span class="sxs-lookup"><span data-stu-id="eb841-215">**GetProcessHandleCount**</span></span>](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[<span data-ttu-id="eb841-216">**GetProcessMemoryInfo**</span><span class="sxs-lookup"><span data-stu-id="eb841-216">**GetProcessMemoryInfo**</span></span>](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[<span data-ttu-id="eb841-217">**GetSystemTimes**</span><span class="sxs-lookup"><span data-stu-id="eb841-217">**GetSystemTimes**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[<span data-ttu-id="eb841-218">**GetSystemRegistryQuota**</span><span class="sxs-lookup"><span data-stu-id="eb841-218">**GetSystemRegistryQuota**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 


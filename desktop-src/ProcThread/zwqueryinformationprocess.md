---
description: Recupera información sobre el proceso especificado.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: ZwQueryInformationProcess función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ZwQueryInformationProcess
api_type:
- DllExport
api_location:
- Ntdll.dll
- ntoskrnl.exe
ms.openlocfilehash: 30207c8d3d54c54f77194b542e10e9fee94e055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677820"
---
# <a name="zwqueryinformationprocess-function"></a><span data-ttu-id="cfbdf-103">ZwQueryInformationProcess función)</span><span class="sxs-lookup"><span data-stu-id="cfbdf-103">ZwQueryInformationProcess function</span></span>

<span data-ttu-id="cfbdf-104">\[**ZwQueryInformationProcess** puede modificarse o no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-104">\[**ZwQueryInformationProcess** may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="cfbdf-105">Las aplicaciones deben usar las funciones alternativas que se enumeran en este tema.\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-105">Applications should use the alternate functions listed in this topic.\]</span></span>

<span data-ttu-id="cfbdf-106">Recupera información sobre el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-106">Retrieves information about the specified process.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbdf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfbdf-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="cfbdf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfbdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbdf-109">*ProcessHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-109">*ProcessHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-110">Identificador del proceso para el que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-110">A handle to the process for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cfbdf-111">*ProcessInformationClass* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-111">*ProcessInformationClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-112">Tipo de información de proceso que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-112">The type of process information to be retrieved.</span></span> <span data-ttu-id="cfbdf-113">Este parámetro puede ser uno de los siguientes valores de la enumeración **PROCESSINFOCLASS** .</span><span class="sxs-lookup"><span data-stu-id="cfbdf-113">This parameter can be one of the following values from the **PROCESSINFOCLASS** enumeration.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfbdf-114">Value</span><span class="sxs-lookup"><span data-stu-id="cfbdf-114">Value</span></span></th>
<th><span data-ttu-id="cfbdf-115">Significado</span><span class="sxs-lookup"><span data-stu-id="cfbdf-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <span data-ttu-id="cfbdf-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-116"><dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-117">Recupera un puntero a una estructura PEB que se puede usar para determinar si se está depurando el proceso especificado y un valor único que utiliza el sistema para identificar el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-117">Retrieves a pointer to a PEB structure that can be used to determine whether the specified process is being debugged, and a unique value used by the system to identify the specified process.</span></span> <br/> <span data-ttu-id="cfbdf-118">Es mejor usar las funciones <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> y <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>getprocessid (</strong></a> para obtener esta información.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-118">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> functions to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <span data-ttu-id="cfbdf-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-119"><dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-120">Recupera un valor de <strong>DWORD_PTR</strong> que es el número de puerto del depurador para el proceso.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-120">Retrieves a <strong>DWORD_PTR</strong> value that is the port number of the debugger for the process.</span></span> <span data-ttu-id="cfbdf-121">Un valor distinto de cero indica que el proceso se ejecuta bajo el control de un depurador de anillo 3.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-121">A nonzero value indicates that the process is being run under the control of a ring 3 debugger.</span></span><br/> <span data-ttu-id="cfbdf-122">Es mejor usar la función <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> o <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cfbdf-122">It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> or <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <span data-ttu-id="cfbdf-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-123"><dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-124">Determina si el proceso se está ejecutando en el entorno WOW64 (WOW64 es el emulador x86 que permite que las aplicaciones basadas en Win32 se ejecuten en Windows de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="cfbdf-124">Determines whether the process is running in the WOW64 environment (WOW64 is the x86 emulator that allows Win32-based applications to run on 64-bit Windows).</span></span><br/> <span data-ttu-id="cfbdf-125">Es mejor usar la función <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> para obtener esta información.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-125">It is best to use the <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> function to obtain this information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <span data-ttu-id="cfbdf-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-126"><dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-127">Recupera un valor de <strong>UNICODE_STRING</strong> que contiene el nombre del archivo de imagen para el proceso.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-127">Retrieves a <strong>UNICODE_STRING</strong> value containing the name of the image file for the process.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <span data-ttu-id="cfbdf-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-128"><dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-129">Recupera un valor <strong>ULong</strong> que indica si el proceso se considera crítico.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-129">Retrieves a <strong>ULONG</strong> value indicating whether the process is considered critical.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="cfbdf-130">Este valor se puede usar a partir de Windows XP con SP3.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-130">This value can be used starting in Windows XP with SP3.</span></span> <span data-ttu-id="cfbdf-131">A partir de Windows 8.1, se debe usar <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-131">Starting in Windows 8.1, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> should be used instead.</span></span>
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <span data-ttu-id="cfbdf-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span><span class="sxs-lookup"><span data-stu-id="cfbdf-132"><dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </span></span></dl></td>
<td><span data-ttu-id="cfbdf-133">Recupera un valor de BYTE que indica el tipo de proceso protegido y el firmante del proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-133">Retrieves a BYTE value indicating the type of protected process and the protected process signer.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="cfbdf-134">*ProcessInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-134">*ProcessInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-135">Puntero a un búfer proporcionado por la aplicación que realiza la llamada en la que la función escribe la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-135">A pointer to a buffer supplied by the calling application into which the function writes the requested information.</span></span> <span data-ttu-id="cfbdf-136">El tamaño de la información escrita varía en función del valor del parámetro *ProcessInformationClass* :</span><span class="sxs-lookup"><span data-stu-id="cfbdf-136">The size of the information written varies depending on the value of the *ProcessInformationClass* parameter:</span></span>

<dl> <dt>

<span data-ttu-id="cfbdf-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESAR \_ \_ información básica</span><span class="sxs-lookup"><span data-stu-id="cfbdf-137"><span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESS\_BASIC\_INFORMATION</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-138">Cuando el parámetro *ProcessInformationClass* es **ProcessBasicInformation**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ información básica de proceso** con el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="cfbdf-138">When the *ProcessInformationClass* parameter is **ProcessBasicInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PROCESS\_BASIC\_INFORMATION** structure having the following layout:</span></span>

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

<span data-ttu-id="cfbdf-139">El miembro **UniqueProcessId** apunta al identificador único del sistema para este proceso.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-139">The **UniqueProcessId** member points to the system's unique identifier for this process.</span></span> <span data-ttu-id="cfbdf-140">Es mejor usar la función [**getprocessid (**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) para recuperar esta información.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-140">It is best to use the [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) function to retrieve this information.</span></span>

<span data-ttu-id="cfbdf-141">El miembro **PebBaseAddress** apunta a una estructura [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .</span><span class="sxs-lookup"><span data-stu-id="cfbdf-141">The **PebBaseAddress** member points to a [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) structure.</span></span>

<span data-ttu-id="cfbdf-142">Los demás miembros de esta estructura se reservan para uso interno del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-142">The other members of this structure are reserved for internal use by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cfbdf-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ ptr</span><span class="sxs-lookup"><span data-stu-id="cfbdf-143"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG\_PTR</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-144">Cuando el parámetro *ProcessInformationClass* es **ProcessWow64Information**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener un **ULong \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-144">When the *ProcessInformationClass* parameter is **ProcessWow64Information**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **ULONG\_PTR**.</span></span> <span data-ttu-id="cfbdf-145">Si este valor es distinto de cero, el proceso se ejecuta en un entorno WOW64; de lo contrario, si el valor es igual a cero, el proceso no se está ejecutando en un entorno WOW64.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-145">If this value is nonzero, the process is running in a WOW64 environment; otherwise, if the value is equal to zero, the process is not running in a WOW64 environment.</span></span>

<span data-ttu-id="cfbdf-146">Es mejor usar la función [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) para determinar si un proceso se está ejecutando en el entorno WOW64.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-146">It is best to use the [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) function to determine whether a process is running in the WOW64 environment.</span></span>

</dd> <dt>

<span data-ttu-id="cfbdf-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>cadena Unicode \_</span><span class="sxs-lookup"><span data-stu-id="cfbdf-147"><span id="UNICODE_STRING"></span><span id="unicode_string"></span>UNICODE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-148">Cuando el parámetro *ProcessInformationClass* es **ProcessImageFileName**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ cadena Unicode** , así como la propia cadena.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-148">When the *ProcessInformationClass* parameter is **ProcessImageFileName**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a **UNICODE\_STRING** structure as well as the string itself.</span></span> <span data-ttu-id="cfbdf-149">La cadena almacenada en el miembro del **búfer** es el nombre del archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-149">The string stored in the **Buffer** member is the name of the image file.</span></span>

<span data-ttu-id="cfbdf-150">Si el búfer es demasiado pequeño, se produce un error en la función con el código de error de coincidencia de longitud de información de estado \_ \_ \_ y el parámetro *ReturnLength* se establece en el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-150">If the buffer is too small, the function fails with the STATUS\_INFO\_LENGTH\_MISMATCH error code and the *ReturnLength* parameter is set to the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="cfbdf-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span><span class="sxs-lookup"><span data-stu-id="cfbdf-151"><span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-152">Cuando el parámetro *ProcessInformationClass* es **ProcessProtectionInformation**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única estructura de **PS_PROTECTION** que tenga el siguiente diseño:</span><span class="sxs-lookup"><span data-stu-id="cfbdf-152">When the *ProcessInformationClass* parameter is **ProcessProtectionInformation**, the buffer pointed to by the *ProcessInformation* parameter should be large enough to hold a single **PS_PROTECTION** structure having the following layout:</span></span>

``` syntax
typedef struct _PS_PROTECTION {
    union {
        UCHAR Level;
        struct {
            UCHAR Type   : 3;
            UCHAR Audit  : 1;                  // Reserved
            UCHAR Signer : 4;
        };
    };
} PS_PROTECTION, *PPS_PROTECTION;
```

<span data-ttu-id="cfbdf-153">Los primeros 3 bits contienen el tipo de proceso protegido:</span><span class="sxs-lookup"><span data-stu-id="cfbdf-153">The first 3 bits contain the type of protected process:</span></span>

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

<span data-ttu-id="cfbdf-154">Los 4 bits principales contienen el firmante del proceso protegido:</span><span class="sxs-lookup"><span data-stu-id="cfbdf-154">The top 4 bits contain the protected process signer:</span></span>

``` syntax
typedef enum _PS_PROTECTED_SIGNER {
    PsProtectedSignerNone = 0,
    PsProtectedSignerAuthenticode,
    PsProtectedSignerCodeGen,
    PsProtectedSignerAntimalware,
    PsProtectedSignerLsa,
    PsProtectedSignerWindows,
    PsProtectedSignerWinTcb,
    PsProtectedSignerWinSystem,
    PsProtectedSignerApp,
    PsProtectedSignerMax
} PS_PROTECTED_SIGNER, *PPS_PROTECTED_SIGNER;
```

</dd> </dl> </dd> <dt>

<span data-ttu-id="cfbdf-155">*ProcessInformationLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-155">*ProcessInformationLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-156">Tamaño del búfer al que apunta el parámetro *ProcessInformation* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-156">The size of the buffer pointed to by the *ProcessInformation* parameter, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cfbdf-157">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-157">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cfbdf-158">Puntero a una variable en la que la función devuelve el tamaño de la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-158">A pointer to a variable in which the function returns the size of the requested information.</span></span> <span data-ttu-id="cfbdf-159">Si la función se realizó correctamente, es el tamaño de la información escrita en el búfer al que apunta el parámetro *ProcessInformation* , pero si el búfer es demasiado pequeño, es el tamaño mínimo del búfer necesario para recibir la información correctamente.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-159">If the function was successful, this is the size of the information written to the buffer pointed to by the *ProcessInformation* parameter, but if the buffer was too small, this is the minimum size of buffer needed to receive the information successfully.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbdf-160">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfbdf-160">Return value</span></span>

<span data-ttu-id="cfbdf-161">Devuelve un código de error o correcto de NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-161">Returns an NTSTATUS success or error code.</span></span>

<span data-ttu-id="cfbdf-162">Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el DDK y se describen en la documentación de DDK en Kernel-Mode guía de arquitectura/diseño de controladores/guías de programación de controladores/errores de registro.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-162">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbdf-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfbdf-163">Remarks</span></span>

<span data-ttu-id="cfbdf-164">La función **ZwQueryInformationProcess** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-164">The **ZwQueryInformationProcess** function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="cfbdf-165">Para mantener la compatibilidad de la aplicación, es mejor usar las funciones públicas que se mencionan en la descripción del parámetro *ProcessInformationClass* en su lugar.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-165">To maintain the compatibility of your application, it is better to use public functions mentioned in the description of the *ProcessInformationClass* parameter instead.</span></span>

<span data-ttu-id="cfbdf-166">Si usa **ZwQueryInformationProcess**, acceda a la función a través [de la vinculación dinámica en tiempo de ejecución](../dlls/using-run-time-dynamic-linking.md).</span><span class="sxs-lookup"><span data-stu-id="cfbdf-166">If you do use **ZwQueryInformationProcess**, access the function through [run-time dynamic linking](../dlls/using-run-time-dynamic-linking.md).</span></span> <span data-ttu-id="cfbdf-167">Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-167">This gives your code an opportunity to respond gracefully if the function has been changed or removed from the operating system.</span></span> <span data-ttu-id="cfbdf-168">Sin embargo, es posible que los cambios en la firma no se puedan detectar.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-168">Signature changes, however, may not be detectable.</span></span>

<span data-ttu-id="cfbdf-169">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-169">This function has no associated import library.</span></span> <span data-ttu-id="cfbdf-170">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="cfbdf-170">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbdf-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfbdf-171">Requirements</span></span>



| <span data-ttu-id="cfbdf-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfbdf-172">Requirement</span></span> | <span data-ttu-id="cfbdf-173">Value</span><span class="sxs-lookup"><span data-stu-id="cfbdf-173">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbdf-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfbdf-174">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbdf-175">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-175">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cfbdf-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfbdf-176">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbdf-177">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cfbdf-177">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cfbdf-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfbdf-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfbdf-179"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfbdf-179"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbdf-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfbdf-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbdf-181">**CheckRemoteDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="cfbdf-181">**CheckRemoteDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[<span data-ttu-id="cfbdf-182">**Getprocessid (**</span><span class="sxs-lookup"><span data-stu-id="cfbdf-182">**GetProcessId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[<span data-ttu-id="cfbdf-183">**IsDebuggerPresent**</span><span class="sxs-lookup"><span data-stu-id="cfbdf-183">**IsDebuggerPresent**</span></span>](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[<span data-ttu-id="cfbdf-184">**IsWow64Process**</span><span class="sxs-lookup"><span data-stu-id="cfbdf-184">**IsWow64Process**</span></span>](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 

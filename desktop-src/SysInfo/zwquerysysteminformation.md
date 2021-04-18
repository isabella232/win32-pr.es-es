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
# <a name="zwquerysysteminformation-function"></a>ZwQuerySystemInformation función)

\[**ZwQuerySystemInformation** ya no está disponible para su uso a partir de Windows 8. En su lugar, use las funciones alternativas que se enumeran en este tema.\]

Recupera la información del sistema especificada.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ZwQuerySystemInformation(
  _In_      SYSTEM_INFORMATION_CLASS SystemInformationClass,
  _Inout_   PVOID                    SystemInformation,
  _In_      ULONG                    SystemInformationLength,
  _Out_opt_ PULONG                   ReturnLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SystemInformationClass* \[ de\]
</dt> <dd>

Tipo de información del sistema que se va a recuperar. Este parámetro puede ser uno de los siguientes valores del tipo de enumeración **\_ \_ clase de información del sistema** .

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

Número de procesadores del sistema en una estructura de **\_ \_ información básica del sistema** . En su lugar, use la función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

Una estructura **de \_ \_ información de rendimiento del sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios. En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

Estructura de **\_ \_ información TIMEOFDAY del sistema** opaca que se puede usar para generar un valor de inicialización imprevisible para un generador de números aleatorios. En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

Una matriz de estructuras de **\_ \_ información de proceso del sistema** , una para cada proceso que se ejecuta en el sistema.

Estas estructuras contienen información sobre el uso de recursos de cada proceso, incluido el número de identificadores utilizados por el proceso, el uso de archivo de página máximo y el número de páginas de memoria que el proceso ha asignado.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

Una matriz de estructuras de **\_ información de \_ rendimiento \_ de procesador del sistema** , una para cada procesador instalado en el sistema.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

Estructura de **\_ \_ información de interrupción opaca del sistema** que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios. En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

Estructura de **\_ \_ información de excepción de sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios. En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

Estructura **de \_ \_ \_ información de cuota del registro del sistema** .

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

Estructura de **\_ \_ información de direcciones de sistema** opaca que se puede usar para generar un valor de inicialización impredecible para un generador de números aleatorios. En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .

</dd> </dl> </dd> <dt>

*SystemInformation* \[ in, out\]
</dt> <dd>

Un puntero a un búfer que recibe la información solicitada. El tamaño y la estructura de esta información varía en función del valor del parámetro *SystemInformationClass* , como se indica en la tabla siguiente.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**\_información básica del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemBasicInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ información básica del sistema** con el siguiente diseño:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

El miembro **NumberOfProcessors** contiene el número de procesadores presentes en el sistema. En su lugar, use [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) para recuperar esta información.

Los demás miembros de la estructura se reservan para uso interno del sistema operativo.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**\_información de rendimiento del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de rendimiento del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios. Para este propósito, la estructura tiene el siguiente diseño:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.

En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**\_información de TIMEOFDAY del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemTimeOfDayInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información TIMEOFDAY del sistema** opaca que se usará para generar un valor de inicialización imprevisible para un generador de números aleatorios. Para este propósito, la estructura tiene el siguiente diseño:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.

En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**\_información del proceso del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemProcessInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de **\_ \_ información de proceso del sistema** como procesos en ejecución en el sistema. Cada estructura tiene el siguiente diseño:

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

El miembro **NumberOfThreads** contiene el número total de subprocesos que se están ejecutando actualmente en el proceso.

El miembro **HandleCount** contiene el número total de identificadores que utiliza el proceso en cuestión; en su lugar, use [**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) para recuperar esta información.

El miembro **PeakPagefileUsage** contiene el número máximo de bytes de almacenamiento de archivo de paginación utilizado por el proceso y el miembro **PrivatePageCount** contiene el número de páginas de memoria asignadas para el uso de este proceso.

También puede recuperar esta información mediante la función [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) o la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) .

Los demás miembros de la estructura se reservan para uso interno del sistema operativo.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**\_información de \_ rendimiento del procesador del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemProcessorPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de **\_ \_ información de proceso del sistema** como procesadores (CPU) instalados en el sistema. Cada estructura tiene el siguiente diseño:

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

El miembro **tiempodeinactividad** contiene la cantidad de tiempo que el sistema ha estado inactivo, en 1/100 $ de un nanosegundo.

El miembro **KernelTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutarse en modo kernel (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 $ de un nanosegundo.

El miembro **UserTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutarse en modo de usuario (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 $ de un nanosegundo.

En su lugar, use [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) para recuperar esta información.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**\_información de interrupción del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemInterruptInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras de información de interrupción opacas **del sistema \_ \_** como procesadores (CPU) instalados en el sistema. Cada estructura, o la matriz en su conjunto, se puede usar para generar un valor de inicialización imprevisible para un generador de números aleatorios. Para este propósito, la estructura tiene el siguiente diseño:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.

En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**\_información de excepción del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemExceptionInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de excepción del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios. Para este propósito, la estructura tiene el siguiente diseño:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.

En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**\_información de \_ cuota del registro del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemRegistryQuotaInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ \_ información de cuota del registro del sistema** con el siguiente diseño:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

El miembro **RegistryQuotaAllowed** contiene el tamaño máximo, en bytes, que el registro puede alcanzar en este sistema.

El miembro **RegistryQuotaUsed** contiene el tamaño actual del registro, en bytes.

En su lugar, use [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) para recuperar esta información.

El otro miembro de la estructura está reservado para uso interno por parte del sistema operativo.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**\_información de traducción del sistema \_**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemLookasideInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ \_ información de traducción del sistema** opaca para su uso en la generación de un valor de inicialización imprevisible para un generador de números aleatorios. Para este propósito, la estructura tiene el siguiente diseño:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

Los miembros individuales de la estructura se reservan para uso interno del sistema operativo.

En su lugar, use la función [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) para generar datos aleatorios criptográficamente.

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta el parámetro *SystemInformation* , en bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Un puntero opcional a una ubicación donde la función escribe el tamaño real de la información solicitada. Si el tamaño es menor o igual que el parámetro *SystemInformationLength* , la función copia la información en el búfer *SystemInformation* ; de lo contrario, devuelve un código de error NTSTATUS y devuelve en *ReturnLength* el tamaño del búfer necesario para recibir la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de error o correcto de NTSTATUS.

Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el DDK y se describen en la documentación de DDK.

## <a name="remarks"></a>Observaciones

La función **ZwQuerySystemInformation** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar en su lugar las funciones alternativas mencionadas anteriormente.

Si usa **ZwQuerySystemInformation**, acceda a la función a través [de la vinculación dinámica en tiempo de ejecución](/windows/desktop/Dlls/using-run-time-dynamic-linking). Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios en la firma no se puedan detectar.

Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 


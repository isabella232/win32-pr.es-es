---
description: Recupera la información del sistema especificada.
ms.assetid: c91b9a35-ca2b-4d81-973d-fe709144df90
title: Función ZwQuerySystemInformation
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
ms.openlocfilehash: 24652888ad5ed299e33039c41a9c4ac58bf3441683df4cbcf9d581c50d4b8cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957298"
---
# <a name="zwquerysysteminformation-function"></a>Función ZwQuerySystemInformation

\[**ZwQuerySystemInformation** ya no está disponible para su uso a Windows 8. En su lugar, use las funciones alternativas enumeradas en este tema.\]

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

*SystemInformationClass* \[ En\]
</dt> <dd>

Tipo de información del sistema que se va a recuperar. Este parámetro puede ser uno de los siguientes valores del tipo de **enumeración SYSTEM \_ INFORMATION \_ CLASS.**

<dt>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>

<span id="SystemBasicInformation"></span><span id="systembasicinformation"></span><span id="SYSTEMBASICINFORMATION"></span>**SystemBasicInformation**


</dt> <dd>

Número de procesadores del sistema en una **estructura SYSTEM \_ BASIC \_ INFORMATION.** En su [**lugar, use la función GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

</dd> <dt>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>

<span id="SystemPerformanceInformation"></span><span id="systemperformanceinformation"></span><span id="SYSTEMPERFORMANCEINFORMATION"></span>**SystemPerformanceInformation**


</dt> <dd>

Estructura **opaca SYSTEM \_ PERFORMANCE \_ INFORMATION** que se puede usar para generar un valor de ed. imprevisible para un generador de números aleatorios. En su [**lugar, use la función CryptGenRandom.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)

</dd> <dt>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>

<span id="SystemTimeOfDayInformation"></span><span id="systemtimeofdayinformation"></span><span id="SYSTEMTIMEOFDAYINFORMATION"></span>**SystemTimeOfDayInformation**


</dt> <dd>

Estructura **opaca SYSTEM \_ TIMEOFDAY \_ INFORMATION** que se puede usar para generar un valor de ed. imprevisible para un generador de números aleatorios. En su [**lugar, use la función CryptGenRandom.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)

</dd> <dt>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>

<span id="SystemProcessInformation"></span><span id="systemprocessinformation"></span><span id="SYSTEMPROCESSINFORMATION"></span>**SystemProcessInformation**


</dt> <dd>

Matriz de **estructuras SYSTEM \_ PROCESS \_ INFORMATION,** una para cada proceso que se ejecuta en el sistema.

Estas estructuras contienen información sobre el uso de recursos de cada proceso, incluido el número de identificadores usados por el proceso, el uso máximo de archivos de página y el número de páginas de memoria que el proceso ha asignado.

</dd> <dt>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>

<span id="SystemProcessorPerformanceInformation"></span><span id="systemprocessorperformanceinformation"></span><span id="SYSTEMPROCESSORPERFORMANCEINFORMATION"></span>**SystemProcessorPerformanceInformation**


</dt> <dd>

Matriz de estructuras **SYSTEM \_ PROCESSOR PERFORMANCE \_ \_ INFORMATION,** una para cada procesador instalado en el sistema.

</dd> <dt>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>

<span id="SystemInterruptInformation"></span><span id="systeminterruptinformation"></span><span id="SYSTEMINTERRUPTINFORMATION"></span>**SystemInterruptInformation**


</dt> <dd>

Estructura **opaca SYSTEM \_ INTERRUPT \_ INFORMATION** que se puede usar para generar un valor de ed. imprevisible para un generador de números aleatorios. En su [**lugar, use la función CryptGenRandom.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)

</dd> <dt>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>

<span id="SystemExceptionInformation"></span><span id="systemexceptioninformation"></span><span id="SYSTEMEXCEPTIONINFORMATION"></span>**SystemExceptionInformation**


</dt> <dd>

Estructura **opaca SYSTEM \_ EXCEPTION \_ INFORMATION** que se puede usar para generar un valor de ed. imprevisible para un generador de números aleatorios. En su [**lugar, use la función CryptGenRandom.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)

</dd> <dt>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>

<span id="SystemRegistryQuotaInformation"></span><span id="systemregistryquotainformation"></span><span id="SYSTEMREGISTRYQUOTAINFORMATION"></span>**SystemRegistryQuotaInformation**


</dt> <dd>

Estructura **SYSTEM REGISTRY QUOTA \_ \_ \_ INFORMATION.**

</dd> <dt>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>

<span id="SystemLookasideInformation"></span><span id="systemlookasideinformation"></span><span id="SYSTEMLOOKASIDEINFORMATION"></span>**SystemLookasideInformation**


</dt> <dd>

Estructura **opaca SYSTEM \_ LOOKASIDE \_ INFORMATION** que se puede usar para generar un valor de ed. imprevisible para un generador de números aleatorios. En su [**lugar, use la función CryptGenRandom.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)

</dd> </dl> </dd> <dt>

*SystemInformation* \[ in, out\]
</dt> <dd>

Puntero a un búfer que recibe la información solicitada. El tamaño y la estructura de esta información varían en función del valor del parámetro *SystemInformationClass,* como se indica en la tabla siguiente.

<dt>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>

<span id="SYSTEM_BASIC_INFORMATION"></span><span id="system_basic_information"></span>**INFORMACIÓN \_ BÁSICA DEL \_ SISTEMA**


</dt> <dd>

Cuando el *parámetro SystemInformationClass* es **SystemBasicInformation,** el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura **SYSTEM BASIC \_ \_ INFORMATION** con el diseño siguiente:

``` syntax
typedef struct _SYSTEM_BASIC_INFORMATION {
    BYTE Reserved1[24];
    PVOID Reserved2[4];
    CCHAR NumberOfProcessors;
} SYSTEM_BASIC_INFORMATION;
```

El **miembro NumberOfProcessors** contiene el número de procesadores presentes en el sistema. Use [**GetSystemInfo en**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) su lugar para recuperar esta información.

El sistema operativo reserva los demás miembros de la estructura para su uso interno.

</dd> <dt>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>

<span id="SYSTEM_PERFORMANCE_INFORMATION"></span><span id="system_performance_information"></span>**INFORMACIÓN DE \_ RENDIMIENTO DEL \_ SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura **opaca SYSTEM \_ PERFORMANCE \_ INFORMATION** para su uso en la generación de un valor de ed. imprevisible para un generador de números aleatorios. Para ello, la estructura tiene el diseño siguiente:

``` syntax
typedef struct _SYSTEM_PERFORMANCE_INFORMATION {
    BYTE Reserved1[312];
} SYSTEM_PERFORMANCE_INFORMATION;
```

El sistema operativo reserva miembros individuales de la estructura para su uso interno.

Use la [**función CryptGenRandom en**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) su lugar para generar datos criptográficos aleatorios.

</dd> <dt>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>

<span id="SYSTEM_TIMEOFDAY_INFORMATION"></span><span id="system_timeofday_information"></span>**INFORMACIÓN \_ DE TIMEOFDAY DEL \_ SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemTimeOfDayInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura **opaca SYSTEM \_ TIMEOFDAY \_ INFORMATION** para su uso en la generación de un valor de ed. imprevisible para un generador de números aleatorios. Para ello, la estructura tiene el diseño siguiente:

``` syntax
typedef struct _SYSTEM_TIMEOFDAY_INFORMATION {
    BYTE Reserved1[48];
} SYSTEM_TIMEOFDAY_INFORMATION;
```

El sistema operativo reserva miembros individuales de la estructura para su uso interno.

Use la [**función CryptGenRandom en**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) su lugar para generar datos criptográficos aleatorios.

</dd> <dt>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>

<span id="SYSTEM_PROCESS_INFORMATION"></span><span id="system_process_information"></span>**INFORMACIÓN DEL \_ PROCESO \_ DEL SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemProcessInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras **SYSTEM PROCESS \_ \_ INFORMATION** como procesos se ejecuten en el sistema. Cada estructura tiene el diseño siguiente:

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

El **miembro NumberOfThreads** contiene el número total de subprocesos que se están ejecutando actualmente en el proceso.

El **miembro HandleCount** contiene el número total de identificadores que usa el proceso en cuestión; use [**GetProcessHandleCount para**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount) recuperar esta información en su lugar.

El **miembro PeakPagefileUsage** contiene el número máximo de bytes de almacenamiento de archivos de página usados por el proceso y el miembro **PrivatePageCount** contiene el número de páginas de memoria asignadas para el uso de este proceso.

También puede recuperar esta información mediante la función [**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo) o la [**clase Win32 \_ Process.**](/windows/desktop/CIMWin32Prov/win32-process)

El sistema operativo reserva los demás miembros de la estructura para su uso interno.

</dd> <dt>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>

<span id="SYSTEM_PROCESSOR_PERFORMANCE_INFORMATION"></span><span id="system_processor_performance_information"></span>**INFORMACIÓN DE \_ RENDIMIENTO DEL PROCESADOR DEL \_ \_ SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemProcessorPerformanceInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras **SYSTEM PROCESS \_ \_ INFORMATION** como procesadores (CPU) instalados en el sistema. Cada estructura tiene el diseño siguiente:

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

El **miembro IdleTime** contiene la cantidad de tiempo que el sistema ha estado inactivo, en 1/100 segundos de un nanosegundo.

El **miembro KernelTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutar en modo kernel (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 segundos de un nanosegundo.

El **miembro UserTime** contiene la cantidad de tiempo que el sistema ha dedicado a ejecutar en modo usuario (incluidos todos los subprocesos de todos los procesos, en todos los procesadores), en 1/100 segundos de un nanosegundo.

Use [**GetSystemTimes en**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) su lugar para recuperar esta información.

</dd> <dt>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>

<span id="SYSTEM_INTERRUPT_INFORMATION"></span><span id="system_interrupt_information"></span>**INFORMACIÓN DE \_ INTERRUPCIÓN \_ DEL SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemInterruptInformation,** el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una matriz que contenga tantas estructuras opacas **de SYSTEM INTERRUPT \_ \_ INFORMATION** como procesadores (CPU) instalados en el sistema. Cada estructura, o la matriz en su conjunto, se puede usar para generar un valor de matriz impredecible para un generador de números aleatorios. Para ello, la estructura tiene el diseño siguiente:

``` syntax
typedef struct _SYSTEM_INTERRUPT_INFORMATION {
    BYTE Reserved1[24];
} SYSTEM_INTERRUPT_INFORMATION;
```

El sistema operativo reserva miembros individuales de la estructura para su uso interno.

Use la [**función CryptGenRandom en**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) su lugar para generar datos criptográficos aleatorios.

</dd> <dt>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>

<span id="SYSTEM_EXCEPTION_INFORMATION"></span><span id="system_exception_information"></span>**INFORMACIÓN DE \_ EXCEPCIONES \_ DEL SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemExceptionInformation,** el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura **opaca SYSTEM \_ EXCEPTION \_ INFORMATION** para su uso en la generación de un valor de ed. imprevisible para un generador de números aleatorios. Para ello, la estructura tiene el diseño siguiente:

``` syntax
typedef struct _SYSTEM_EXCEPTION_INFORMATION {
    BYTE Reserved1[16];
} SYSTEM_EXCEPTION_INFORMATION;
```

El sistema operativo reserva miembros individuales de la estructura para su uso interno.

Use la [**función CryptGenRandom en**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) su lugar para generar datos criptográficos aleatorios.

</dd> <dt>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>

<span id="SYSTEM_REGISTRY_QUOTA_INFORMATION"></span><span id="system_registry_quota_information"></span>**INFORMACIÓN DE \_ CUOTA DEL REGISTRO DEL \_ \_ SISTEMA**


</dt> <dd>

Cuando el *parámetro SystemInformationClass* es **SystemRegistryQuotaInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una única estructura **SYSTEM REGISTRY QUOTA \_ \_ \_ INFORMATION** con el diseño siguiente:

``` syntax
typedef struct _SYSTEM_REGISTRY_QUOTA_INFORMATION {
    ULONG RegistryQuotaAllowed;
    ULONG RegistryQuotaUsed;
    PVOID Reserved1;
} SYSTEM_REGISTRY_QUOTA_INFORMATION;
```

El **miembro RegistryQuotaAllowed** contiene el tamaño máximo, en bytes, que el Registro puede alcanzar en este sistema.

El **miembro RegistryQuotaUsed** contiene el tamaño actual del Registro, en bytes.

Use [**GetSystemRegistryQuota en**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota) su lugar para recuperar esta información.

El otro miembro de la estructura está reservado para su uso interno por parte del sistema operativo.

</dd> <dt>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>

<span id="SYSTEM_LOOKASIDE_INFORMATION"></span><span id="system_lookaside_information"></span>**INFORMACIÓN \_ DE ASPECTO DEL \_ SISTEMA**


</dt> <dd>

Cuando el parámetro *SystemInformationClass* es **SystemLookasideInformation**, el búfer al que apunta el parámetro *SystemInformation* debe ser lo suficientemente grande como para contener una estructura **opaca SYSTEM \_ LOOKASIDE \_ INFORMATION** para su uso en la generación de un valor de ed. imprevisible para un generador de números aleatorios. Para ello, la estructura tiene el diseño siguiente:

``` syntax
typedef struct _SYSTEM_LOOKASIDE_INFORMATION {
    BYTE Reserved1[32];
} SYSTEM_LOOKASIDE_INFORMATION;
```

El sistema operativo reserva miembros individuales de la estructura para su uso interno.

Use la [**función CryptGenRandom en**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) su lugar para generar datos criptográficos aleatorios.

</dd> </dl> </dd> <dt>

*SystemInformationLength* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta el *parámetro SystemInformation,* en bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Puntero opcional a una ubicación donde la función escribe el tamaño real de la información solicitada. Si ese tamaño es menor o igual que el parámetro *SystemInformationLength,* la función copia la información en el *búfer SystemInformation;* de lo contrario, devuelve un código de error NTSTATUS y devuelve en *ReturnLength* el tamaño del búfer necesario para recibir la información solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código ntstatus correcto o de error.

Los formularios y la importancia de los códigos de error NTSTATUS se enumeran en el archivo de encabezado Ntstatus.h disponible en el DDK y se describen en la documentación de DDK.

## <a name="remarks"></a>Comentarios

La **función ZwQuerySystemInformation** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar las funciones alternativas mencionadas anteriormente en su lugar.

Si usa **ZwQuerySystemInformation**, acceda a la función a través de la vinculación [dinámica en tiempo de ejecución.](/windows/desktop/Dlls/using-run-time-dynamic-linking) Esto ofrece al código la oportunidad de responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios de firma no sean detectables.

Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Getsysteminfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)
</dt> <dt>

[**GetProcessHandleCount**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)
</dt> <dt>

[**GetProcessMemoryInfo**](/windows/desktop/api/psapi/nf-psapi-getprocessmemoryinfo)
</dt> <dt>

[**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)
</dt> <dt>

[**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)
</dt> </dl>

 


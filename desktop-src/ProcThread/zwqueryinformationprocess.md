---
description: Recupera información sobre el proceso especificado.
ms.assetid: c36c023f-7f9a-4ba5-a41f-f2f755a24eb6
title: Función ZwQueryInformationProcess
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
ms.openlocfilehash: 7972d3d2e6b98f56829680dd77c4c0a97b51679ffb2d9cfef928d4a279f6b7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792919"
---
# <a name="zwqueryinformationprocess-function"></a>Función ZwQueryInformationProcess

\[**ZwQueryInformationProcess** puede modificarse o no estar disponible en versiones futuras de Windows. Las aplicaciones deben usar las funciones alternativas enumeradas en este tema.\]

Recupera información sobre el proceso especificado.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ZwQueryInformationProcess(
  _In_      HANDLE           ProcessHandle,
  _In_      PROCESSINFOCLASS ProcessInformationClass,
  _Out_     PVOID            ProcessInformation,
  _In_      ULONG            ProcessInformationLength,
  _Out_opt_ PULONG           ReturnLength
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ProcessHandle* \[ En\]
</dt> <dd>

Identificador del proceso para el que se va a recuperar la información.

</dd> <dt>

*ProcessInformationClass* \[ En\]
</dt> <dd>

Tipo de información de proceso que se va a recuperar. Este parámetro puede ser uno de los siguientes valores de la **enumeración PROCESSINFOCLASS.**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ProcessBasicInformation"></span><span id="processbasicinformation"></span><span id="PROCESSBASICINFORMATION"></span><dl> <dt><strong>ProcessBasicInformation</strong></dt> <dt>0</dt> </dl></td>
<td>Recupera un puntero a una estructura PEB que se puede usar para determinar si se está depurando el proceso especificado y un valor único utilizado por el sistema para identificar el proceso especificado. <br/> Es mejor usar las <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>funciones CheckRemoteDebuggerPresent</strong></a> y <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>GetProcessId</strong></a> para obtener esta información.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>Recupera un valor <strong>DWORD_PTR</strong> que es el número de puerto del depurador para el proceso. Un valor distinto de cero indica que el proceso se ejecuta bajo el control de un depurador de anillo 3.<br/> Es mejor usar la <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>función CheckRemoteDebuggerPresent</strong></a> <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>o IsDebuggerPresent.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Determina si el proceso se ejecuta en el entorno WOW64 (WOW64 es el emulador x86 que permite que las aplicaciones basadas en Win32 se ejecuten en aplicaciones de 64 Windows).<br/> Es mejor usar la <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>función IsWow64Process</strong></a> para obtener esta información.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>Recupera un <strong>UNICODE_STRING</strong> que contiene el nombre del archivo de imagen para el proceso.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>Recupera un valor <strong>ULONG</strong> que indica si el proceso se considera crítico.<br/>
<blockquote>
[!Note]<br />
Este valor se puede usar a partir de Windows XP con SP3. A partir Windows 8.1, se debe usar <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>Recupera un valor BYTE que indica el tipo de proceso protegido y el firmante del proceso protegido.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*ProcessInformation* \[ out\]
</dt> <dd>

Puntero a un búfer proporcionado por la aplicación que realiza la llamada en el que la función escribe la información solicitada. El tamaño de la información escrita varía en función del valor del *parámetro ProcessInformationClass:*

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESAR \_ INFORMACIÓN \_ BÁSICA
</dt> <dd>

Cuando el *parámetro ProcessInformationClass* es **ProcessBasicInformation,** el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única estructura **PROCESS BASIC \_ \_ INFORMATION** con el diseño siguiente:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

El **miembro UniqueProcessId** apunta al identificador único del sistema para este proceso. Es mejor usar la función [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) para recuperar esta información.

El **miembro PebBaseAddress** apunta a una [**estructura PEB.**](/windows/desktop/api/Winternl/ns-winternl-peb)

Los demás miembros de esta estructura están reservados para su uso interno por parte del sistema operativo.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ PTR
</dt> <dd>

Cuando el *parámetro ProcessInformationClass* es **ProcessWow64Information**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener **un \_ PTR de ULONG.** Si este valor es distinto de cero, el proceso se ejecuta en un entorno WOW64; De lo contrario, si el valor es igual a cero, el proceso no se ejecuta en un entorno WOW64.

Es mejor usar la función [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) para determinar si un proceso se está ejecutando en el entorno WOW64.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>CADENA \_ UNICODE
</dt> <dd>

Cuando el *parámetro ProcessInformationClass* es **ProcessImageFileName**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una estructura **\_ STRING UNICODE,** así como la propia cadena. La cadena almacenada en el miembro **Buffer** es el nombre del archivo de imagen.

Si el búfer es demasiado pequeño, se produce un error en la función con el código de error STATUS INFO LENGTH MISMATCH y el \_ \_ parámetro \_ *ReturnLength* se establece en el tamaño de búfer necesario.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Cuando el *parámetro ProcessInformationClass* es **ProcessProtectionInformation,** el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única **estructura PS_PROTECTION** que tenga el diseño siguiente:

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

Los tres primeros bits contienen el tipo de proceso protegido:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Los 4 bits superiores contienen el firmante del proceso protegido:

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

*ProcessInformationLength* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta el *parámetro ProcessInformation,* en bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable en la que la función devuelve el tamaño de la información solicitada. Si la función se ha realizado correctamente, este es el tamaño de la información escrita en el búfer al que apunta el parámetro *ProcessInformation,* pero si el búfer era demasiado pequeño, este es el tamaño mínimo de búfer necesario para recibir la información correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código ntstatus correcto o de error.

Los formularios y la importancia de los códigos de error NTSTATUS se enumeran en el archivo de encabezado Ntstatus.h disponible en el DDK y se describen en la documentación de DDK en Kernel-Mode Driver Architecture /Design Guide /Driver Programming Techniques/Logging Errors.

## <a name="remarks"></a>Comentarios

La **función ZwQueryInformationProcess** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar las funciones públicas mencionadas en la descripción del *parámetro ProcessInformationClass* en su lugar.

Si usa **ZwQueryInformationProcess**, acceda a la función a través de la vinculación [dinámica en tiempo de ejecución.](../dlls/using-run-time-dynamic-linking.md) Esto ofrece al código la oportunidad de responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios de firma no sean detectables.

Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 

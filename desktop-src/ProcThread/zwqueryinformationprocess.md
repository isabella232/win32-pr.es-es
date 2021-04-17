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
# <a name="zwqueryinformationprocess-function"></a>ZwQueryInformationProcess función)

\[**ZwQueryInformationProcess** puede modificarse o no estar disponible en versiones futuras de Windows. Las aplicaciones deben usar las funciones alternativas que se enumeran en este tema.\]

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

*ProcessHandle* \[ de\]
</dt> <dd>

Identificador del proceso para el que se va a recuperar información.

</dd> <dt>

*ProcessInformationClass* \[ de\]
</dt> <dd>

Tipo de información de proceso que se va a recuperar. Este parámetro puede ser uno de los siguientes valores de la enumeración **PROCESSINFOCLASS** .



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
<td>Recupera un puntero a una estructura PEB que se puede usar para determinar si se está depurando el proceso especificado y un valor único que utiliza el sistema para identificar el proceso especificado. <br/> Es mejor usar las funciones <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> y <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessid"><strong>getprocessid (</strong></a> para obtener esta información.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessDebugPort"></span><span id="processdebugport"></span><span id="PROCESSDEBUGPORT"></span><dl> <dt><strong>ProcessDebugPort</strong></dt> <dt>7</dt> </dl></td>
<td>Recupera un valor de <strong>DWORD_PTR</strong> que es el número de puerto del depurador para el proceso. Un valor distinto de cero indica que el proceso se ejecuta bajo el control de un depurador de anillo 3.<br/> Es mejor usar la función <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent"><strong>CheckRemoteDebuggerPresent</strong></a> o <a href="/windows/desktop/api/debugapi/nf-debugapi-isdebuggerpresent"><strong>IsDebuggerPresent</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessWow64Information"></span><span id="processwow64information"></span><span id="PROCESSWOW64INFORMATION"></span><dl> <dt><strong>ProcessWow64Information</strong></dt> <dt>26</dt> </dl></td>
<td>Determina si el proceso se está ejecutando en el entorno WOW64 (WOW64 es el emulador x86 que permite que las aplicaciones basadas en Win32 se ejecuten en Windows de 64 bits).<br/> Es mejor usar la función <a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process"><strong>IsWow64Process</strong></a> para obtener esta información.<br/></td>
</tr>
<tr class="even">
<td><span id="ProcessImageFileName"></span><span id="processimagefilename"></span><span id="PROCESSIMAGEFILENAME"></span><dl> <dt><strong>ProcessImageFileName</strong></dt> <dt>27</dt> </dl></td>
<td>Recupera un valor de <strong>UNICODE_STRING</strong> que contiene el nombre del archivo de imagen para el proceso.<br/></td>
</tr>
<tr class="odd">
<td><span id="ProcessBreakOnTermination"></span><span id="processbreakontermination"></span><span id="PROCESSBREAKONTERMINATION"></span><dl> <dt><strong>ProcessBreakOnTermination</strong></dt> <dt>29</dt> </dl></td>
<td>Recupera un valor <strong>ULong</strong> que indica si el proceso se considera crítico.<br/>
<blockquote>
[!Note]<br />
Este valor se puede usar a partir de Windows XP con SP3. A partir de Windows 8.1, se debe usar <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-isprocesscritical"><strong>IsProcessCritical</strong></a> en su lugar.
</blockquote>
<br/></td>
</tr><tr class="even">
<td><span id="ProcessProtectionInformation"></span><span id="processprotectioninformation"></span><span id="PROCESSPROTECTIONINFORMATION"></span><dl> <dt><strong>ProcessProtectionInformation</strong></dt> <dt>61</dt> </dl></td>
<td>Recupera un valor de BYTE que indica el tipo de proceso protegido y el firmante del proceso protegido.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*ProcessInformation* \[ enuncia\]
</dt> <dd>

Puntero a un búfer proporcionado por la aplicación que realiza la llamada en la que la función escribe la información solicitada. El tamaño de la información escrita varía en función del valor del parámetro *ProcessInformationClass* :

<dl> <dt>

<span id="PROCESS_BASIC_INFORMATION"></span><span id="process_basic_information"></span>PROCESAR \_ \_ información básica
</dt> <dd>

Cuando el parámetro *ProcessInformationClass* es **ProcessBasicInformation**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única estructura de **\_ \_ información básica de proceso** con el siguiente diseño:

``` syntax
typedef struct _PROCESS_BASIC_INFORMATION {
    PVOID Reserved1;
    PPEB PebBaseAddress;
    PVOID Reserved2[2];
    ULONG_PTR UniqueProcessId;
    PVOID Reserved3;
} PROCESS_BASIC_INFORMATION;
```

El miembro **UniqueProcessId** apunta al identificador único del sistema para este proceso. Es mejor usar la función [**getprocessid (**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid) para recuperar esta información.

El miembro **PebBaseAddress** apunta a una estructura [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb) .

Los demás miembros de esta estructura se reservan para uso interno del sistema operativo.

</dd> <dt>

<span id="ULONG_PTR"></span><span id="ulong_ptr"></span>ULONG \_ ptr
</dt> <dd>

Cuando el parámetro *ProcessInformationClass* es **ProcessWow64Information**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener un **ULong \_ ptr**. Si este valor es distinto de cero, el proceso se ejecuta en un entorno WOW64; de lo contrario, si el valor es igual a cero, el proceso no se está ejecutando en un entorno WOW64.

Es mejor usar la función [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process) para determinar si un proceso se está ejecutando en el entorno WOW64.

</dd> <dt>

<span id="UNICODE_STRING"></span><span id="unicode_string"></span>cadena Unicode \_
</dt> <dd>

Cuando el parámetro *ProcessInformationClass* es **ProcessImageFileName**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una estructura de **\_ cadena Unicode** , así como la propia cadena. La cadena almacenada en el miembro del **búfer** es el nombre del archivo de imagen.

Si el búfer es demasiado pequeño, se produce un error en la función con el código de error de coincidencia de longitud de información de estado \_ \_ \_ y el parámetro *ReturnLength* se establece en el tamaño de búfer necesario.

</dd> <dt>

<span id="PS_PROTECTION"></span><span id="ps_protection"></span>PS_PROTECTION
</dt> <dd>

Cuando el parámetro *ProcessInformationClass* es **ProcessProtectionInformation**, el búfer al que apunta el parámetro *ProcessInformation* debe ser lo suficientemente grande como para contener una única estructura de **PS_PROTECTION** que tenga el siguiente diseño:

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

Los primeros 3 bits contienen el tipo de proceso protegido:

``` syntax
typedef enum _PS_PROTECTED_TYPE {
    PsProtectedTypeNone = 0,
    PsProtectedTypeProtectedLight = 1,
    PsProtectedTypeProtected = 2
} PS_PROTECTED_TYPE, *PPS_PROTECTED_TYPE;
```

Los 4 bits principales contienen el firmante del proceso protegido:

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

*ProcessInformationLength* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta el parámetro *ProcessInformation* , en bytes.

</dd> <dt>

*ReturnLength* \[ out, opcional\]
</dt> <dd>

Puntero a una variable en la que la función devuelve el tamaño de la información solicitada. Si la función se realizó correctamente, es el tamaño de la información escrita en el búfer al que apunta el parámetro *ProcessInformation* , pero si el búfer es demasiado pequeño, es el tamaño mínimo del búfer necesario para recibir la información correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de error o correcto de NTSTATUS.

Los formularios y la importancia de los códigos de error de NTSTATUS se enumeran en el archivo de encabezado NTSTATUS. h disponible en el DDK y se describen en la documentación de DDK en Kernel-Mode guía de arquitectura/diseño de controladores/guías de programación de controladores/errores de registro.

## <a name="remarks"></a>Observaciones

La función **ZwQueryInformationProcess** y las estructuras que devuelve son internas del sistema operativo y están sujetas a cambios de una versión de Windows a otra. Para mantener la compatibilidad de la aplicación, es mejor usar las funciones públicas que se mencionan en la descripción del parámetro *ProcessInformationClass* en su lugar.

Si usa **ZwQueryInformationProcess**, acceda a la función a través [de la vinculación dinámica en tiempo de ejecución](../dlls/using-run-time-dynamic-linking.md). Esto proporciona al código una oportunidad para responder correctamente si la función se ha cambiado o quitado del sistema operativo. Sin embargo, es posible que los cambios en la firma no se puedan detectar.

Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)
</dt> <dt>

[**Getprocessid (**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)
</dt> <dt>

[**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
</dt> <dt>

[**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)
</dt> </dl>

 

 

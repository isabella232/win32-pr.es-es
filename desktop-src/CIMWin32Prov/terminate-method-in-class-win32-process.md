---
description: El&\# 32; El método de clase WMI finaliza un proceso y todos sus subprocesos.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Método Terminate de la Win32_Process clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f0b9671891b9f9c90e8a36e3fc0b58e92a513935d2923e3a2eed5134dcef777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009361"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Método Terminate de la clase Process de Win32 \_

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Terminate** finaliza un proceso y todos sus subprocesos.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Motivo* \[ En\]
</dt> <dd>

Código de salida para el proceso y para todos los subprocesos finalizados como resultado de esta llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el proceso se finalizó correctamente y cualquier otro número para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**Ruta de acceso no encontrada** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otros** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

**Información general**

Los problemas del equipo suelen deberse a un proceso que ya no funciona según lo previsto. Por ejemplo, el proceso podría estar filtrando memoria o podría haber dejado de responder a la entrada del usuario. Cuando se producen problemas como estos, se debe finalizar el proceso. Aunque esto puede parecer una tarea lo suficientemente sencilla, la finalización de un proceso puede ser complicada por varios factores:

-   El proceso podría estar cerrado y, por tanto, ya no responde a los comandos de menú o teclado para cerrar la aplicación. Esto hace todo menos imposible para el usuario típico descartar la aplicación y finalizar el proceso.
-   El proceso podría estar huérfano. Por ejemplo, un script podría crear una instancia de Word y, a continuación, salir sin destruir esa instancia. En efecto, Word sigue ejecutándose en el equipo, aunque no haya ninguna interfaz de usuario visible. Dado que no hay ninguna interfaz de usuario, no hay ningún comando de menú o teclado disponible para finalizar el proceso.
-   Es posible que no sepa qué proceso debe finalizar. Por ejemplo, puede que desee finalizar todos los programas que superen una cantidad de memoria especificada.
-   Dado Administrador de tareas permite finalizar solo los procesos que creó, es posible que no pueda finalizar un proceso, incluso si es administrador en el equipo.

Los scripts le permiten superar todos estos posibles obstáculos, lo que le proporciona un control administrativo considerable sobre los equipos. Por ejemplo, si sospecha que los usuarios están haciendo juegos prohibidos en su organización, puede escribir fácilmente un script para conectarse a cada equipo, identificar si el juego se está ejecutando y finalizar inmediatamente el proceso.

**Usar el método Terminate**

Puede finalizar un proceso mediante:

-   Terminación de un proceso que se está ejecutando actualmente. Por ejemplo, es posible que tenga que finalizar un programa de diagnóstico que se ejecuta en un equipo remoto. Si no hay ninguna manera de controlar la aplicación de forma remota, simplemente puede finalizar el proceso de esa aplicación.
-   Impedir que un proceso se ejecute en primer lugar. Al supervisar continuamente la creación de procesos en un equipo, puede identificar y finalizar al instante cualquier proceso en cuanto se inicie. Esto proporciona un método para garantizar que determinadas aplicaciones (como los programas que descargan archivos multimedia grandes a través de Internet) nunca se ejecuten en determinados equipos.

> [!Note]  
> directiva de grupo también se puede usar para restringir los programas que se ejecutan en un equipo. Sin embargo, directiva de grupo puede restringir solo los programas que se ejecutan mediante menú Inicio o Windows Explorer; no tiene ningún efecto en los programas que empezaron a usar otros medios, como la línea de comandos. Por el contrario, WMI puede impedir que un proceso se ejecute independientemente de cómo se inició el proceso.

 

**Terminación de un proceso que no es de su propiedad**

Para finalizar un proceso que no es de su propiedad, habilite el **privilegio SeDebugPrivilege.** En VBScript, puede habilitar este privilegio con las siguientes líneas de código:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Para obtener más información sobre cómo habilitar este privilegio en C++, vea Habilitar y deshabilitar [privilegios en C++.](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)

## <a name="examples"></a>Ejemplos

El ejemplo de código de PowerShell Terminate [running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) on TechNet Gallery (Finalizar el proceso en ejecución en varios servidores en la Galería de TechNet) finaliza un proceso que se ejecuta en uno o varios equipos.

El siguiente ejemplo de VBScript finaliza el proceso en el que la aplicación Diagnose.exe está ejecutando actualmente.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



En el ejemplo de VBScript siguiente se usa un consumidor de eventos temporal para finalizar un proceso en cuanto se inicia.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



En el ejemplo de código de VBScript siguiente se conecta a un equipo remoto y Notepad.exe en ese equipo.


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



El siguiente código de C++ finaliza el Notepad.exe en el equipo local. Especifique un identificador de proceso o (identificador de proceso) en el código para finalizar el proceso. Este valor se puede encontrar en la propiedad handle de la clase Process de [**Win32 \_**](win32-process.md) (la propiedad clave de la clase). Al especificar un valor para la propiedad Handle, se proporciona una ruta de acceso a la instancia de la clase que desea finalizar. Para obtener más información sobre cómo conectarse a un equipo remoto, vea Ejemplo: Obtener datos [WMI de un equipo remoto.](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer)


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Proceso \_ win32**](win32-process.md)
</dt> <dt>

[Tareas wmi: supervisión del rendimiento](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Tareas wmi: procesos](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 


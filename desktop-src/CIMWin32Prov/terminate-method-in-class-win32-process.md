---
description: La terminación&\# 32; El método de clase WMI finaliza un proceso y todos los subprocesos.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Método Terminate de la clase Win32_Process
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
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998187"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Método Terminate de la \_ clase Process de Win32

El método **Finalizar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) finaliza un proceso y todos sus subprocesos.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Motivo* \[ de\]
</dt> <dd>

Código de salida para el proceso y para todos los subprocesos finalizados como resultado de esta llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el proceso se ha terminado correctamente y cualquier otro número para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Finalización correcta** (0)
</dt> <dt>

**Acceso denegado** (2)
</dt> <dt>

**Privilegios insuficientes** (3)
</dt> <dt>

**Error desconocido** (8)
</dt> <dt>

**No se encontró la ruta de acceso** (9)
</dt> <dt>

**Parámetro no válido** (21)
</dt> <dt>

**Otro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

**Información general**

Los problemas del equipo suelen deberse a un proceso que ya no funciona según lo esperado. Por ejemplo, el proceso podría estar perdiendo memoria o podría haber dejado de responder a los datos proporcionados por el usuario. Cuando se producen problemas como estos, el proceso debe terminarse. Aunque esto puede parecer una tarea bastante sencilla, la terminación de un proceso puede ser complicada en varios factores:

-   El proceso podría estar bloqueado y, por lo tanto, ya no responde a los comandos de menú o teclado para cerrar la aplicación. Esto hace que sea todo lo posible para el usuario típico descartar la aplicación y finalizar el proceso.
-   Es posible que el proceso esté huérfano. Por ejemplo, un script puede crear una instancia de Word y después salir sin destruir esa instancia. En efecto, Word permanece en ejecución en el equipo, aunque no esté visible ninguna interfaz de usuario. Dado que no hay ninguna interfaz de usuario, no hay ningún comando de menú o de teclado disponible para finalizar el proceso.
-   Es posible que no sepa qué proceso debe terminar. Por ejemplo, puede que desee finalizar todos los programas que superen una cantidad especificada de memoria.
-   Dado que el administrador de tareas permite finalizar solo los procesos que ha creado, es posible que no pueda finalizar un proceso, incluso si es un administrador del equipo.

Los scripts le permiten superar todos estos posibles obstáculos, lo que le proporciona un control administrativo considerable sobre los equipos. Por ejemplo, si sospecha que los usuarios están jugando a juegos prohibidos en su organización, puede escribir fácilmente un script para conectarse a cada equipo, identificar si el juego se está ejecutando y finalizar inmediatamente el proceso.

**Usar el método Terminate**

Para finalizar un proceso, puede:

-   Finalizar un proceso que se está ejecutando actualmente. Por ejemplo, puede que necesite terminar un programa de diagnóstico que se ejecuta en un equipo remoto. Si no hay ninguna manera de controlar la aplicación de forma remota, puede terminar simplemente el proceso de esa aplicación.
-   Impedir que un proceso se ejecute en primer lugar. Al supervisar continuamente la creación de procesos en un equipo, puede identificar y finalizar de forma instantánea cualquier proceso en cuanto se inicie. Esto proporciona un método para garantizar que determinadas aplicaciones (como los programas que descargan archivos multimedia de gran tamaño a través de Internet) nunca se ejecutan en ciertos equipos.

> [!Note]  
> Directiva de grupo también puede usarse para restringir los programas que se ejecutan en un equipo. Sin embargo, directiva de grupo solo pueden restringir los programas que se ejecutan mediante el menú Inicio o el explorador de Windows; no tiene ningún efecto en los programas iniciados mediante otros medios, como la línea de comandos. Por el contrario, WMI puede impedir que un proceso se ejecute con independencia de cómo se inicie el proceso.

 

**Finalizar un proceso que no es de su propiedad**

Para finalizar un proceso que no es de su propiedad, habilite el privilegio **SeDebugPrivilege** . En VBScript, puede habilitar este privilegio con las siguientes líneas de código:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Para obtener más información sobre cómo habilitar este privilegio en C++, vea [habilitar y deshabilitar privilegios en c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de PowerShell [terminar en ejecución en varios servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) de la galería de TechNet finaliza un proceso que se ejecuta en uno o varios equipos.

En el siguiente ejemplo de VBScript se finaliza el proceso en el que la aplicación Diagnose.exe se está ejecutando actualmente.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



El siguiente ejemplo de VBScript utiliza un consumidor de eventos temporal para finalizar un proceso en cuanto se inicia.


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



El siguiente ejemplo de código de VBScript se conecta a un equipo remoto y finaliza Notepad.exe en ese equipo.


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



El siguiente código de C++ finaliza el proceso de Notepad.exe en el equipo local. Especifique un identificador de proceso o (identificador de proceso) en el código para finalizar el proceso. Este valor puede encontrarse en la propiedad Handle de la clase de [**\_ proceso Win32**](win32-process.md) (la propiedad clave de la clase). Al especificar un valor para la propiedad Handle, se proporciona una ruta de acceso a la instancia de la clase que desea finalizar. Para obtener más información acerca de cómo conectarse a un equipo remoto, vea [ejemplo: obtener datos WMI desde un equipo remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Proceso Win32**](win32-process.md)
</dt> <dt>

[Tareas WMI: supervisión del rendimiento](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Tareas de WMI: procesos](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 


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
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="d30e4-103">Método Terminate de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="d30e4-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="d30e4-104">El método **Finalizar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) finaliza un proceso y todos sus subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d30e4-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="d30e4-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d30e4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d30e4-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d30e4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d30e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d30e4-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="d30e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d30e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d30e4-109">*Motivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d30e4-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d30e4-110">Código de salida para el proceso y para todos los subprocesos finalizados como resultado de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="d30e4-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d30e4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d30e4-111">Return value</span></span>

<span data-ttu-id="d30e4-112">Devuelve un valor de 0 (cero) si el proceso se ha terminado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="d30e4-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="d30e4-113">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d30e4-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d30e4-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d30e4-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d30e4-115">**Finalización correcta** (0)</span><span class="sxs-lookup"><span data-stu-id="d30e4-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-116">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="d30e4-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-117">**Privilegios insuficientes** (3)</span><span class="sxs-lookup"><span data-stu-id="d30e4-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-118">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="d30e4-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-119">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="d30e4-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-120">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="d30e4-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="d30e4-121">**Otro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="d30e4-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d30e4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d30e4-122">Remarks</span></span>

<span data-ttu-id="d30e4-123">**Información general**</span><span class="sxs-lookup"><span data-stu-id="d30e4-123">**Overview**</span></span>

<span data-ttu-id="d30e4-124">Los problemas del equipo suelen deberse a un proceso que ya no funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="d30e4-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="d30e4-125">Por ejemplo, el proceso podría estar perdiendo memoria o podría haber dejado de responder a los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e4-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="d30e4-126">Cuando se producen problemas como estos, el proceso debe terminarse.</span><span class="sxs-lookup"><span data-stu-id="d30e4-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="d30e4-127">Aunque esto puede parecer una tarea bastante sencilla, la terminación de un proceso puede ser complicada en varios factores:</span><span class="sxs-lookup"><span data-stu-id="d30e4-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="d30e4-128">El proceso podría estar bloqueado y, por lo tanto, ya no responde a los comandos de menú o teclado para cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d30e4-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="d30e4-129">Esto hace que sea todo lo posible para el usuario típico descartar la aplicación y finalizar el proceso.</span><span class="sxs-lookup"><span data-stu-id="d30e4-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="d30e4-130">Es posible que el proceso esté huérfano.</span><span class="sxs-lookup"><span data-stu-id="d30e4-130">The process might be orphaned.</span></span> <span data-ttu-id="d30e4-131">Por ejemplo, un script puede crear una instancia de Word y después salir sin destruir esa instancia.</span><span class="sxs-lookup"><span data-stu-id="d30e4-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="d30e4-132">En efecto, Word permanece en ejecución en el equipo, aunque no esté visible ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e4-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="d30e4-133">Dado que no hay ninguna interfaz de usuario, no hay ningún comando de menú o de teclado disponible para finalizar el proceso.</span><span class="sxs-lookup"><span data-stu-id="d30e4-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="d30e4-134">Es posible que no sepa qué proceso debe terminar.</span><span class="sxs-lookup"><span data-stu-id="d30e4-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="d30e4-135">Por ejemplo, puede que desee finalizar todos los programas que superen una cantidad especificada de memoria.</span><span class="sxs-lookup"><span data-stu-id="d30e4-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="d30e4-136">Dado que el administrador de tareas permite finalizar solo los procesos que ha creado, es posible que no pueda finalizar un proceso, incluso si es un administrador del equipo.</span><span class="sxs-lookup"><span data-stu-id="d30e4-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="d30e4-137">Los scripts le permiten superar todos estos posibles obstáculos, lo que le proporciona un control administrativo considerable sobre los equipos.</span><span class="sxs-lookup"><span data-stu-id="d30e4-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="d30e4-138">Por ejemplo, si sospecha que los usuarios están jugando a juegos prohibidos en su organización, puede escribir fácilmente un script para conectarse a cada equipo, identificar si el juego se está ejecutando y finalizar inmediatamente el proceso.</span><span class="sxs-lookup"><span data-stu-id="d30e4-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="d30e4-139">**Usar el método Terminate**</span><span class="sxs-lookup"><span data-stu-id="d30e4-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="d30e4-140">Para finalizar un proceso, puede:</span><span class="sxs-lookup"><span data-stu-id="d30e4-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="d30e4-141">Finalizar un proceso que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d30e4-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="d30e4-142">Por ejemplo, puede que necesite terminar un programa de diagnóstico que se ejecuta en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="d30e4-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="d30e4-143">Si no hay ninguna manera de controlar la aplicación de forma remota, puede terminar simplemente el proceso de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="d30e4-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="d30e4-144">Impedir que un proceso se ejecute en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="d30e4-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="d30e4-145">Al supervisar continuamente la creación de procesos en un equipo, puede identificar y finalizar de forma instantánea cualquier proceso en cuanto se inicie.</span><span class="sxs-lookup"><span data-stu-id="d30e4-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="d30e4-146">Esto proporciona un método para garantizar que determinadas aplicaciones (como los programas que descargan archivos multimedia de gran tamaño a través de Internet) nunca se ejecutan en ciertos equipos.</span><span class="sxs-lookup"><span data-stu-id="d30e4-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="d30e4-147">Directiva de grupo también puede usarse para restringir los programas que se ejecutan en un equipo.</span><span class="sxs-lookup"><span data-stu-id="d30e4-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="d30e4-148">Sin embargo, directiva de grupo solo pueden restringir los programas que se ejecutan mediante el menú Inicio o el explorador de Windows; no tiene ningún efecto en los programas iniciados mediante otros medios, como la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d30e4-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="d30e4-149">Por el contrario, WMI puede impedir que un proceso se ejecute con independencia de cómo se inicie el proceso.</span><span class="sxs-lookup"><span data-stu-id="d30e4-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="d30e4-150">**Finalizar un proceso que no es de su propiedad**</span><span class="sxs-lookup"><span data-stu-id="d30e4-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="d30e4-151">Para finalizar un proceso que no es de su propiedad, habilite el privilegio **SeDebugPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d30e4-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="d30e4-152">En VBScript, puede habilitar este privilegio con las siguientes líneas de código:</span><span class="sxs-lookup"><span data-stu-id="d30e4-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="d30e4-153">Para obtener más información sobre cómo habilitar este privilegio en C++, vea [habilitar y deshabilitar privilegios en c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="d30e4-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="d30e4-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d30e4-154">Examples</span></span>

<span data-ttu-id="d30e4-155">En el ejemplo de código de PowerShell [terminar en ejecución en varios servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) de la galería de TechNet finaliza un proceso que se ejecuta en uno o varios equipos.</span><span class="sxs-lookup"><span data-stu-id="d30e4-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="d30e4-156">En el siguiente ejemplo de VBScript se finaliza el proceso en el que la aplicación Diagnose.exe se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="d30e4-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="d30e4-157">El siguiente ejemplo de VBScript utiliza un consumidor de eventos temporal para finalizar un proceso en cuanto se inicia.</span><span class="sxs-lookup"><span data-stu-id="d30e4-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


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



<span data-ttu-id="d30e4-158">El siguiente ejemplo de código de VBScript se conecta a un equipo remoto y finaliza Notepad.exe en ese equipo.</span><span class="sxs-lookup"><span data-stu-id="d30e4-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


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



<span data-ttu-id="d30e4-159">El siguiente código de C++ finaliza el proceso de Notepad.exe en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d30e4-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="d30e4-160">Especifique un identificador de proceso o (identificador de proceso) en el código para finalizar el proceso.</span><span class="sxs-lookup"><span data-stu-id="d30e4-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="d30e4-161">Este valor puede encontrarse en la propiedad Handle de la clase de [**\_ proceso Win32**](win32-process.md) (la propiedad clave de la clase).</span><span class="sxs-lookup"><span data-stu-id="d30e4-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="d30e4-162">Al especificar un valor para la propiedad Handle, se proporciona una ruta de acceso a la instancia de la clase que desea finalizar.</span><span class="sxs-lookup"><span data-stu-id="d30e4-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="d30e4-163">Para obtener más información acerca de cómo conectarse a un equipo remoto, vea [ejemplo: obtener datos WMI desde un equipo remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="d30e4-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d30e4-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d30e4-164">Requirements</span></span>



| <span data-ttu-id="d30e4-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="d30e4-165">Requirement</span></span> | <span data-ttu-id="d30e4-166">Value</span><span class="sxs-lookup"><span data-stu-id="d30e4-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d30e4-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d30e4-167">Minimum supported client</span></span><br/> | <span data-ttu-id="d30e4-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d30e4-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d30e4-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d30e4-169">Minimum supported server</span></span><br/> | <span data-ttu-id="d30e4-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d30e4-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d30e4-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d30e4-171">Namespace</span></span><br/>                | <span data-ttu-id="d30e4-172">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d30e4-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d30e4-173">MOF</span><span class="sxs-lookup"><span data-stu-id="d30e4-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d30e4-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d30e4-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d30e4-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d30e4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d30e4-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d30e4-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d30e4-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="d30e4-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="d30e4-178">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d30e4-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d30e4-179">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="d30e4-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="d30e4-180">Tareas WMI: supervisión del rendimiento</span><span class="sxs-lookup"><span data-stu-id="d30e4-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="d30e4-181">Tareas de WMI: procesos</span><span class="sxs-lookup"><span data-stu-id="d30e4-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 


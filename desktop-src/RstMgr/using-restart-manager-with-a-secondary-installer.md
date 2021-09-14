---
title: Usar el Administrador de reinicio con un instalador secundario
description: En el procedimiento siguiente se describe el uso del Administrador de reinicio con instaladores principales y secundarios.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb44105d9f3d391bb2ed793aca8a6da2c330b30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169002"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a>Usar el Administrador de reinicio con un instalador secundario

En el procedimiento siguiente se describe el uso del Administrador de reinicio con instaladores principales y secundarios.

Cuando se usan instaladores principales y secundarios, el instalador principal controla la interfaz de usuario.

**Para usar el Administrador de reinicio con instaladores principales y secundarios**

1.  El instalador principal llama a la [**función RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) para iniciar la sesión del Administrador de reinicio y obtener un identificador de sesión y una clave.
2.  El instalador principal inicia o se pone en contacto con el instalador secundario y le proporciona la clave de sesión obtenida en el paso anterior.
3.  El instalador secundario llama a la [**función RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) con la clave de sesión para unirse a la sesión de Restart Manager. Un instalador secundario puede unirse a una sesión iniciada por el instalador principal solo cuando ambos instaladores se ejecutan en el mismo contexto de usuario.
4.  Los instaladores principal y secundario llaman a [**la función RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) para registrar los recursos. El Administrador de reinicio solo puede usar recursos registrados para determinar qué aplicaciones y servicios deben apagarse y reiniciarse. Todos los recursos que pueden verse afectados por la instalación deben registrarse con la sesión. Los recursos se pueden identificar por nombre de archivo, nombre corto del servicio o una [**estructura \_ RM UNIQUE \_ PROCESS.**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process)
5.  El instalador principal llama a la [**función RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) para obtener una matriz de estructuras [**DE RM PROCESS \_ \_ INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) que enumera todas las aplicaciones y servicios que se deben apagar y reiniciar.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es distinto de cero, el Administrador de reinicio no puede liberar un recurso registrado al apagar una aplicación o un servicio. En este caso, se requiere un apagado y reinicio del sistema para continuar con la instalación. El instalador principal debe solicitar al usuario una acción, detener programas o servicios, o programar un apagado y reinicio del sistema.

    Si el valor del parámetro *lpdwRebootReason* devuelto por la función [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) es cero, el instalador debe llamar a la [**función RmShutdown.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) Esto cierra los servicios y las aplicaciones que usan recursos registrados. A continuación, los instaladores principales y secundarios deben realizar las modificaciones del sistema necesarias para completar la instalación. Por último, el instalador principal debe llamar a la función [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) para que el Administrador de reinicio pueda reiniciar las aplicaciones que ha apagado y que se han registrado para un reinicio.

6.  El instalador principal y secundario llaman a [**la función RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) para cerrar la sesión de Restart Manager.

El fragmento de código siguiente muestra un ejemplo de un instalador principal que inicia y usa una sesión de Restart Manager. El ejemplo requiere Windows 7 o Windows Server 2008 R2. En Windows Vista o Windows Server 2008, la aplicación Calculadora se cierra pero no se reinicia. En este ejemplo se muestra cómo un instalador principal puede usar el Administrador de reinicio para apagar y reiniciar un proceso. En el ejemplo se da por supuesto que la calculadora ya se está ejecutando antes de iniciar la sesión del Administrador de reinicio.


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the  
    // Text-Encoded session key,defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of calc files to be registered.
    DWORD dwFiles           = 2;   

    //
    // NOTE:We register two calc executable files. 
    // The second one is for the redirection of 32 bit calc on 
    // 64 bit machines. Even if you are using a 32 bit machine,  
    // you don't need to comment out the second line. 
    //
    LPCWSTR rgsFiles[]      = 
     {L"C:\\Windows\\System32\\calc.exe",
      L"C:\\Windows\\SysWow64\\calc.exe"};

    UINT nRetry             = 0; 
    UINT nAffectedApps      = 0;
    UINT nProcInfoNeeded    = 0;
    RM_REBOOT_REASON dwRebootReasons    = RmRebootReasonNone;
    RM_PROCESS_INFO *rgAffectedApps     = NULL;
    
    //
    // Start a Restart Manager Session
    //
    dwErrCode = RmStartSession(&dwSessionHandle, 0, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: we only register two calc executable files 
    // in this sample. You can register files, processes 
    // (in the form of process ID), and services (in the   
    // form of service short names) with Restart Manager.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,       // Files
                                    0,  
                                    NULL,           // Processes
                                    0, 
                                    NULL);          // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Obtain the list of affected applications/services.
    //
    // NOTE: Restart Manager returns the results into the  
    // buffer allocated by the caller. The first call to 
    // RmGetList() will return the size of the buffer  
    // (i.e. nProcInfoNeeded) the caller needs to allocate. 
    // The caller then needs to allocate the buffer  
    // (i.e. rgAffectedApps) and make another RmGetList() 
    // call to ask Restart Manager to write the results 
    // into the buffer. However, since Restart Manager 
    // refreshes the list every time RmGetList()is called, 
    // it is possible that the size returned by the first 
    // RmGetList()call is not sufficient to hold the results  
    // discovered by the second RmGetList() call. Therefore, 
    // it is recommended that the caller follows the 
    // following practice to handle this race condition:
    //   
    //    Use a loop to call RmGetList() in case the buffer 
    //    allocated according to the size returned in previous 
    //    call is not enough.      
    // 
    // In this example, we use a do-while loop trying to make 
    // 3 RmGetList() calls (including the first attempt to get 
    // buffer size) and if we still cannot succeed, we give up. 
    //
    do
    {
        dwErrCode = RmGetList(dwSessionHandle,
                              &nProcInfoNeeded,
                              &nAffectedApps, 
                              rgAffectedApps, 
                              (LPDWORD) &dwRebootReasons);
        if (ERROR_SUCCESS == dwErrCode)
        {
            //
            // RmGetList() succeeded
            //
            break;
        }

        if (ERROR_MORE_DATA != dwErrCode)
        {
            //
            // RmGetList() failed, with errors 
            // other than ERROR_MORE_DATA
            //
            goto RM_CLEANUP;
        }

        //
        // RmGetList() is asking for more data
        //
        nAffectedApps = nProcInfoNeeded;
        
        if (NULL != rgAffectedApps)
        {
            delete []rgAffectedApps;
            rgAffectedApps = NULL;
        }

        rgAffectedApps = new RM_PROCESS_INFO[nAffectedApps];
    } while ((ERROR_MORE_DATA == dwErrCode) && (nRetry ++ < 3));

    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    if (RmRebootReasonNone != dwRebootReasons)
    {
        //
        // Restart Manager cannot mitigate a reboot. 
        // We goes to the clean up. The caller may want   
        // to add additional code to handle this scenario.
        //
        goto RM_CLEANUP;
    }
    
    //
    // Now rgAffectedApps contains the affected applications 
    // and services. The number of applications and services
    // returned is nAffectedApps. The result of RmGetList can 
    // be interpreted by the user to determine subsequent  
    // action (e.g. ask user's permission to shutdown).
    //
    // CALLER CODE GOES HERE...
     
    //
    // Shut down all running instances of affected 
    // applications and services.
    //
    dwErrCode = RmShutdown(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // An installer can now replace or update
    // the calc executable file.
    //
    // CALLER CODE GOES HERE...


    //
    // Restart applications and services, after the 
    // files have been replaced or updated.
    //
    dwErrCode = RmRestart(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:
    
    if (NULL != rgAffectedApps)
    {
        delete [] rgAffectedApps;
        rgAffectedApps = NULL;
    }

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // Clean up the Restart Manager session.
        //
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}
```



El fragmento de código siguiente muestra un ejemplo de cómo unir un instalador secundario a la sesión existente de Restart Manager. El ejemplo requiere Windows Vista o Windows Server 2008. El instalador secundario obtiene la clave de sesión del instalador principal y la usa para unirse a la sesión.


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the 
    // Text-Encoded session key, defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of files to be registered.
    DWORD dwFiles           = 1;   
    //
    // We register oleaut32.dll with Restart Manager.
    //
    LPCWSTR rgsFiles[]      = 
        {L"C:\\Windows\\System32\\oleaut32.dll"};

    //    
    // Secondary installer needs to obtain the session key from  
    // the primary installer and uses it to join the session.
    //
    // CALLER CODE GOES HERE ...
    //

    // We assume the session key obtained is stored in sessKey
    dwErrCode = RmJoinSession(&dwSessionHandle, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: In Vista, the subordinate is only allowed to 
    // register resources and cannot perform any other 
    // getlist, shutdown, restart or filter operations.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,     // Files
                                    0,  
                                    NULL,         // Processes
                                    0, 
                                    NULL);        // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // The subordinate leaves the conductor's session 
        // by calling RmEndSession(). The session itself 
        // won't be destroyed until the primary installer 
        // calls RmEndSession()
        //          
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}

```



 

 





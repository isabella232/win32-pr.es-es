---
title: Registrando el reinicio de la aplicación
description: Para registrar la aplicación para que se reinicie, llame a la función RegisterApplicationRestart.
ms.assetid: 4dfbced7-77db-4042-823f-b4b81b2b27a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 717f8984f26570284a70b40eef70a9d6f753d66a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271355"
---
# <a name="registering-for-application-restart"></a>Registrando el reinicio de la aplicación

Para registrar la aplicación para que se reinicie, llame a la función [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) . [Informe de errores de Windows (WER)](/windows/desktop/wer/windows-error-reporting) reiniciará la aplicación si se ha estado ejecutando durante al menos 60 segundos antes de dejar de responder o encontrar una excepción no controlada.

También debe considerar la posibilidad [de registrarse para la recuperación](registering-for-application-recovery.md), lo que le permite guardar datos e información de estado que puede resultar útil cuando wer reinicie la aplicación. WER reiniciará la aplicación después de que se complete el proceso de recuperación, si también se registra para la recuperación.

Una vez finalizado el proceso de recuperación, WER finaliza la aplicación y, a continuación, la reinicia. En el caso de las aplicaciones de consola, la aplicación se inicia en una ventana de consola independiente que se cierra cuando se cierra la aplicación.

**Nota para los autores de instalador de aplicaciones:** El registro para el reinicio de la aplicación también hará que Windows reinicie automáticamente la aplicación después de reiniciar el equipo en los casos en los que el equipo se reinicie debido a una actualización de software. Para que esto funcione, el instalador de la aplicación debe llamar a la función [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con el \_ conjunto de marcas EWX RESTARTAPPS o la función [**INITIATESHUTDOWN**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con la \_ marca Shutdown RESTARTAPPS establecida.

En el ejemplo siguiente se muestra cómo registrar para que WER reinicie la aplicación. En el ejemplo se produce una infracción de acceso después del registro para el reinicio de la aplicación. Informe de errores de Windows recogerá la infracción de acceso y mostrará la experiencia del usuario de informes de errores, incluido el reinicio de la aplicación. Debe ejecutarse desde una ventana de consola sin argumentos de línea de comandos.


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#define RESTART_SWITCH L"/restart"

void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId); 
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId); 
BOOL WINAPI CtrlHandler(DWORD dwControlType);
DWORD WINAPI Recover(PVOID pContext);

// A simple example to show how to use application recovery. For simplicity,
// the state information (record ID) is passed as part of the command line. 
void wmain(int argc, wchar_t* argv[])
{
    HRESULT hr = S_OK;
    DWORD dwRecordId = 0;
    BOOL fIsRestart = FALSE;

    GetRestartInfo(argc, argv, &fIsRestart, &dwRecordId);

    if (FAILED(hr = InitApplication(fIsRestart, &dwRecordId)))
    {
        wprintf(L"Failed to initialize the application.\n");
        goto cleanup;
    }

    // Do work. If you have a lot of state information, you should
    // periodically persist the state information to save time
    // in the recovery process.

    // The application must exist for at least 60 seconds for the
    // application to be restarted. Use Sleep() to mimic 60 seconds
    // worth of work.
    wprintf(L"Sleeping...\n");
    Sleep(62 * 1000);

    // Set the record ID to verify restart value.
    dwRecordId = 10;

    // Generate an access violation to force a restart. If we've already
    // restarted just exit because the example already demonstrated
    // the restart feature.
    if (FALSE == fIsRestart)
    {
        wprintf(L"Causing access violation...\n");
        int* p = NULL;
        *p = 5;
    }

cleanup:

    wprintf(L"Exiting...\n");
}


// Get the restart info from the command line. The command line is 
// of the form, /restart -r <RecordId>. The application 
// is being restarted if the first argument is /restart.
void GetRestartInfo(int argc, wchar_t* argv[], BOOL* pfIsRestart, DWORD* pdwRecordId) 
{
    if (argc > 1)
    {
        if (!wcsncmp(RESTART_SWITCH, argv[1], sizeof(RESTART_SWITCH)))
        {
            *pfIsRestart = TRUE;
            *pdwRecordId = _wtoi(argv[3]);
        }
    }

}

// Initialize the application. If this is a restart, use the state 
// information to reset the state of the application. This example 
// does not fail the initialization process if the process of 
// registering for application recovery and restart failed.
DWORD InitApplication(BOOL fIsRestart, DWORD* pdwRecordId)
{
    DWORD status = ERROR_SUCCESS;  // Set only if the initializing the application fails,
    HRESULT hr = S_OK;             // not if registering for recovery and restart fails.
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering InitApplication...\n");

    if (fIsRestart)
    {
        // TODO: Use the record ID to initialize the application.
        wprintf(L"Restart record ID is %lu\n", *pdwRecordId);
    }
    else
    {
        // This is not a restart, so initialize the application accordingly.
    }

    // Register for restart. The command line is updated in the recovery callback.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", *pdwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
        goto cleanup;
    }

    // Register the callback that handles the control event notifications.
    // Used for recovery when an installer is updating a component of the
    // application.
    if (!SetConsoleCtrlHandler(CtrlHandler, TRUE))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"SetConsoleCtrlHandler failed.\n");
        goto cleanup;
    }

    // Register the callback that handles recovery when the application
    // encounters an unhandled exception or becomes unresponsive.
    hr = RegisterApplicationRecoveryCallback(Recover, pdwRecordId, RECOVERY_DEFAULT_PING_INTERVAL, 0);
    if (FAILED(hr))
    {
        // Not failing initialization because the registration failed.
        // Consider calling UnregisterApplicationRestart if you must
        // have the latest state information.
        wprintf(L"RegisterApplicationRecoveryCallback failed with ox%x.\n", hr);
        goto cleanup;
    }

cleanup:

    return hr;
}


// Implement the callback for handling control character events.
// You'd implement this callback if an installer could update a
// component of your application. The system sends a CTRL_C_EVENT
// notification when an installer needs to shutdown your application
// or restart the computer in order to complete the installation.
// You can use the CTRL_C_EVENT to save final state information or
// data before exiting.
BOOL WINAPI CtrlHandler(DWORD dwControlType)
{
    wprintf(L"Entering CtrlHandler...\n");

    switch (dwControlType)
    {
        case CTRL_C_EVENT:
            wprintf(L"Handling CTRL_C_EVENT\n");
            return FALSE;

        // Other cases go here.

        default: 
            wprintf(L"Other, %ul\n", dwControlType);
            return FALSE;
    }
}


// Implement the recovery callback. This callback lets the application
// save state information or data in the event that the application
// encounters an unhandled exception or becomes unresponsive.
DWORD WINAPI Recover(PVOID pContext)
{
    HRESULT hr = S_OK;
    BOOL bCanceled = FALSE;
    DWORD dwRecordId = *(DWORD*)pContext;
    WCHAR wsCommandLine[RESTART_MAX_CMD_LINE];

    wprintf(L"Entering Recover callback...\n");

    // Do recovery work. 

    // Update the restart command line.
    RtlZeroMemory(wsCommandLine, sizeof(wsCommandLine));
    StringCchPrintf(wsCommandLine, sizeof(wsCommandLine), L"/restart -r %lu", dwRecordId);

    hr = RegisterApplicationRestart(wsCommandLine, RESTART_NO_PATCH | RESTART_NO_REBOOT);
    if (FAILED(hr))
    {
        // Not failing because the registration failed.
        wprintf(L"RegisterApplicationRestart failed with ox%x.\n", hr);
    }

    // You must call the ApplicationRecoveryInProgress function within
    // the specified ping interval or the recovery callback exits.
    // Typically, you would do a block of work, call the function, and repeat.
    hr = ApplicationRecoveryInProgress(&bCanceled);
    if (bCanceled)  
    {
        wprintf(L"Recovery was canceled by the user.\n");
        goto cleanup;
    }

    // Do more recovery work. 
    
    // You could also call the RegisterApplicationRestart function to
    // update the command line used for the restart.

cleanup:

    // Save the state file.

    wprintf(L"Leaving Recover callback...\n");
    ApplicationRecoveryFinished((bCanceled) ? FALSE: TRUE);

    return 0;
}
```



 

 
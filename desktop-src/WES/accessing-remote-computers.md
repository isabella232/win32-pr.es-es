---
title: Acceso a equipos remotos
description: Puede usar la API del registro de eventos de Windows para tener acceso a los datos en el equipo local o en un equipo remoto.
ms.assetid: df789981-0e1c-4d68-9bd5-5d054f1724d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0063238560ddd7f1613e94b83ecc7f27900bb3
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104149136"
---
# <a name="accessing-remote-computers"></a>Acceso a equipos remotos

Puede usar la API del registro de eventos de Windows para tener acceso a los datos en el equipo local o en un equipo remoto. Para tener acceso a los datos de un equipo remoto, debe llamar a la función [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) para crear un contexto de sesión remota. Cuando se llama a esta función, se especifica el nombre del equipo remoto al que se desea conectar, las credenciales de usuario que se van a usar para realizar la conexión y el tipo de autenticación que se va a usar para autenticar al usuario. Para especificar el usuario actual, establezca el dominio, el usuario y los miembros de la contraseña en **null**.

Cuando se llama a la API del registro de eventos de Windows, se pasa el identificador al contexto de sesión remota que devuelve la función [**EvtOpenSession**](/windows/desktop/api/WinEvt/nf-winevt-evtopensession) . (Para tener acceso a los datos en el equipo local, pase **null** para especificar la sesión predeterminada). Para tener acceso a los datos del equipo remoto, el equipo remoto debe habilitar la excepción de Firewall de Windows "administración remota de registro de eventos"; de lo contrario, al intentar usar el identificador de sesión, la llamada producirá un error con el \_ servidor RPC S \_ \_ no disponible. El equipo al que se está conectando debe ejecutar Windows Vista o posterior.

En el ejemplo siguiente se muestra cómo conectarse a un equipo remoto.


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote);
void EnumProviders(EVT_HANDLE hRemote);

void main(void)
{
    EVT_HANDLE hRemote = NULL;
    LPWSTR pwsComputerName = L"<name of the remote computer goes here>";
    

    // Enumerate the registered providers on the local computer.
    wprintf(L"Registered providers on the local computer\n\n");
    EnumProviders(hRemote);

    hRemote = ConnectToRemote(pwsComputerName);
    if (NULL == hRemote)
    {
        wprintf(L"Failed to connect to remote computer. Error code is %d.\n", GetLastError());
        goto cleanup;
    }

    // Enumerate the registered providers on the remote computer.
    // To access a remote computer, the remote computer must enable 
    // Remote Event Log Management as an exception in the firewall;
    // otherwise, the remote call fails with RPC_S_SERVER_UNAVAILABLE.
    wprintf(L"\n\nRegistered providers on the remote computer\n\n");
    EnumProviders(hRemote);

cleanup:

    if (hRemote)
        EvtClose(hRemote);
}

// Create a session conext for the remote computer. Set the 
// Domain, User, and Password member to NULL to specify
// the current user.
EVT_HANDLE ConnectToRemote(LPWSTR lpwszRemote)
{
    EVT_HANDLE hRemote = NULL;
    EVT_RPC_LOGIN Credentials;

    RtlZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));
    Credentials.Server = lpwszRemote;
    Credentials.Domain = NULL; 
    Credentials.User = NULL; 
    Credentials.Password = NULL; 
    Credentials.Flags = EvtRpcLoginAuthNegotiate; 

    // This call creates a remote session context; it does not actually
    // create a connection to the remote computer. The connection to
    // the remote computer happens when you use the context.
    hRemote = EvtOpenSession(EvtRpcLogin, &Credentials, 0, 0);

    SecureZeroMemory(&Credentials, sizeof(EVT_RPC_LOGIN));

    return hRemote;
}

// Enumerate the registered providers on the computer.
void EnumProviders(EVT_HANDLE hRemote)
{
    EVT_HANDLE hPublishers = NULL;
    WCHAR wszPublisherName[255 + 1];
    DWORD dwBufferUsed = 0;
    DWORD status = ERROR_SUCCESS;

    hPublishers = EvtOpenPublisherEnum(hRemote, 0);
    if (NULL == hPublishers)
    {
        wprintf(L"EvtOpenPublisherEnum failed with %d\n", GetLastError());
        goto cleanup;
    }

    while (true)
    {
        if (EvtNextPublisherId(hPublishers, sizeof(wszPublisherName)/sizeof(WCHAR), wszPublisherName, &dwBufferUsed))
        {
            wprintf(L"%s\n", wszPublisherName);
        }
        else
        {
            status = GetLastError();
            if (ERROR_NO_MORE_ITEMS == status)
            {
                break;
            }
            else
            {
                wprintf(L"EvtNextPublisherId failed with 0x%ud\n", GetLastError());
            }
        }
    }

cleanup:

    if (hPublishers)
        EvtClose(hPublishers);
}
```

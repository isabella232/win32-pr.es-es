---
description: Windows 8, Windows Server 2012 y versiones posteriores incluyen una nueva característica de Connection Manager que permite a los usuarios conectarse fácilmente a Internet y a otras redes (por ejemplo, redes de trabajo y hogar).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API Interfaz de usuario inalámbricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2b2af7faccc5452163ad89ed28d12e7de917f4b872011165e0cfb1760657dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619932"
---
# <a name="wireless-user-interface-apis"></a>API Interfaz de usuario inalámbricas

Windows 8, Windows Server 2012 y versiones posteriores incluyen una nueva característica de Connection Manager que permite a los usuarios conectarse fácilmente a Internet y a otras redes (por ejemplo, redes de trabajo y hogar). Esta nueva característica Connection Manager reemplaza el Conectar anterior **a** una  red y las interfaces de usuario Administrar redes inalámbricas incluidas con versiones anteriores de Windows para administrar conexiones Wi-Fi nativas.

En Windows 7, Windows Server 2008 y Windows Vista, hay varias interfaces de usuario (URI) que se usan para conectarse a una red inalámbrica o configurarla. Estas URI se pueden iniciar en una aplicación mediante Native Wifi y Windows Shell. Estas URI no están disponibles en Windows 8, Windows Server 2012 y versiones posteriores.

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se puede iniciar ninguna interfaz de usuario usada para conectarse a una red inalámbrica o configurarla en una aplicación mediante programación.

## <a name="connect-to-a-network"></a>Conexión a una red

En Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 y Windows Vista, el asistente de **Conectar a** una red se puede usar para establecer una conexión a una red inalámbrica. Puede usar la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar el Conectar **en un asistente de** red.

El código siguiente muestra una [**llamada a ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) que inicia el **Conectar a un asistente de** red.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**Administración de redes inalámbricas**

En Windows 7, Windows Server 2008 y Windows Vista, el elemento Administrar redes **inalámbricas** Panel de control se usa para administrar perfiles de red inalámbrica. La [**función ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) también se puede usar para iniciar el **elemento Administrar redes inalámbricas.** La ruta de acceso que se va a usar al llamar **a ShellExecute** Windows 7 y Windows Vista es la siguiente:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

El código de ejemplo siguiente muestra cómo usar [**ShellExecute para**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) iniciar el Asistente para redes **inalámbricas administradas** desde una aplicación.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>Opciones Configuración perfiles de red inalámbrica

Windows Vista y versiones posteriores incluyen una interfaz de usuario avanzada que se usa para ver y editar la configuración avanzada de un perfil de red inalámbrica. Puede iniciar esta interfaz de usuario avanzada llamando a [**la función WlanUIEditProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 

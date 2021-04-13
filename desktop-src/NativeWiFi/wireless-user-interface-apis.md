---
description: Windows 8, Windows Server 2012 y versiones posteriores incluyen una nueva característica de administrador de conexiones que permite a los usuarios conectarse fácilmente a Internet y a otras redes (por ejemplo, redes domésticas y de trabajo).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API de interfaz de usuario inalámbrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547086"
---
# <a name="wireless-user-interface-apis"></a>API de interfaz de usuario inalámbrica

Windows 8, Windows Server 2012 y versiones posteriores incluyen una nueva característica de administrador de conexiones que permite a los usuarios conectarse fácilmente a Internet y a otras redes (por ejemplo, redes domésticas y de trabajo). Esta nueva característica de administrador de conexiones reemplaza a las interfaces de usuario **conectarse a una red** y **administrar redes inalámbricas** incluidas con versiones anteriores de Windows para administrar conexiones WiFi nativas.

En Windows 7, Windows Server 2008 y Windows Vista, hay varias interfaces de usuario (UI) que se usan para conectarse a una red inalámbrica o configurarla. Estas interfaces de red se pueden iniciar en una aplicación mediante las funciones nativas de Wi-Fi y Windows Shell. Estas ius no están disponibles en Windows 8, Windows Server 2012 y versiones posteriores.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** No se puede iniciar ninguna interfaz de usuario utilizada para conectarse a una red inalámbrica o configurarla en una aplicación mediante programación.

## <a name="connect-to-a-network"></a>Conexión a una red

En Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 y Windows Vista, el Asistente para **conectarse a una red** se puede usar para establecer una conexión a una red inalámbrica. Puede utilizar la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar el Asistente para **conectarse a una red** .

En el código siguiente se muestra una llamada a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) que inicia el asistente **para conectarse a una red** .


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



## <a name="manage-wireless-networks"></a>**Administrar redes inalámbricas**

En Windows 7, Windows Server 2008 y Windows Vista, el elemento **administrar redes inalámbricas** del panel de control se utiliza para administrar los perfiles de red inalámbrica. La función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) también se puede usar para iniciar el elemento **administrar redes inalámbricas** . La ruta de acceso que se debe usar al llamar a **ShellExecute** en Windows 7 y Windows Vista es la siguiente:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

En el código de ejemplo siguiente se muestra cómo usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar el Asistente para **redes inalámbricas administradas** desde una aplicación.


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



## <a name="advanced-settings-for-wireless-network-profiles"></a>Configuración avanzada para perfiles de red inalámbrica

Windows Vista y versiones posteriores incluyen una interfaz de usuario avanzada que se usa para ver y editar la configuración avanzada de un perfil de red inalámbrica. Puede iniciar esta interfaz de usuario avanzada mediante una llamada a la función [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 

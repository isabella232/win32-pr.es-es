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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="e4ef6-103">API de interfaz de usuario inalámbrica</span><span class="sxs-lookup"><span data-stu-id="e4ef6-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="e4ef6-104">Windows 8, Windows Server 2012 y versiones posteriores incluyen una nueva característica de administrador de conexiones que permite a los usuarios conectarse fácilmente a Internet y a otras redes (por ejemplo, redes domésticas y de trabajo).</span><span class="sxs-lookup"><span data-stu-id="e4ef6-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="e4ef6-105">Esta nueva característica de administrador de conexiones reemplaza a las interfaces de usuario **conectarse a una red** y **administrar redes inalámbricas** incluidas con versiones anteriores de Windows para administrar conexiones WiFi nativas.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="e4ef6-106">En Windows 7, Windows Server 2008 y Windows Vista, hay varias interfaces de usuario (UI) que se usan para conectarse a una red inalámbrica o configurarla.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="e4ef6-107">Estas interfaces de red se pueden iniciar en una aplicación mediante las funciones nativas de Wi-Fi y Windows Shell.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="e4ef6-108">Estas ius no están disponibles en Windows 8, Windows Server 2012 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="e4ef6-109">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** No se puede iniciar ninguna interfaz de usuario utilizada para conectarse a una red inalámbrica o configurarla en una aplicación mediante programación.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="e4ef6-110">Conexión a una red</span><span class="sxs-lookup"><span data-stu-id="e4ef6-110">Connect to a network</span></span>

<span data-ttu-id="e4ef6-111">En Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 y Windows Vista, el Asistente para **conectarse a una red** se puede usar para establecer una conexión a una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="e4ef6-112">Puede utilizar la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar el Asistente para **conectarse a una red** .</span><span class="sxs-lookup"><span data-stu-id="e4ef6-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="e4ef6-113">En el código siguiente se muestra una llamada a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) que inicia el asistente **para conectarse a una red** .</span><span class="sxs-lookup"><span data-stu-id="e4ef6-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="e4ef6-114">**Administrar redes inalámbricas**</span><span class="sxs-lookup"><span data-stu-id="e4ef6-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="e4ef6-115">En Windows 7, Windows Server 2008 y Windows Vista, el elemento **administrar redes inalámbricas** del panel de control se utiliza para administrar los perfiles de red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="e4ef6-116">La función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) también se puede usar para iniciar el elemento **administrar redes inalámbricas** .</span><span class="sxs-lookup"><span data-stu-id="e4ef6-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="e4ef6-117">La ruta de acceso que se debe usar al llamar a **ShellExecute** en Windows 7 y Windows Vista es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4ef6-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="e4ef6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="e4ef6-119">En el código de ejemplo siguiente se muestra cómo usar [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar el Asistente para **redes inalámbricas administradas** desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="e4ef6-120">Configuración avanzada para perfiles de red inalámbrica</span><span class="sxs-lookup"><span data-stu-id="e4ef6-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="e4ef6-121">Windows Vista y versiones posteriores incluyen una interfaz de usuario avanzada que se usa para ver y editar la configuración avanzada de un perfil de red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e4ef6-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="e4ef6-122">Puede iniciar esta interfaz de usuario avanzada mediante una llamada a la función [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .</span><span class="sxs-lookup"><span data-stu-id="e4ef6-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ef6-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4ef6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ef6-124">Usar Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="e4ef6-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="e4ef6-125">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="e4ef6-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="e4ef6-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="e4ef6-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="e4ef6-127">**WlanUIEditProfile**</span><span class="sxs-lookup"><span data-stu-id="e4ef6-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 

---
description: Para enumerar todos los dispositivos del equipo, llame a la función EnumDisplayDevices. La información que se devuelve también indica qué monitor forma parte del escritorio.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Enumeración y control de visualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082361"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="a461a-104">Enumeración y control de visualización</span><span class="sxs-lookup"><span data-stu-id="a461a-104">Enumeration and Display Control</span></span>

<span data-ttu-id="a461a-105">Para enumerar todos los dispositivos del equipo, llame a la función [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) .</span><span class="sxs-lookup"><span data-stu-id="a461a-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="a461a-106">La información que se devuelve también indica qué monitor forma parte del escritorio.</span><span class="sxs-lookup"><span data-stu-id="a461a-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="a461a-107">Para enumerar los dispositivos del escritorio que forman una intersección con una región de recorte, llame a [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span><span class="sxs-lookup"><span data-stu-id="a461a-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="a461a-108">Esto devuelve el identificador HMONITOR de cada monitor, que se usa con [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="a461a-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="a461a-109">Para enumerar todos los dispositivos de la pantalla virtual, use **EnumDisplayMonitors**.</span><span class="sxs-lookup"><span data-stu-id="a461a-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="a461a-110">como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="a461a-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="a461a-111">Para obtener información acerca de un dispositivo de pantalla, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) o [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span><span class="sxs-lookup"><span data-stu-id="a461a-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="a461a-112">La función [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) se usa para controlar los dispositivos de pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="a461a-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="a461a-113">Puede modificar la configuración de los dispositivos, como especificar la posición de un monitor en el escritorio virtual y cambiar la profundidad de bits de cualquier pantalla.</span><span class="sxs-lookup"><span data-stu-id="a461a-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="a461a-114">Normalmente, una aplicación no usa esta función.</span><span class="sxs-lookup"><span data-stu-id="a461a-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="a461a-115">Para agregar un monitor de pantalla a un sistema de varios monitores mediante programación, establezca **DEVMODE. dmFields** en \_ la posición DM y especifique una posición (mediante **DEVMODE. dmPosition** ) para el monitor que está agregando, que es adyacente al menos a un píxel del área de visualización de un monitor existente.</span><span class="sxs-lookup"><span data-stu-id="a461a-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="a461a-116">Para desasociar el monitor, establezca **DEVMODE. dmFields** en la \_ posición DM y establezca **DEVMODE. DmPelsWidth** y **DEVMODE. dmPelsHeight** en cero.</span><span class="sxs-lookup"><span data-stu-id="a461a-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="a461a-117">En el código siguiente se muestra cómo desasociar todos los dispositivos de pantalla secundarios del escritorio:</span><span class="sxs-lookup"><span data-stu-id="a461a-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



<span data-ttu-id="a461a-118">Para cada dispositivo de pantalla, la aplicación puede guardar información en el registro que describe los parámetros de configuración para el dispositivo, así como los parámetros de ubicación.</span><span class="sxs-lookup"><span data-stu-id="a461a-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="a461a-119">La aplicación también puede determinar qué pantallas forman parte del escritorio y cuáles no, a través de la marca Mostrar el \_ dispositivo \_ conectado \_ a \_ escritorio en la estructura de pantalla del [**\_ dispositivo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="a461a-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="a461a-120">Una vez que toda la información de configuración se almacena en el registro, la aplicación puede volver a llamar a [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) para cambiar la configuración de forma dinámica, sin necesidad de reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="a461a-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 




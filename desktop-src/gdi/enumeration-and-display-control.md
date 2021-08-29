---
description: Para enumerar todos los dispositivos del equipo, llame a la función EnumDisplayDevices. La información que se devuelve también indica qué monitor forma parte del escritorio.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Enumeración y control de visualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5af1449100c667b6e1a964887c26e3301d6e14c748c3a822e3abdc7fe36da8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965985"
---
# <a name="enumeration-and-display-control"></a>Enumeración y control de visualización

Para enumerar todos los dispositivos del equipo, llame a la [**función EnumDisplayDevices.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) La información que se devuelve también indica qué monitor forma parte del escritorio.

Para enumerar los dispositivos del escritorio que se intersecan con una región de recorte, llame a [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors). Esto devuelve el identificador HMONITOR a cada monitor, que se usa con [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa). Para enumerar todos los dispositivos de la pantalla virtual, use **EnumDisplayMonitors**. como se muestra en el código siguiente:


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Para obtener información sobre un dispositivo para mostrar, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) o [**EnumDisplaySettingsEx.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)

La [**función ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) se usa para controlar los dispositivos de visualización en el equipo. Puede modificar la configuración de los dispositivos, como especificar la posición de un monitor en el escritorio virtual y cambiar la profundidad de bits de cualquier pantalla. Normalmente, una aplicación no usa esta función. Para agregar un monitor de pantalla a un sistema de varios monitores mediante programación, establezca **DEVMODE.dmFields** en DM POSITION y especifique una posición \_ (mediante **DEVMODE.dmPosition)** para el monitor que va a agregar que sea adyacente al menos a un píxel del área de visualización de un monitor existente. Para desasociar el monitor, establezca **DEVMODE.dmFields** en DM POSITION y \_ **establezca DEVMODE.dmPelsWidth** y **DEVMODE.dmPelsHeight** en cero.

En el código siguiente se muestra cómo separar todos los dispositivos de visualización secundarios del escritorio:


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



Para cada dispositivo para mostrar, la aplicación puede guardar información en el Registro que describe los parámetros de configuración del dispositivo, así como los parámetros de ubicación. La aplicación también puede determinar qué pantallas forman parte del escritorio y cuáles no a través de la marca DISPLAY DEVICE ATTACHED TO DESKTOP en la estructura \_ \_ DISPLAY \_ \_ [**\_ DEVICE.**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) Una vez almacenada toda la información de configuración en el Registro, la aplicación puede volver a llamar a [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) para cambiar dinámicamente la configuración, sin necesidad de reiniciarla.

 

 




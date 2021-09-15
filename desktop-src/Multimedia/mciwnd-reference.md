---
title: Referencia de MCIWnd
description: Referencia de MCIWnd
ms.assetid: 11fba6bb-17f1-4fbe-b148-4755a3c6216a
keywords:
- MCI (interfaz de control multimedia), referencia de MCIWnd
- Clase de ventana MCIWnd, referencia
- Ventana de MCIWnd, referencia
- Referencia de MCIWnd, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76333f38a5dec3edaadcae69777703ebea61296f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476823"
---
# <a name="mciwnd-reference"></a>Referencia de MCIWnd

En esta sección se describen las funciones, mensajes y macros asociados a la clase de ventana MCIWnd. Estos elementos se agrupan como se muestra a continuación.

## <a name="window-management"></a>Administración de ventanas

-   [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
-   [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
-   [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles)
-   [**MCIWndRegisterClass**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass)

## <a name="file-and-device-management"></a>Archivo y Administración de dispositivos

-   [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose)
-   [**MCIWndDestroy**](/windows/desktop/api/Vfw/nf-vfw-mciwnddestroy)
-   [**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
-   [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
-   [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
-   [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)
-   [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave)
-   [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog)

## <a name="playback-options"></a>Opciones de reproducción

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="recording"></a>Grabación

-   [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord)

## <a name="positioning"></a>Posicionamiento

-   [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)
-   [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
-   [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
-   [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
-   [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
-   [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
-   [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome)
-   [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
-   [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep)

## <a name="pause-and-resume-playback"></a>Pausar y reanudar la reproducción

-   [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
-   [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay)
-   [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)
-   [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
-   [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
-   [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
-   [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)

## <a name="performance-tuning"></a>Optimización del rendimiento

-   [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
-   [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
-   [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
-   [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
-   [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
-   [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)

## <a name="image-and-palette-adjustments"></a>Ajustes de imagen y paleta

-   [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
-   [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette)
-   [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
-   [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
-   [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource)
-   [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
-   [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)

## <a name="event-and-error-notification"></a>Notificación de eventos y errores

-   [**MCIWndGetError**](/windows/desktop/api/Vfw/nf-vfw-mciwndgeterror)
-   [**MCIWNDM \_ NOTIFYERROR**](mciwndm-notifyerror.md)
-   [**MCIWNDM \_ NOTIFYMEDIA**](mciwndm-notifymedia.md)
-   [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md)
-   [**MCIWNDM \_ NOTIFYPOS**](mciwndm-notifypos.md)
-   [**MCIWNDM \_ NOTIFYSIZE**](mciwndm-notifysize.md)

## <a name="time-formats"></a>Formatos de hora

-   [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
-   [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
-   [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
-   [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
-   [**MCIWndValidateMedia**](/windows/desktop/api/Vfw/nf-vfw-mciwndvalidatemedia)

## <a name="status-updates"></a>Actualizaciones de estado

-   [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
-   [**MCIWndGetCiónTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
-   [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
-   [**MCIWndSetCiónTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
-   [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)

## <a name="device-capabilities"></a>Capacidades del dispositivo

-   [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
-   [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
-   [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
-   [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
-   [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
-   [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)

## <a name="mci-device-settings"></a>MCI Device Configuración

-   [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
-   [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice)
-   [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
-   [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename)
-   [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)

## <a name="mci-command-string-interface"></a>Interfaz Command-String MCI

-   [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring)
-   [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clase Window de MCIWnd](mciwnd-window-class.md)
</dt> </dl>

 

 





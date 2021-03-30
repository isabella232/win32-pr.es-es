---
title: Proporcionar seguridad de cliente RDP
description: Algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775721"
---
# <a name="providing-for-rdp-client-security"></a>Proporcionar seguridad de cliente RDP

Para permitir que los clientes se protejan de servidores potencialmente no confiables, algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. Esto significa que, cuando un usuario que examina la Web accede a la página y la página se encuentra en una zona de seguridad de dirección URL superior a la del equipo en el que explora la web, estas propiedades se deshabilitan. Se tiene acceso a estas propiedades restringidas mediante la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) y la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , y están disponibles en las siguientes zonas de seguridad de direcciones URL de Internet Explorer:

-   Mi PC
-   Intranet local
-   Sitios de confianza

Están deshabilitadas en estas zonas:

-   Internet
-   Sitios restringidos

Si llama a estas propiedades restringidas dentro de su Servicios de Escritorio remoto aplicación Web, debe llamar a [**IMsTscAx:: get \_ SecuredSettings**](imstscax-securedsettings.md) y [**IMsTscAx:: get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para tener acceso a las propiedades de configuración segura.

Las propiedades restringidas a las que tiene acceso la interfaz **IMsTscSecuredSettings** son las siguientes:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Esta propiedad especifica el programa que se iniciará al conectarse.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Esta propiedad especifica el directorio de trabajo del programa especificado en [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   [**Pantalla completa**](imstscsecuredsettings-fullscreen.md). Esta propiedad especifica si el estado del control al conectarse estará en modo de pantalla completa o de ventana. Si el valor de esta propiedad es **true**, la conexión se abrirá en modo de pantalla completa. Aunque el uso de la propiedad **Fullscreen** está restringido a las zonas de seguridad de direcciones URL de Internet Explorer enumeradas anteriormente, un usuario siempre puede cambiar al modo de pantalla completa después de la conexión presionando la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).

Las propiedades a las que accede la interfaz **IMsRdpClientSecuredSettings** son las siguientes:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Esta propiedad especifica si se deben redirigir los sonidos o reproducir sonidos en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Esta propiedad especifica cómo y cuándo aplicar las combinaciones de teclas de Windows; por ejemplo, ALT + TAB.

El siguiente script inicia Microsoft Notepad.exe tras la conexión. Ejecute este script antes de llamar al método [**IMsTscAx:: Connect**](imstscax-connect.md) .

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 





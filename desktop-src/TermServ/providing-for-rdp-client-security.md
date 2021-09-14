---
title: Proporcionar seguridad de cliente RDP
description: Algunas propiedades del objeto Escritorio remoto ActiveX control están restringidas a zonas de seguridad de Internet Explorer URL específicas.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068605"
---
# <a name="providing-for-rdp-client-security"></a>Proporcionar seguridad de cliente RDP

Para permitir que los clientes se protejan de servidores potencialmente no confiables, algunas propiedades del objeto de control Escritorio remoto ActiveX están restringidas a zonas de seguridad de Internet Explorer URL específicas. Esto significa que, cuando un usuario que examina la web accede a la página y la página está en una zona de seguridad de dirección URL más alta que el equipo con el que está explorando la web, estas propiedades están deshabilitadas. A estas propiedades restringidas se accede mediante la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) y la interfaz [**IMsRdpClientSecuredSettings,**](imsrdpclientsecuredsettings-interface.md) y están disponibles en las siguientes zonas de seguridad Internet Explorer URL:

-   Mi equipo
-   Intranet local
-   Sitios de confianza

Están deshabilitadas en estas zonas:

-   Internet
-   Sitios restringidos

Si llama a estas propiedades restringidas dentro de la aplicación web de Servicios de Escritorio remoto, debe llamar a [**IMsTscAx::get \_ SecuredSettings**](imstscax-securedsettings.md) e [**IMsTscAx::get \_ SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para acceder a las propiedades Configuración seguras.

Las propiedades restringidas a las que accede la interfaz **IMsTscSecuredSettings** son las siguientes:

-   [**StartProgram**](imstscsecuredsettings-startprogram.md). Esta propiedad especifica el programa que se va a iniciar tras la conexión.
-   [**WorkDir**](imstscsecuredsettings-workdir.md). Esta propiedad especifica el directorio de trabajo del programa especificado en [**StartProgram**](imstscsecuredsettings-startprogram.md).
-   [**FullScreen**](imstscsecuredsettings-fullscreen.md). Esta propiedad especifica si el estado del control tras la conexión estará en modo de pantalla completa o de ventana. Si el valor de esta propiedad es **TRUE,** la conexión se abrirá en modo de pantalla completa. Aunque el uso de la propiedad **FullScreen** está restringido a las zonas de seguridad de url de Internet Explorer enumeradas anteriormente, [](terminal-services-shortcut-keys.md) un usuario siempre puede cambiar al modo de pantalla completa después de la conexión presionando la combinación de teclas de método abreviado de modo de pantalla completa (CTRL+ALT+BREAK).

Las propiedades a las que accede la interfaz **IMsRdpClientSecuredSettings** son las siguientes:

-   [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md). Esta propiedad especifica si se redirigirán los sonidos o se reproducirán sonidos en el Escritorio remoto host de sesión de Escritorio remoto.
-   [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md). Esta propiedad especifica cómo y cuándo aplicar Windows combinaciones de teclas; por ejemplo, ALT+TAB.

El siguiente script inicia Microsoft Notepad.exe conexión. Ejecute este script antes de llamar al [**método IMsTscAx::Conectar.**](imstscax-connect.md)

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 





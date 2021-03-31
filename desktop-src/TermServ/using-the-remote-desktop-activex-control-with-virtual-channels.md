---
title: Usar el control ActiveX Escritorio remoto con canales virtuales
description: Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903546"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Usar el control ActiveX Escritorio remoto con canales virtuales

Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente que tienen acceso al servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) mediante el control Escritorio remoto ActiveX.

**Para hacer que una aplicación de canal virtual esté disponible**

1.  Implemente el módulo del lado servidor de la aplicación y asegúrese de que se está ejecutando en el servidor host de sesión de escritorio remoto. En la página conexión de la aplicación Web Servicios de Escritorio remoto que se ejecuta en el servidor Web, acceda a la propiedad **PluginDlls** de la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar el nombre de la dll del canal virtual. Si tiene más de un complemento, especifique una lista delimitada por comas de nombres de archivos DLL. Por ejemplo, si el complemento de canal virtual se denomina "MyPlugin.dll", use el código siguiente:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Use el código siguiente si tiene dos dll de canal virtual. En este ejemplo, los nombres de archivo DLL son "MyPlugin.dll" y "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Por motivos de seguridad, la propiedad **PluginDlls** solo acepta una lista con nombre de dll de canal virtual. El control devuelve un error si se especifica algún tipo de sistema de archivos o ruta de acceso UNC. Además, los nombres de los archivos dll solo deben contener caracteres alfanuméricos.

2.  Asegúrese de que el módulo de cliente está instalado en el directorio% WINDIR% \\ system32.

La API de canal virtual no permite que se carguen varias instancias de la misma DLL de canal virtual dentro de un único proceso. Por este motivo, si hay varias instancias del control ActiveX Escritorio remoto que se ejecutan en el mismo proceso, solo la primera instancia del control podrá cargar el archivo DLL del canal virtual. Si está diseñando una aplicación de canal virtual que debe admitir varias instancias en un único proceso, debe usar la API de [canales virtuales dinámicos](dynamic-virtual-channels.md) para implementar la aplicación de canal virtual.

> [!Note]  
> De forma predeterminada, el control ActiveX Escritorio remoto carga los archivos DLL del cliente del canal virtual desde el directorio% WINDIR% \\ system32. Un administrador puede cambiar este directorio DLL de complemento de cliente predeterminado. Para ello, edite la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** en el equipo cliente. No se puede especificar esta ruta de acceso del directorio en el formato UNC.

 

 

 





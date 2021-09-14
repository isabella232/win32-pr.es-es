---
title: Uso del control Escritorio remoto ActiveX con canales virtuales
description: Si ha habilitado una aplicación de canales virtuales en Servicios de Escritorio remoto implementación, puede hacer que esta aplicación esté disponible para los equipos cliente.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249855"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Uso del control Escritorio remoto ActiveX con canales virtuales

Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente que acceden al servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) mediante el control Escritorio remoto ActiveX.

**Para que una aplicación de canal virtual esté disponible**

1.  Implemente el módulo del lado servidor de la aplicación y asegúrese de que se ejecuta en el servidor host de sesión de Escritorio remoto. En la página de conexión de la aplicación web Servicios de Escritorio remoto que se ejecuta en el servidor web, acceda a la propiedad **PluginDlls** de la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar el nombre del archivo DLL del canal virtual. Si tiene más de un complemento, especifique una lista delimitada por comas de nombres dll. Por ejemplo, si el complemento de canal virtual se denomina "MyPlugin.dll", use el código siguiente:

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Use el código siguiente si tiene dos archivos DLL de canal virtual. En este ejemplo, los nombres de archivo DLL son "MyPlugin.dll" y "Vdriver.dll":

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Por motivos de seguridad, **la propiedad PluginDlls** solo acepta una lista con nombre de archivos DLL de canal virtual. El control devuelve un error si se especifica cualquier forma de sistema de archivos o ruta de acceso UNC. Además, los nombres de los archivos DLL deben contener solo caracteres alfanuméricos.

2.  Asegúrese de que el módulo del lado cliente está instalado en el directorio %windir% \\ system32.

La API de canal virtual no permite que varias instancias del mismo archivo DLL de canal virtual se carguen dentro de un único proceso. Por este problema, si hay varias instancias del control Escritorio remoto ActiveX que se ejecutan dentro del mismo proceso, solo la primera instancia del control podrá cargar el archivo DLL del canal virtual. Si va a diseñar una aplicación de canal virtual que debe admitir varias instancias dentro de un único proceso, debe usar la [API](dynamic-virtual-channels.md) de canales virtuales dinámicos para implementar la aplicación de canal virtual.

> [!Note]  
> De forma predeterminada, el Escritorio remoto ActiveX carga archivos DLL de cliente de canal virtual desde el directorio %windir% \\ system32. Es posible que un administrador cambie este directorio DLL de complemento de cliente predeterminado. Para ello, edite la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** en el equipo cliente. Esta ruta de acceso del directorio no se puede especificar en el formato UNC.

 

 

 





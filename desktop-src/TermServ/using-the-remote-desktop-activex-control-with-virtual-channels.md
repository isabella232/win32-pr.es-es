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
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="cb0af-103">Usar el control ActiveX Escritorio remoto con canales virtuales</span><span class="sxs-lookup"><span data-stu-id="cb0af-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="cb0af-104">Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente que tienen acceso al servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) mediante el control Escritorio remoto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="cb0af-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="cb0af-105">**Para hacer que una aplicación de canal virtual esté disponible**</span><span class="sxs-lookup"><span data-stu-id="cb0af-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="cb0af-106">Implemente el módulo del lado servidor de la aplicación y asegúrese de que se está ejecutando en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cb0af-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="cb0af-107">En la página conexión de la aplicación Web Servicios de Escritorio remoto que se ejecuta en el servidor Web, acceda a la propiedad **PluginDlls** de la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) para especificar el nombre de la dll del canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb0af-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="cb0af-108">Si tiene más de un complemento, especifique una lista delimitada por comas de nombres de archivos DLL.</span><span class="sxs-lookup"><span data-stu-id="cb0af-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="cb0af-109">Por ejemplo, si el complemento de canal virtual se denomina "MyPlugin.dll", use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="cb0af-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="cb0af-110">Use el código siguiente si tiene dos dll de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb0af-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="cb0af-111">En este ejemplo, los nombres de archivo DLL son "MyPlugin.dll" y "Vdriver.dll":</span><span class="sxs-lookup"><span data-stu-id="cb0af-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="cb0af-112">Por motivos de seguridad, la propiedad **PluginDlls** solo acepta una lista con nombre de dll de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb0af-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="cb0af-113">El control devuelve un error si se especifica algún tipo de sistema de archivos o ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="cb0af-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="cb0af-114">Además, los nombres de los archivos dll solo deben contener caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="cb0af-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="cb0af-115">Asegúrese de que el módulo de cliente está instalado en el directorio% WINDIR% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="cb0af-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="cb0af-116">La API de canal virtual no permite que se carguen varias instancias de la misma DLL de canal virtual dentro de un único proceso.</span><span class="sxs-lookup"><span data-stu-id="cb0af-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="cb0af-117">Por este motivo, si hay varias instancias del control ActiveX Escritorio remoto que se ejecutan en el mismo proceso, solo la primera instancia del control podrá cargar el archivo DLL del canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb0af-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="cb0af-118">Si está diseñando una aplicación de canal virtual que debe admitir varias instancias en un único proceso, debe usar la API de [canales virtuales dinámicos](dynamic-virtual-channels.md) para implementar la aplicación de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="cb0af-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="cb0af-119">De forma predeterminada, el control ActiveX Escritorio remoto carga los archivos DLL del cliente del canal virtual desde el directorio% WINDIR% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="cb0af-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="cb0af-120">Un administrador puede cambiar este directorio DLL de complemento de cliente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cb0af-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="cb0af-121">Para ello, edite la clave del registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="cb0af-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="cb0af-122">No se puede especificar esta ruta de acceso del directorio en el formato UNC.</span><span class="sxs-lookup"><span data-stu-id="cb0af-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 





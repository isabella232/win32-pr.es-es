---
description: La parte entera de la prueba y depuración de las implementaciones del controlador de protocolo es entender cómo se inician los controladores de protocolo.
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Controladores de protocolo de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153945"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="ebc2a-103">Controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="ebc2a-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="ebc2a-104">La parte entera de la prueba y depuración de las implementaciones del controlador de protocolo es entender cómo se inician los controladores de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="ebc2a-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ebc2a-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ebc2a-106">Acerca de los controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="ebc2a-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="ebc2a-107">Configuración de la depuración</span><span class="sxs-lookup"><span data-stu-id="ebc2a-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="ebc2a-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ebc2a-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="ebc2a-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc2a-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="ebc2a-110">Acerca de los controladores de protocolo de depuración</span><span class="sxs-lookup"><span data-stu-id="ebc2a-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="ebc2a-111">El proceso SearchIndexer (searchindexer.exe) inicia una copia del proceso SearchProtocolHost (SearchProtocolHost.exe) en el contexto del sistema y otra copia en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="ebc2a-112">A continuación, los controladores de protocolo se cargan en el proceso SearchProtocolHost según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="ebc2a-113">No se descargan hasta que se detiene el servicio de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="ebc2a-114">Se reutiliza la misma instancia de un controlador de protocolo cualquier número de veces que se esté ejecutando el servicio.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="ebc2a-115">Los procesos SearchIndexer y SearchProtocolHost se comunican con frecuencia durante la indexación.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="ebc2a-116">Si pausa o detiene el proceso SearchProtocolHost para depurar, el SearchIndexer iniciará un nuevo proceso SearchProtocolHost, invalidando la sesión de depuración.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="ebc2a-117">Además, si asocia el depurador directamente al proceso SearchProtocolHost, puede interrumpir la herencia de identificador de searchindexer.exe a searchprotocolhost.exe y los dos procesos no podrán comunicarse.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="ebc2a-118">Para evitar estos problemas, debe notificar al servicio de búsqueda que está depurando y debe adjuntar el depurador al proceso SearchIndexer con instrucciones para depurar procesos secundarios, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="ebc2a-119">Configuración de la depuración</span><span class="sxs-lookup"><span data-stu-id="ebc2a-119">Setting Up Debugging</span></span>

<span data-ttu-id="ebc2a-120">Siga estos pasos para configurar la depuración para el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="ebc2a-121">Notifique al servicio de búsqueda que está depurando estableciendo el valor de DebugFilters en 1 en el registro:</span><span class="sxs-lookup"><span data-stu-id="ebc2a-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="ebc2a-122">Adjunte un depurador mediante la clave del registro opciones de ejecución del archivo de imagen:</span><span class="sxs-lookup"><span data-stu-id="ebc2a-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="ebc2a-123">En la tabla siguiente se describen las opciones de un depurador de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="ebc2a-124">**Ejemplo de uso del** depurador NTSD Debugger *= C: \\ debuggers \\ntsd.exe-odGx-C: "sxe LD mydll.dll; g"*   </span><span class="sxs-lookup"><span data-stu-id="ebc2a-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="ebc2a-125">Reinicie searchindexer.exe en el depurador con compmgmt. msc, Services. msc o una ventana de comandos con comandos similares a los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ebc2a-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="ebc2a-126">Para distinguir entre un proceso SearchProtocolHost que se ejecuta en el contexto del sistema y otro que se ejecuta en el contexto de usuario, puede revisar las cadenas de entorno.</span><span class="sxs-lookup"><span data-stu-id="ebc2a-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="ebc2a-127">Con ntsd.exe, por ejemplo, puede usar el comando de extensión **! PEB** para mostrar una vista con formato de la información en el bloque de entorno de proceso (PEB).</span><span class="sxs-lookup"><span data-stu-id="ebc2a-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebc2a-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ebc2a-128">Additional Resources</span></span>

-   <span data-ttu-id="ebc2a-129">Para obtener información sobre cómo crear controladores, consulte [registrar extensiones de Shell](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="ebc2a-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebc2a-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebc2a-130">Related topics</span></span>

<dl> <span data-ttu-id="ebc2a-131"><dt>**Conceptos**</dt> básicos del <dt><a href="-search-3x-wds-phaddins.md">desarrollo de controladores</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Descripción</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">de los controladores de protocolo notificación del índice de cambios</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Agregar iconos y menús contextuales</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">ejemplo de código: extensiones de Shell para controladores de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">crear un conector de búsqueda para un controlador de protocolo</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">instalar y registrar controladores</a></dt> de protocolo </span><span class="sxs-lookup"><span data-stu-id="ebc2a-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 

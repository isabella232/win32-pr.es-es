---
description: Obtenga información acerca de cómo extender la cinta de opciones del explorador de Windows.
title: Extender la cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540454"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="bb12f-103">Extender la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="bb12f-103">Extending the Ribbon</span></span>

<span data-ttu-id="bb12f-104">En el explorador de Windows, la cinta de opciones facilita más la detección de las actividades comunes de administración de archivos de usuario final, pero hay cambios afoot para los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bb12f-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="bb12f-105">Por ejemplo, la antigua barra de comandos era extensible pero la cinta de opciones está más restringida en este momento.</span><span class="sxs-lookup"><span data-stu-id="bb12f-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="bb12f-106">Además, la cinta no se muestra de forma predeterminada para todas las extensiones de espacio de nombres, por lo que tiene que optar por obtener la cinta de opciones. de lo contrario, obtendrá la barra de comandos anterior.</span><span class="sxs-lookup"><span data-stu-id="bb12f-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="bb12f-107">Las acciones disponibles para los usuarios de la cinta de opciones se dividen en tres categorías de extensibilidad:</span><span class="sxs-lookup"><span data-stu-id="bb12f-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="bb12f-108">No es necesaria la extensibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb12f-108">Extensibility is not needed.</span></span> <span data-ttu-id="bb12f-109">Ejemplos: copiar, pegar y eliminar.</span><span class="sxs-lookup"><span data-stu-id="bb12f-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="bb12f-110">Windows controla estos verbos automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bb12f-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="bb12f-111">Actualmente no se permite la extensibilidad: ejemplos: zip, cerrar sesión y otras acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bb12f-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="bb12f-112">Use el menú contextual para cubrir estos escenarios.</span><span class="sxs-lookup"><span data-stu-id="bb12f-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="bb12f-113">La extensibilidad está integrada en la propia acción.</span><span class="sxs-lookup"><span data-stu-id="bb12f-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="bb12f-114">Ejemplos: buscar, correo electrónico, imprimir, nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="bb12f-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="bb12f-115">Debe registrar estos verbos para incluir la aplicación o el formato de archivo en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="bb12f-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="bb12f-116">En este documento se describe cómo puede participar para obtener la cinta de opciones y cómo registrarse para administrar verbos de la cinta de opciones específicos.</span><span class="sxs-lookup"><span data-stu-id="bb12f-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="bb12f-117">Participar en la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="bb12f-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="bb12f-118">Para participar en la cinta de opciones, la implementación de [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) debe especificar la **\_ cinta de EP** en [**IExplorerPaneVisibility:: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) y devolver el **\_** \| **\_ valor predeterminado \_ de EPS de** la fuerza EPS en.</span><span class="sxs-lookup"><span data-stu-id="bb12f-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="bb12f-119">Extender la cinta de opciones para extensiones de archivo</span><span class="sxs-lookup"><span data-stu-id="bb12f-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="bb12f-120">Estos botones de la cinta son extensibles en función de las extensiones de archivo:</span><span class="sxs-lookup"><span data-stu-id="bb12f-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="bb12f-121">Extraer todo</span><span class="sxs-lookup"><span data-stu-id="bb12f-121">Extract All</span></span>
-   <span data-ttu-id="bb12f-122">Montaje de la \| grabación (ISO)</span><span class="sxs-lookup"><span data-stu-id="bb12f-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="bb12f-123">Reproducir \| todo \| Agregar a lista de reproducción (verbo: enqueue)</span><span class="sxs-lookup"><span data-stu-id="bb12f-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="bb12f-124">Abrir</span><span class="sxs-lookup"><span data-stu-id="bb12f-124">Open</span></span>
-   <span data-ttu-id="bb12f-125">Editar</span><span class="sxs-lookup"><span data-stu-id="bb12f-125">Edit</span></span>
-   <span data-ttu-id="bb12f-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb12f-126">Properties</span></span>

<span data-ttu-id="bb12f-127">Cuando se registra para controlar estáticamente los verbos relevantes para los nuevos tipos de archivo, la cinta de opciones controla los verbos de manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="bb12f-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="bb12f-128">Se registra del mismo modo que lo haría para los verbos de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="bb12f-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="bb12f-129">Para obtener más información sobre las asociaciones de archivos y el registro de verbos, vea [verbos y asociaciones de archivos](fa-verbs.md) y [crear controladores de menús contextuales](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="bb12f-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="bb12f-130">Registro como controlador predeterminado para ActionIds</span><span class="sxs-lookup"><span data-stu-id="bb12f-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="bb12f-131">En primer lugar, registre el identificador de programa en la subclave AssocActionId adecuada.</span><span class="sxs-lookup"><span data-stu-id="bb12f-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="bb12f-132">Cada subclave AssocActionId representa un verbo o una acción que los usuarios pueden invocar desde la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="bb12f-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="bb12f-133">En este ejemplo, la aplicación se registra para el ZipSelection ActionID para extender el botón "extraer todo" en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="bb12f-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="bb12f-134">Una vez completado el registro, debe registrarse para controlar los protocolos de la manera habitual, tal como se describe en [programas predeterminados](default-programs.md).</span><span class="sxs-lookup"><span data-stu-id="bb12f-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 




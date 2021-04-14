---
description: La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres del shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Mostrar una vista de Self-Contained de una extensión de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985663"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="ff3d8-103">Mostrar una vista de Self-Contained de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff3d8-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="ff3d8-104">La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="ff3d8-105">Cuando se crea un punto de Unión, como se describe en [especificar la ubicación de una extensión de espacio de nombres](nse-junction.md), el explorador de Windows permite a los usuarios navegar dentro y fuera de la extensión de espacio de nombres como cualquier otra carpeta.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="ff3d8-106">Sin embargo, también es posible usar el explorador de Windows para mostrar solo el contenido de la extensión de espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="ff3d8-107">Esta opción de presentación se denomina a veces *vista con raíz*.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="ff3d8-108">Aunque no se usa habitualmente, las vistas con raíz podrían ser preferibles a las vistas normales de algunos tipos de extensiones.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="ff3d8-109">Con una vista con raíz, se crea una nueva instancia del explorador de Windows que muestra el contenido de la extensión como un espacio de nombres independiente.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="ff3d8-110">La vista de árbol de una vista con raíz muestra solo las carpetas que forman parte de la extensión.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="ff3d8-111">Los usuarios no pueden navegar desde una vista con raíz hasta otras partes del espacio de nombres del shell.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="ff3d8-112">Las extensiones se implementan de la misma manera para las vistas con raíz que para las vistas normales.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="ff3d8-113">La única diferencia radica en la forma en que el explorador de Windows muestra el contenido de la extensión.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="ff3d8-114">Incluso es posible tener vistas normales y de raíz de la misma extensión.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="ff3d8-115">Para abrir una vista de una extensión, debe iniciar una instancia de Explorer.exe con una marca/root.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="ff3d8-116">Hay varias maneras de iniciar una vista con raíz, en función de la naturaleza de la extensión.</span><span class="sxs-lookup"><span data-stu-id="ff3d8-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="ff3d8-117">Cómo usar un punto de Unión para abrir una vista con raíz</span><span class="sxs-lookup"><span data-stu-id="ff3d8-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="ff3d8-118">Cómo usar un archivo de acceso directo para abrir una vista con raíz</span><span class="sxs-lookup"><span data-stu-id="ff3d8-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="ff3d8-119">Cómo mostrar una vista raíz de un archivo</span><span class="sxs-lookup"><span data-stu-id="ff3d8-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 




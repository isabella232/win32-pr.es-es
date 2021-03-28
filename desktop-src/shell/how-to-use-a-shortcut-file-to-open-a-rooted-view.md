---
description: Puede iniciar una vista con raíz de un punto de unión a través de un archivo de acceso directo en ese punto de Unión.
title: Cómo abrir una vista con raíz de un punto de unión a través de un archivo de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb83a6628b0dcffdf7d3bad66a25fc671c1feea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276742"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="ed0a7-103">Cómo abrir una vista con raíz de un punto de unión a través de un archivo de acceso directo</span><span class="sxs-lookup"><span data-stu-id="ed0a7-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="ed0a7-104">Puede iniciar una vista con raíz de un punto de unión a través de un [archivo de acceso directo](./links.md) en ese punto de Unión.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="ed0a7-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ed0a7-105">Instructions</span></span>


<span data-ttu-id="ed0a7-106">Establezca la línea de destino del archivo de acceso directo en Explorer.exe con una marca/root.</span><span class="sxs-lookup"><span data-stu-id="ed0a7-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="ed0a7-107">La forma exacta del comando depende de la ubicación del punto de Unión:</span><span class="sxs-lookup"><span data-stu-id="ed0a7-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="ed0a7-108">Si el punto de Unión es una subcarpeta del escritorio, use:</span><span class="sxs-lookup"><span data-stu-id="ed0a7-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="ed0a7-109">Si el punto de Unión es una carpeta del sistema de archivos, use:</span><span class="sxs-lookup"><span data-stu-id="ed0a7-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="ed0a7-110">Si el punto de Unión es una subcarpeta de una carpeta virtual del sistema, use:</span><span class="sxs-lookup"><span data-stu-id="ed0a7-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="ed0a7-111">Las carpetas virtuales del sistema que pueden contener puntos de Unión tienen los siguientes identificadores de clase (CLSID):</span><span class="sxs-lookup"><span data-stu-id="ed0a7-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    |                   |                                        |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="ed0a7-112">Mi PC</span><span class="sxs-lookup"><span data-stu-id="ed0a7-112">My Computer</span></span>       | <span data-ttu-id="ed0a7-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="ed0a7-113">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="ed0a7-114">Mis sitios de red</span><span class="sxs-lookup"><span data-stu-id="ed0a7-114">My Network Places</span></span> | <span data-ttu-id="ed0a7-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="ed0a7-115">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="ed0a7-116">Panel de control</span><span class="sxs-lookup"><span data-stu-id="ed0a7-116">Control Panel</span></span>     | <span data-ttu-id="ed0a7-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="ed0a7-117">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="ed0a7-118">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="ed0a7-118">Internet Explorer</span></span> | <span data-ttu-id="ed0a7-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="ed0a7-119">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="ed0a7-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed0a7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed0a7-121">Especificar la ubicación de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed0a7-121">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="ed0a7-122">Cómo abrir una vista con raíz de un punto de unión a través del registro</span><span class="sxs-lookup"><span data-stu-id="ed0a7-122">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 

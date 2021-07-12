---
description: Puede iniciar una vista con raíz de un punto de unión a través de un archivo de acceso directo a ese punto de unión.
title: Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52096f0dbbcebadb60e2612f0304ed497199b2ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581613"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-a-shortcut-file"></a><span data-ttu-id="aa143-103">Cómo abrir una vista raíz de un punto de unión a través de un archivo de acceso directo</span><span class="sxs-lookup"><span data-stu-id="aa143-103">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>

<span data-ttu-id="aa143-104">Puede iniciar una vista con raíz de un punto de unión a través de un archivo [de acceso directo](./links.md) a ese punto de unión.</span><span class="sxs-lookup"><span data-stu-id="aa143-104">You can launch a rooted view of a junction point through a [shortcut file](./links.md) to that junction point.</span></span>

## <a name="instructions"></a><span data-ttu-id="aa143-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="aa143-105">Instructions</span></span>


<span data-ttu-id="aa143-106">Establezca la línea Destino del archivo de acceso directo en Explorer.exe con una marca /root.</span><span class="sxs-lookup"><span data-stu-id="aa143-106">Set the shortcut file's Target line to Explorer.exe with a /root flag.</span></span> <span data-ttu-id="aa143-107">La forma exacta del comando depende de la ubicación del punto de unión:</span><span class="sxs-lookup"><span data-stu-id="aa143-107">The exact form of the command depends on the location of the junction point:</span></span>

-   <span data-ttu-id="aa143-108">Si el punto de unión es una subcarpeta del escritorio, use:</span><span class="sxs-lookup"><span data-stu-id="aa143-108">If the junction point is a subfolder of the Desktop, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Extension CLSID}
    ```

-   <span data-ttu-id="aa143-109">Si el punto de unión es una carpeta del sistema de archivos, use:</span><span class="sxs-lookup"><span data-stu-id="aa143-109">If the junction point is a file system folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,[Fully qualified path to the folder]
    ```

-   <span data-ttu-id="aa143-110">Si el punto de unión es una subcarpeta de una carpeta virtual del sistema, use:</span><span class="sxs-lookup"><span data-stu-id="aa143-110">If the junction point is a subfolder of a system virtual folder, use:</span></span>

    ``` syntax
    Explorer.exe /e,/root,::{Folder CLSID}\::{Extension CLSID}
    ```

    <span data-ttu-id="aa143-111">Las carpetas virtuales del sistema que pueden contener puntos de unión tienen los siguientes identificadores de clase (CLID):</span><span class="sxs-lookup"><span data-stu-id="aa143-111">The system virtual folders that can contain junction points have the following class identifiers (CLSIDs):</span></span>

    

    | <span data-ttu-id="aa143-112">Carpeta del sistema</span><span class="sxs-lookup"><span data-stu-id="aa143-112">System folder</span></span>     | <span data-ttu-id="aa143-113">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="aa143-113">Class identifier</span></span>                       |
    |-------------------|----------------------------------------|
    | <span data-ttu-id="aa143-114">Mi PC</span><span class="sxs-lookup"><span data-stu-id="aa143-114">My Computer</span></span>       | <span data-ttu-id="aa143-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="aa143-115">{20D04FE0-3AEA-1069-A2D8-08002B30309D}</span></span> |
    | <span data-ttu-id="aa143-116">Mis sitios de red</span><span class="sxs-lookup"><span data-stu-id="aa143-116">My Network Places</span></span> | <span data-ttu-id="aa143-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="aa143-117">{208D2C60-3AEA-1069-A2D7-08002B30309D}</span></span> |
    | <span data-ttu-id="aa143-118">Panel de control</span><span class="sxs-lookup"><span data-stu-id="aa143-118">Control Panel</span></span>     | <span data-ttu-id="aa143-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="aa143-119">{21EC2020-3AEA-1069-A2DD-08002B30309D}</span></span> |
    | <span data-ttu-id="aa143-120">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="aa143-120">Internet Explorer</span></span> | <span data-ttu-id="aa143-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="aa143-121">{871C5380-42A0-1069-A2EA-08002B30309D}</span></span> |

    

     

## <a name="related-topics"></a><span data-ttu-id="aa143-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa143-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa143-123">Especificar la ubicación de una extensión de espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa143-123">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="aa143-124">Cómo abrir una vista con raíz de un punto de unión a través del Registro</span><span class="sxs-lookup"><span data-stu-id="aa143-124">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> </dl>

 

 

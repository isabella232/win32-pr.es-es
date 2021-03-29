---
description: Una extensión de complemento de datos adjuntos debe agregarse en el nodo servicios cuando un usuario expande ese nodo.
ms.assetid: af853c29-11c2-4fd0-ad81-80aebeb74cc3
title: Agregar un nodo de extensión del complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2604a58284af7bc55ff57ae114bc77d8f0cd42ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815739"
---
# <a name="adding-an-attachment-snap-in-extension-node"></a><span data-ttu-id="12dd0-103">Agregar un nodo de extensión del complemento de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="12dd0-103">Adding an Attachment Snap-in Extension Node</span></span>

<span data-ttu-id="12dd0-104">Una extensión de complemento de datos adjuntos debe agregarse en el nodo servicios cuando un usuario expande ese nodo.</span><span class="sxs-lookup"><span data-stu-id="12dd0-104">An attachment snap-in extension must add itself under the Services node when that node is expanded by a user.</span></span>

<span data-ttu-id="12dd0-105">Cuando un usuario expande el nodo servicios de uno de los complementos de configuración de seguridad, MMC usa [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) y el \_ mensaje de notificación expandir MMCN para notificar al complemento configuración de seguridad, además de todas sus extensiones.</span><span class="sxs-lookup"><span data-stu-id="12dd0-105">When a user expands the Services node under one of the Security Configuration snap-ins, MMC uses [**IComponentData::Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) and the MMCN\_EXPAND notification message to notify the Security Configuration snap-in, plus all its extensions.</span></span>

<span data-ttu-id="12dd0-106">A continuación, el complemento configuración de seguridad extrae su formato interno de *lpDataObject*, que se pasa desde el marco principal de MMC como tipo **lpDataObject**.</span><span class="sxs-lookup"><span data-stu-id="12dd0-106">The Security Configuration snap-in then extracts its internal format from the *lpDataObject*, which is passed in from the MMC main framework as type **LPDATAOBJECT**.</span></span> <span data-ttu-id="12dd0-107">Detiene el procesamiento cuando ve el tipo de nodo servicios.</span><span class="sxs-lookup"><span data-stu-id="12dd0-107">It stops processing when it sees the Services node type.</span></span> <span data-ttu-id="12dd0-108">A continuación, la extensión del complemento de datos adjuntos extrae el tipo de nodo de *lpDataObject*.</span><span class="sxs-lookup"><span data-stu-id="12dd0-108">The attachment snap-in extension then extracts the node type from the *lpDataObject*.</span></span> <span data-ttu-id="12dd0-109">Si el tipo de nodo es uno de los tipos de nodo definidos del servicio, la extensión del complemento de datos adjuntos inserta sus nodos raíz en el nodo primario especificado.</span><span class="sxs-lookup"><span data-stu-id="12dd0-109">If the node type is one of the service's defined node types, the attachment snap-in extension inserts its root nodes under the specified parent node.</span></span>

<span data-ttu-id="12dd0-110">Tenga en cuenta que en este ejemplo, ExtractNodeType, es una función privada que implementa la extensión.</span><span class="sxs-lookup"><span data-stu-id="12dd0-110">Note that in this example, ExtractNodeType, is a private function that the extension implements.</span></span> <span data-ttu-id="12dd0-111">La extensión examina el objeto de datos para obtener el tipo de nodo.</span><span class="sxs-lookup"><span data-stu-id="12dd0-111">The extension examines the data object to get the node type.</span></span> <span data-ttu-id="12dd0-112">No se muestra la implementación de ExtractNodeType.</span><span class="sxs-lookup"><span data-stu-id="12dd0-112">The implementation of ExtractNodeType is not shown.</span></span>


```C++
//  Detect which extension node to expand.
GUID* nodeType = ExtractNodeType(lpdataObject);

if (NULL == nodeType)
{
  return S_OK;
}

if (TRUE == ::IsEqualGUID(*nodeType, cNodetypeSceTemplateServices))
{
  folderType = ATTACHMENT_STATIC;  // defined by attachment writer
}

else if (TRUE == ::IsEqualGUID
    (*nodeType, cNodetypeSceAnalysisServices))
{
  folderType = ATTACHMENT_STATIC_ANALYSIS;
               // defined by attachment writer
}

//  Free resources.
::GlobalFree(reinterpret_cast<HANDLE>(nodeType));

//  Add service attachment root node and remember it as the
//  root of the SMB extension namespace.
//  ...
```



 

 

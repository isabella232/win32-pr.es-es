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
# <a name="adding-an-attachment-snap-in-extension-node"></a>Agregar un nodo de extensión del complemento de datos adjuntos

Una extensión de complemento de datos adjuntos debe agregarse en el nodo servicios cuando un usuario expande ese nodo.

Cuando un usuario expande el nodo servicios de uno de los complementos de configuración de seguridad, MMC usa [**IComponentData:: Notify**](/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify) y el \_ mensaje de notificación expandir MMCN para notificar al complemento configuración de seguridad, además de todas sus extensiones.

A continuación, el complemento configuración de seguridad extrae su formato interno de *lpDataObject*, que se pasa desde el marco principal de MMC como tipo **lpDataObject**. Detiene el procesamiento cuando ve el tipo de nodo servicios. A continuación, la extensión del complemento de datos adjuntos extrae el tipo de nodo de *lpDataObject*. Si el tipo de nodo es uno de los tipos de nodo definidos del servicio, la extensión del complemento de datos adjuntos inserta sus nodos raíz en el nodo primario especificado.

Tenga en cuenta que en este ejemplo, ExtractNodeType, es una función privada que implementa la extensión. La extensión examina el objeto de datos para obtener el tipo de nodo. No se muestra la implementación de ExtractNodeType.


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



 

 

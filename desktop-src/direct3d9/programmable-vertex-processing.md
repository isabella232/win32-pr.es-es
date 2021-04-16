---
description: Cuando se usa un sombreador de vértices programado, los elementos actualizados en el búfer de vértice de destino se controlan mediante el programa de función de sombreador.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Procesamiento de vértices programable (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696084"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Procesamiento de vértices programable (Direct3D 9)

Cuando se usa un sombreador de vértices programado, los elementos actualizados en el búfer de vértice de destino se controlan mediante el programa de función de sombreador. Cuando la aplicación escribe en uno de los registros de vértice de destino, se actualiza el elemento correspondiente dentro de cada vértice del búfer de vértice de destino. Los elementos del búfer de vértice de destino en los que no se escribe la aplicación no se modifican. [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) producirá un error si la aplicación escribe en elementos que no están presentes en el búfer de vértices de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 

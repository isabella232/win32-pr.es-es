---
description: Cuando se usa un sombreador de vértices programado, los elementos actualizados en el búfer de vértices de destino se controlan mediante el programa de función de sombreador.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Procesamiento de vértices programables (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118601"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Procesamiento de vértices programables (Direct3D 9)

Cuando se usa un sombreador de vértices programado, los elementos actualizados en el búfer de vértices de destino se controlan mediante el programa de función de sombreador. Cuando la aplicación escribe en uno de los registros de vértices de destino, se actualiza el elemento correspondiente dentro de cada vértice del búfer de vértices de destino. No se modifican los elementos del búfer de vértices de destino que no se escriben en la aplicación. [**IDirect3DDevice9::P rocessVertices producirá**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) un error si la aplicación escribe en elementos que no están presentes en el búfer de vértices de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de vértices](vertex-buffers.md)
</dt> </dl>

 

 

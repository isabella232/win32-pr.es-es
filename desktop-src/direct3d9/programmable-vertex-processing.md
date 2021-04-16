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
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="09c95-103">Procesamiento de vértices programable (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="09c95-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="09c95-104">Cuando se usa un sombreador de vértices programado, los elementos actualizados en el búfer de vértice de destino se controlan mediante el programa de función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="09c95-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="09c95-105">Cuando la aplicación escribe en uno de los registros de vértice de destino, se actualiza el elemento correspondiente dentro de cada vértice del búfer de vértice de destino.</span><span class="sxs-lookup"><span data-stu-id="09c95-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="09c95-106">Los elementos del búfer de vértice de destino en los que no se escribe la aplicación no se modifican.</span><span class="sxs-lookup"><span data-stu-id="09c95-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="09c95-107">[**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) producirá un error si la aplicación escribe en elementos que no están presentes en el búfer de vértices de destino.</span><span class="sxs-lookup"><span data-stu-id="09c95-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09c95-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09c95-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c95-109">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="09c95-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 

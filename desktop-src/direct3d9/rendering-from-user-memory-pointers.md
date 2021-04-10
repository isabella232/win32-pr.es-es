---
description: Un conjunto secundario de interfaces de representación permite pasar datos de vértices e índices directamente desde punteros de memoria de usuario. Estas interfaces admiten solo una secuencia de datos de vértice. Para obtener más información, vea los temas de referencia siguientes.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Representación de punteros de memoria de usuario (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274745"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a><span data-ttu-id="9e161-105">Representación de punteros de memoria de usuario (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9e161-105">Rendering from User Memory Pointers (Direct3D 9)</span></span>

<span data-ttu-id="9e161-106">Un conjunto secundario de interfaces de representación permite pasar datos de vértices e índices directamente desde punteros de memoria de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e161-106">A secondary set of rendering interfaces supports passing vertex and index data directly from user memory pointers.</span></span> <span data-ttu-id="9e161-107">Estas interfaces admiten solo una secuencia de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="9e161-107">These interfaces support a single stream of vertex data only.</span></span> <span data-ttu-id="9e161-108">Para obtener más información, vea los temas de referencia siguientes.</span><span class="sxs-lookup"><span data-stu-id="9e161-108">For more information, see the following reference topics.</span></span>

-   [<span data-ttu-id="9e161-109">**IDirect3DDevice9::D rawPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9e161-109">**IDirect3DDevice9::DrawPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [<span data-ttu-id="9e161-110">**IDirect3DDevice9::D rawIndexedPrimitiveUP**</span><span class="sxs-lookup"><span data-stu-id="9e161-110">**IDirect3DDevice9::DrawIndexedPrimitiveUP**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

<span data-ttu-id="9e161-111">Estos métodos se representan con datos especificados por punteros de memoria de usuario, en lugar de búferes de índice y vértices.</span><span class="sxs-lookup"><span data-stu-id="9e161-111">These methods render with data specified by user memory pointers, instead of vertex and index buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e161-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e161-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e161-113">Representación de primitivas</span><span class="sxs-lookup"><span data-stu-id="9e161-113">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 

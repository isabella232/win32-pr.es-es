---
description: El término blit es una abreviatura para &\# 0034; transferencia de bloque de bits, &\# 0034; que es el proceso de transferir bloques de datos de un lugar de memoria a otro.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copiar superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696120"
---
# <a name="copying-surfaces-direct3d-9"></a><span data-ttu-id="773a6-103">Copiar superficies (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="773a6-103">Copying Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="773a6-104">El término blit es una abreviatura de "transferencia de bloque de bits", que es el proceso de transferir bloques de datos de un lugar de memoria a otro.</span><span class="sxs-lookup"><span data-stu-id="773a6-104">The term blit is shorthand for "bit block transfer," which is the process of transferring blocks of data from one place in memory to another.</span></span> <span data-ttu-id="773a6-105">La interfaz de controlador de dispositivo (DDI) de blitting se sigue usando en Direct3D 9 como el mecanismo principal para mover grandes rectángulos de píxeles en cada fotograma, el mecanismo detrás del IDirect3DDevice9 orientado a copia [**::P método reenviado**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="773a6-105">The blitting device driver interface (DDI) continues to be used in Direct3D 9 as the primary mechanism for moving large rectangles of pixels on a per-frame basis, the mechanism behind the copy-oriented [**IDirect3DDevice9::Present**](/windows/desktop/api) method.</span></span> <span data-ttu-id="773a6-106">El transporte de material gráfico en la operación de blit lo realiza el método [**IDirect3DDevice9:: UpdateTexture**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="773a6-106">The transportation of artwork in the blit operation is performed by the [**IDirect3DDevice9::UpdateTexture**](/windows/desktop/api) method.</span></span> <span data-ttu-id="773a6-107">También se puede copiar material gráfico en Direct3D 9 mediante el método [**IDirect3DDevice9:: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , que copia un subconjunto rectangular de píxeles.</span><span class="sxs-lookup"><span data-stu-id="773a6-107">Artwork can also be copied in Direct3D 9 by using the [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) method, which copies a rectangular subset of pixels.</span></span>

> [!Note]  
> <span data-ttu-id="773a6-108">Direct3D 9 proporciona funciones de D3DX que permiten cargar ilustraciones desde archivos, aplicar la conversión de colores y cambiar el tamaño de la ilustración.</span><span class="sxs-lookup"><span data-stu-id="773a6-108">Direct3D 9 provides D3DX functions that enable you to load artwork from files, apply color conversion, and resize artwork.</span></span> <span data-ttu-id="773a6-109">Para obtener más información sobre las funciones disponibles, consulte [funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span><span class="sxs-lookup"><span data-stu-id="773a6-109">For more information about the available functions see [Texture Functions in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="773a6-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="773a6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773a6-111">Superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="773a6-111">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="773a6-112">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="773a6-112">**IDirect3DDevice9::StretchRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

<span data-ttu-id="773a6-113">**IDirect3DDevice9::StretchRect**</span><span class="sxs-lookup"><span data-stu-id="773a6-113">**IDirect3DDevice9::StretchRect**</span></span>
</dt> </dl>

 

 

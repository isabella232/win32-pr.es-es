---
description: Direct3D mantiene una lista de hasta ocho texturas actuales. Combina estas texturas en todas las representaciones de primitivas. Solo las texturas creadas como punteros de interfaz de textura se pueden usar en el conjunto de texturas actuales.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Asignar las texturas actuales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496739"
---
# <a name="assigning-the-current-textures-direct3d-9"></a><span data-ttu-id="49638-105">Asignar las texturas actuales (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="49638-105">Assigning the Current Textures (Direct3D 9)</span></span>

<span data-ttu-id="49638-106">Direct3D mantiene una lista de hasta ocho texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="49638-106">Direct3D maintains a list of up to eight current textures.</span></span> <span data-ttu-id="49638-107">Combina estas texturas en todas las representaciones de primitivas.</span><span class="sxs-lookup"><span data-stu-id="49638-107">It blends these textures onto all the primitive it renders.</span></span> <span data-ttu-id="49638-108">Solo las texturas creadas como punteros de interfaz de textura se pueden usar en el conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="49638-108">Only textures created as texture interface pointers can be used in the set of current textures.</span></span>

<span data-ttu-id="49638-109">Las aplicaciones llaman al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asignar texturas al conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="49638-109">Applications call the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method to assign textures into the set of current textures.</span></span> <span data-ttu-id="49638-110">El primer parámetro debe ser un número en el intervalo de 0-7, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="49638-110">The first parameter must be a number in the range of 0-7, inclusive.</span></span> <span data-ttu-id="49638-111">Pase el puntero de la interfaz de textura como segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="49638-111">Pass the texture interface pointer as the second parameter.</span></span>

<span data-ttu-id="49638-112">En el ejemplo de código de C++ siguiente se muestra cómo se puede asignar una textura al conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="49638-112">The following C++ code example demonstrates how a texture can be assigned to the set of current textures.</span></span>


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> <span data-ttu-id="49638-113">Los dispositivos de software no admiten la asignación de una textura a más de una fase de textura a la vez.</span><span class="sxs-lookup"><span data-stu-id="49638-113">Software devices do not support assigning a texture to more than one texture stage at a time.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="49638-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49638-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49638-115">Combinación de texturas</span><span class="sxs-lookup"><span data-stu-id="49638-115">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 

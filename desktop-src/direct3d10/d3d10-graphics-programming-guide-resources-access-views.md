---
description: En Direct3D 10, se accede a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Vistas de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335589"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="c7043-103">Vistas de textura (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c7043-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="c7043-104">En Direct3D 10, se accede a los recursos de textura con una vista, que es un mecanismo para la interpretación de hardware de un recurso en memoria.</span><span class="sxs-lookup"><span data-stu-id="c7043-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="c7043-105">Una vista permite que una fase de canalización determinada acceda solo a los [subrecursos](d3d10-graphics-programming-guide-resources-types.md) que necesita, en la representación deseada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7043-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="c7043-106">Una vista admite la noción de un recurso sin tipo.</span><span class="sxs-lookup"><span data-stu-id="c7043-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="c7043-107">Un recurso sin tipo es un recurso creado con un tamaño específico, pero no un tipo de datos específico.</span><span class="sxs-lookup"><span data-stu-id="c7043-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="c7043-108">Los datos se interpretan dinámicamente cuando se enlazan a la canalización.</span><span class="sxs-lookup"><span data-stu-id="c7043-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="c7043-109">En la ilustración siguiente se muestra un ejemplo de enlace de una matriz de texturas 2D con 6 texturas como un recurso de sombreador mediante la creación de una vista de recursos de sombreador para él.</span><span class="sxs-lookup"><span data-stu-id="c7043-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="c7043-110">A continuación, el recurso se dirige como una matriz de texturas.</span><span class="sxs-lookup"><span data-stu-id="c7043-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="c7043-111">(Nota: Un subrecurso no se puede enlazar como entrada y salida a la canalización simultáneamente).</span><span class="sxs-lookup"><span data-stu-id="c7043-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![ilustración de una matriz de texturas con seis texturas](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="c7043-113">Cuando se usa una matriz de texturas 2D como destino de representación, el recurso se puede ver como una matriz de texturas 2D (6 en este ejemplo) con niveles de mapa mip (3 en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="c7043-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="c7043-114">Cree un objeto de vista para un destino de representación mediante una llamada a CreateRenderTargetView.</span><span class="sxs-lookup"><span data-stu-id="c7043-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="c7043-115">A continuación, llame a OMSetRenderTargets para establecer la vista de destino de representación en la canalización.</span><span class="sxs-lookup"><span data-stu-id="c7043-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="c7043-116">Represente en los destinos de representación llamando a Draw y usando RenderTargetArrayIndex para indexar en la textura adecuada de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c7043-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="c7043-117">Puede usar un subcurso (un nivel mipmap, combinación de índice de matriz) para enlazar a cualquier matriz de subrecursos.</span><span class="sxs-lookup"><span data-stu-id="c7043-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="c7043-118">Por lo tanto, puede enlazar al segundo nivel de mapa mip y actualizar solo este nivel de mapa mip determinado si lo desea, como en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7043-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![ilustración del enlace solo al segundo nivel de mapa mip de una matriz de textura](images/d3d10-cube-texture-faces-subresource.png)



<span data-ttu-id="c7043-120">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="c7043-120">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="c7043-121">En Direct3D 10, ya no se enlaza un recurso directamente a la canalización, se crea una vista de un recurso y, a continuación, se establece la vista en la canalización.</span><span class="sxs-lookup"><span data-stu-id="c7043-121">In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="c7043-122">Esto permite que la validación y asignación en el tiempo de ejecución y el controlador se produzcan en la creación de vistas, lo que minimiza la comprobación de tipos en tiempo de enlace.</span><span class="sxs-lookup"><span data-stu-id="c7043-122">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="c7043-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7043-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7043-124">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c7043-124">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 





---
description: Las enumeraciones siguientes se utilizan para especificar información sobre cómo se crean y se obtiene acceso a los recursos durante la representación.
ms.assetid: c986b22c-2960-4571-98bc-028c9f41ec65
title: Enumeraciones de recursos (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ae6e115fe8ae9a731e5778b986940cb17a915d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080298"
---
# <a name="resource-enumerations-direct3d-10-graphics"></a><span data-ttu-id="b924a-103">Enumeraciones de recursos (gráficos de Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b924a-103">Resource Enumerations (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="b924a-104">Las enumeraciones siguientes se utilizan para especificar información sobre cómo se crean y se obtiene acceso a los recursos durante la representación.</span><span class="sxs-lookup"><span data-stu-id="b924a-104">The following enumerations are used to specify information about how resources are created and accessed during rendering.</span></span>



| <span data-ttu-id="b924a-105">Enumeración</span><span class="sxs-lookup"><span data-stu-id="b924a-105">Enumeration</span></span>                                                     | <span data-ttu-id="b924a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b924a-106">Description</span></span>                                                                                                               |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b924a-107">**D3D10 \_ marca de enlace \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-107">**D3D10\_BIND\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)                    | <span data-ttu-id="b924a-108">Identifica cómo usará un recurso la canalización y determina a qué fases de canalización se puede enlazar un recurso.</span><span class="sxs-lookup"><span data-stu-id="b924a-108">Identifies how a resource will be used by the pipeline and determines which pipeline stage(s) a resource can be bound to.</span></span> |
| [<span data-ttu-id="b924a-109">**\_Marca de \_ acceso de CPU de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-109">**D3D10\_CPU\_ACCESS\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)       | <span data-ttu-id="b924a-110">Especifica los tipos de acceso de CPU permitidos para un recurso.</span><span class="sxs-lookup"><span data-stu-id="b924a-110">Specifies the types of CPU access allowed for a resource.</span></span>                                                                 |
| [<span data-ttu-id="b924a-111">**D3D10 \_ \_ dimensión DSV**</span><span class="sxs-lookup"><span data-stu-id="b924a-111">**D3D10\_DSV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_dsv_dimension)            | <span data-ttu-id="b924a-112">Especifica cómo obtener acceso a un recurso que se usa en una vista de galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="b924a-112">Specifies how to access a resource that is used in a depth-stencil view.</span></span>                                                  |
| [<span data-ttu-id="b924a-113">**\_Mapa D3D10**</span><span class="sxs-lookup"><span data-stu-id="b924a-113">**D3D10\_MAP**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map)                                 | <span data-ttu-id="b924a-114">Identifica un recurso que se va a asignar para lectura y escritura de la CPU.</span><span class="sxs-lookup"><span data-stu-id="b924a-114">Identifies a resource to be mapped for reading and writing by the CPU.</span></span>                                                    |
| [<span data-ttu-id="b924a-115">**D3D10 \_ marca de mapa \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-115">**D3D10\_MAP\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_map_flag)                      | <span data-ttu-id="b924a-116">Especifica cómo debe responder la CPU a los métodos de asignación cuando la GPU todavía no ha finalizado con el recurso.</span><span class="sxs-lookup"><span data-stu-id="b924a-116">Specifies how the CPU should respond to any Map methods when the GPU is not yet finished with the resource.</span></span>               |
| [<span data-ttu-id="b924a-117">**\_Dimensión de recursos D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-117">**D3D10\_RESOURCE\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)  | <span data-ttu-id="b924a-118">Identifica el tipo de recurso que está en uso.</span><span class="sxs-lookup"><span data-stu-id="b924a-118">Identifies the type of resource that is in use.</span></span>                                                                           |
| [<span data-ttu-id="b924a-119">**\_Marca de recursos \_ varios \_ de D3D10**</span><span class="sxs-lookup"><span data-stu-id="b924a-119">**D3D10\_RESOURCE\_MISC\_FLAG**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag) | <span data-ttu-id="b924a-120">Identifica las opciones de creación de recursos menos comunes.</span><span class="sxs-lookup"><span data-stu-id="b924a-120">Identifies less common resource creation options.</span></span>                                                                         |
| [<span data-ttu-id="b924a-121">**D3D10 \_ dimensión de RTV \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-121">**D3D10\_RTV\_DIMENSION**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_rtv_dimension)            | <span data-ttu-id="b924a-122">Especifica cómo obtener acceso a un recurso usado en una vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="b924a-122">Specifies how to access a resource used in a render target view.</span></span>                                                          |
| [<span data-ttu-id="b924a-123">**Uso de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="b924a-123">**D3D10\_USAGE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)                             | <span data-ttu-id="b924a-124">Identifica cómo se espera que un recurso se lea y escriba en la CPU o la GPU.</span><span class="sxs-lookup"><span data-stu-id="b924a-124">Identifies how a resource is expected to be read and written by the CPU and/or the GPU.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="b924a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b924a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b924a-126">Referencia de recursos</span><span class="sxs-lookup"><span data-stu-id="b924a-126">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 




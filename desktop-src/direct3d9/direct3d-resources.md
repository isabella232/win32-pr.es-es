---
description: Los recursos son las texturas y los búferes que se usan para representar una escena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Recursos de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152328"
---
# <a name="direct3d-resources-direct3d-9"></a><span data-ttu-id="10895-103">Recursos de Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-103">Direct3D Resources (Direct3D 9)</span></span>

<span data-ttu-id="10895-104">Los recursos son las texturas y los búferes que se usan para representar una escena.</span><span class="sxs-lookup"><span data-stu-id="10895-104">Resources are the textures and buffers that are used to render a scene.</span></span> <span data-ttu-id="10895-105">Las aplicaciones necesitan crear, cargar, copiar y usar recursos.</span><span class="sxs-lookup"><span data-stu-id="10895-105">Applications need to create, load, copy, and use resources.</span></span> <span data-ttu-id="10895-106">En esta sección se proporciona una breve introducción a los recursos y los pasos y métodos que usan las aplicaciones al trabajar con recursos.</span><span class="sxs-lookup"><span data-stu-id="10895-106">This section gives a brief introduction to resources and the steps and methods used by applications when working with resources.</span></span>

<span data-ttu-id="10895-107">Todos los recursos, incluidos los recursos de Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) y [**IDirect3DVertexBuffer9**](/windows/desktop/api), se heredan de la interfaz [**IDirect3DResource9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="10895-107">All resources, including the geometry resources [**IDirect3DIndexBuffer9**](/windows/desktop/api) and [**IDirect3DVertexBuffer9**](/windows/desktop/api), inherit from the [**IDirect3DResource9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="10895-108">Los recursos de textura, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)y [**IDirect3DVolumeTexture9**](/windows/desktop/api), también heredan de la interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .</span><span class="sxs-lookup"><span data-stu-id="10895-108">The texture resources, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api), and [**IDirect3DVolumeTexture9**](/windows/desktop/api), also inherit from the [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface.</span></span>

-   [<span data-ttu-id="10895-109">Propiedades de recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-109">Resource Properties (Direct3D 9)</span></span>](resource-properties.md)
-   [<span data-ttu-id="10895-110">Manipular recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-110">Manipulating Resources (Direct3D 9)</span></span>](manipulating-resources.md)
-   [<span data-ttu-id="10895-111">Bloquear recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-111">Locking Resources (Direct3D 9)</span></span>](locking-resources.md)
-   [<span data-ttu-id="10895-112">Relaciones de recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-112">Resource Relationships (Direct3D 9)</span></span>](resource-relationships.md)
-   [<span data-ttu-id="10895-113">Administrar recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-113">Managing Resources (Direct3D 9)</span></span>](managing-resources.md)
-   [<span data-ttu-id="10895-114">Recursos administrados por la aplicación y estrategias de asignación (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-114">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [<span data-ttu-id="10895-115">Búferes de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-115">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
-   [<span data-ttu-id="10895-116">Búferes de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10895-116">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)

## <a name="related-topics"></a><span data-ttu-id="10895-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10895-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10895-118">Introducción</span><span class="sxs-lookup"><span data-stu-id="10895-118">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 

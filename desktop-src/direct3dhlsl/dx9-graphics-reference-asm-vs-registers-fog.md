---
title: Registro de niebla
description: Este registro de salida del sombreador de vértices contiene un color de niebla por vértice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983711"
---
# <a name="fog-register"></a><span data-ttu-id="8af5a-103">Registro de niebla</span><span class="sxs-lookup"><span data-stu-id="8af5a-103">Fog Register</span></span>

<span data-ttu-id="8af5a-104">Este registro de salida del sombreador de vértices contiene un color de niebla por vértice.</span><span class="sxs-lookup"><span data-stu-id="8af5a-104">This vertex shader output register contains a per-vertex fog color.</span></span>

<span data-ttu-id="8af5a-105">Un registro consta de propiedades que determinan el comportamiento de cada registro.</span><span class="sxs-lookup"><span data-stu-id="8af5a-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="8af5a-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8af5a-106">Property</span></span>        | <span data-ttu-id="8af5a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8af5a-107">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af5a-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="8af5a-108">Name</span></span>            | <span data-ttu-id="8af5a-109">oFog</span><span class="sxs-lookup"><span data-stu-id="8af5a-109">oFog</span></span>                                                                                            |
| <span data-ttu-id="8af5a-110">Count</span><span class="sxs-lookup"><span data-stu-id="8af5a-110">Count</span></span>           | <span data-ttu-id="8af5a-111">Un vector, del que solo se puede usar un componente y que debe especificar la máscara de componente.</span><span class="sxs-lookup"><span data-stu-id="8af5a-111">One vector, of which only one component can be used and must be specified by the component mask</span></span> |
| <span data-ttu-id="8af5a-112">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="8af5a-112">I/O permissions</span></span> | <span data-ttu-id="8af5a-113">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="8af5a-113">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="8af5a-114">El valor de niebla de salida se registra.</span><span class="sxs-lookup"><span data-stu-id="8af5a-114">The output fog value registers.</span></span> <span data-ttu-id="8af5a-115">El valor es el factor de niebla que se va a interpolar y, a continuación, enrutar a la tabla de niebla.</span><span class="sxs-lookup"><span data-stu-id="8af5a-115">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="8af5a-116">Solo se usa el componente x escalar de la niebla.</span><span class="sxs-lookup"><span data-stu-id="8af5a-116">Only the scalar x-component of the fog is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8af5a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8af5a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8af5a-118">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="8af5a-118">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





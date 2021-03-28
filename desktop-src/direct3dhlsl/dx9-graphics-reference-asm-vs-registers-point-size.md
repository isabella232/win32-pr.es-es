---
title: Registro de tamaño de punto
description: Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértices.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418612"
---
# <a name="point-size-register"></a><span data-ttu-id="c9772-103">Registro de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="c9772-103">Point Size Register</span></span>

<span data-ttu-id="c9772-104">Este registro de salida del sombreador de vértices contiene datos de tamaño de punto por vértices.</span><span class="sxs-lookup"><span data-stu-id="c9772-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="c9772-105">Versiones del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c9772-105">Vertex shader versions</span></span> | <span data-ttu-id="c9772-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="c9772-106">1\_1</span></span> | <span data-ttu-id="c9772-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9772-107">2\_0</span></span> | <span data-ttu-id="c9772-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c9772-108">2\_sw</span></span> | <span data-ttu-id="c9772-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c9772-109">2\_x</span></span> | <span data-ttu-id="c9772-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c9772-110">3\_0</span></span> | <span data-ttu-id="c9772-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c9772-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="c9772-112">Registro de tamaño de punto</span><span class="sxs-lookup"><span data-stu-id="c9772-112">Point Size Register</span></span>    | <span data-ttu-id="c9772-113">x</span><span class="sxs-lookup"><span data-stu-id="c9772-113">x</span></span>    | <span data-ttu-id="c9772-114">x</span><span class="sxs-lookup"><span data-stu-id="c9772-114">x</span></span>    | <span data-ttu-id="c9772-115">x</span><span class="sxs-lookup"><span data-stu-id="c9772-115">x</span></span>     | <span data-ttu-id="c9772-116">x</span><span class="sxs-lookup"><span data-stu-id="c9772-116">x</span></span>    | <span data-ttu-id="c9772-117">x</span><span class="sxs-lookup"><span data-stu-id="c9772-117">x</span></span>    | <span data-ttu-id="c9772-118">x</span><span class="sxs-lookup"><span data-stu-id="c9772-118">x</span></span>     |



 

<span data-ttu-id="c9772-119">Un registro consta de propiedades que determinan el comportamiento de cada registro.</span><span class="sxs-lookup"><span data-stu-id="c9772-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="c9772-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9772-120">Property</span></span>        | <span data-ttu-id="c9772-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9772-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9772-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9772-122">Name</span></span>            | <span data-ttu-id="c9772-123">Aporta</span><span class="sxs-lookup"><span data-stu-id="c9772-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="c9772-124">Count</span><span class="sxs-lookup"><span data-stu-id="c9772-124">Count</span></span>           | <span data-ttu-id="c9772-125">1 Vector, del que solo se puede usar un componente y debe especificarse mediante la máscara del componente.</span><span class="sxs-lookup"><span data-stu-id="c9772-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="c9772-126">Permisos de e/s</span><span class="sxs-lookup"><span data-stu-id="c9772-126">I/O permissions</span></span> | <span data-ttu-id="c9772-127">De solo escritura.</span><span class="sxs-lookup"><span data-stu-id="c9772-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="c9772-128">Solo se usa el componente x escalar del tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="c9772-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9772-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9772-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9772-130">Registros del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="c9772-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 





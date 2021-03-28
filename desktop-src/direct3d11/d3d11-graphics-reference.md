---
title: Referencia de Direct3D 11
description: En esta sección se describe la API de Direct3D 11.
ms.assetid: c6ec864b-4565-45af-a95f-d1ed1e70a316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd135a17ebf09a4e1db1d431a2f5b69cba624db4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996792"
---
# <a name="direct3d-11-reference"></a><span data-ttu-id="7354b-103">Referencia de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7354b-103">Direct3D 11 Reference</span></span>

<span data-ttu-id="7354b-104">En esta sección se describe la API de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="7354b-104">The Direct3D 11 API is described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7354b-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7354b-105">In this section</span></span>



| <span data-ttu-id="7354b-106">Tema</span><span class="sxs-lookup"><span data-stu-id="7354b-106">Topic</span></span>                                                                            | <span data-ttu-id="7354b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7354b-107">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7354b-108">Referencia básica</span><span class="sxs-lookup"><span data-stu-id="7354b-108">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)<br/>             | <span data-ttu-id="7354b-109">La API de Direct3D define varios elementos principales de la API.</span><span class="sxs-lookup"><span data-stu-id="7354b-109">The Direct3D API defines several core API elements.</span></span><br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="7354b-110">Referencia de capas</span><span class="sxs-lookup"><span data-stu-id="7354b-110">Layer Reference</span></span>](d3d11-graphics-reference-d3d11-layer.md)<br/>           | <span data-ttu-id="7354b-111">La API de Direct3D define varios elementos de la API de capa.</span><span class="sxs-lookup"><span data-stu-id="7354b-111">The Direct3D API defines several layer API elements.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="7354b-112">Referencia de recursos</span><span class="sxs-lookup"><span data-stu-id="7354b-112">Resource Reference</span></span>](d3d11-graphics-reference-resource.md)<br/>           | <span data-ttu-id="7354b-113">La API de Direct3D define varios elementos de API que le ayudarán a crear y administrar recursos.</span><span class="sxs-lookup"><span data-stu-id="7354b-113">The Direct3D API defines several API elements to help you create and manage resources.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="7354b-114">Referencia de los sombreadores</span><span class="sxs-lookup"><span data-stu-id="7354b-114">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)<br/>         | <span data-ttu-id="7354b-115">La API de Direct3D define varios elementos de API que le ayudarán a crear y administrar sombreadores programables.</span><span class="sxs-lookup"><span data-stu-id="7354b-115">The Direct3D API defines several API elements to help you create and manage programmable shaders.</span></span> <span data-ttu-id="7354b-116">Los sombreadores son programas ejecutables que se programan exclusivamente mediante HLSL.</span><span class="sxs-lookup"><span data-stu-id="7354b-116">Shaders are executable programs that are programmed exclusively using HLSL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="7354b-117">Referencia de 10Level9</span><span class="sxs-lookup"><span data-stu-id="7354b-117">10Level9 Reference</span></span>](d3d11-graphics-reference-10level9.md)<br/>           | <span data-ttu-id="7354b-118">En esta sección se especifican las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ de nivel 11 \_ 0 y superior para los métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="7354b-118">This section specifies the differences between each 10Level9 feature level and the D3D\_FEATURE\_LEVEL\_11\_0 and higher feature level for the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods.</span></span><br/>             |
| [<span data-ttu-id="7354b-119">Códigos de retorno de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7354b-119">Direct3D 11 Return Codes</span></span>](d3d11-graphics-reference-returnvalues.md)<br/> | <span data-ttu-id="7354b-120">Códigos de retorno de las funciones de la API.</span><span class="sxs-lookup"><span data-stu-id="7354b-120">The return codes from API functions.</span></span> <br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="7354b-121">Referencia de la versión común</span><span class="sxs-lookup"><span data-stu-id="7354b-121">Common Version Reference</span></span>](d3d11-graphics-reference-d3d11-common.md)<br/> | <span data-ttu-id="7354b-122">La API de Direct3D define varios elementos de API comunes a Direct3D 12, Direct3D 11, Direct3D 10 y Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="7354b-122">The Direct3D API defines several API elements that are common to the Direct3D 12, Direct3D 11, Direct3D 10, and Direct3D 10.1.</span></span> <span data-ttu-id="7354b-123">Puede usar estos elementos de la API en el código para cualquiera de estas versiones de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7354b-123">You can use these API elements in your code for any of these Direct3D versions.</span></span> <span data-ttu-id="7354b-124">Estos elementos de la API se conocen como versiones neutras.</span><span class="sxs-lookup"><span data-stu-id="7354b-124">These API elements are known as version neutral.</span></span><br/> |
| [<span data-ttu-id="7354b-125">Estructuras auxiliares de CD3D11</span><span class="sxs-lookup"><span data-stu-id="7354b-125">CD3D11 Helper Structures</span></span>](cd3d11-helper-classes.md)<br/>                 | <span data-ttu-id="7354b-126">Direct3D 11 define varias estructuras auxiliares que puede usar para crear estructuras de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7354b-126">Direct3D 11 defines several helper structures that you can use to create Direct3D structures.</span></span> <span data-ttu-id="7354b-127">Estas estructuras auxiliares se comportan como clases de C++.</span><span class="sxs-lookup"><span data-stu-id="7354b-127">These helper structures behave like C++ classes.</span></span> <br/>                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="7354b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7354b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7354b-129">Referencia de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7354b-129">Direct3D 11 Reference</span></span>](atoc-d3d11-graphics-reference.md)
</dt> <dt>

[<span data-ttu-id="7354b-130">Gráficos de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="7354b-130">Direct3D 11 Graphics</span></span>](atoc-dx-graphics-direct3d-11.md)
</dt> </dl>

 

 






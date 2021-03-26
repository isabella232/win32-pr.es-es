---
title: Direct3D 11 en hardware de nivel inferior
description: En esta sección se describe cómo Direct3D 11 está diseñado para admitir hardware nuevo y existente, de DirectX 9 a DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104560908"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="2d7be-103">Direct3D 11 en hardware de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="2d7be-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="2d7be-104">En esta sección se describe cómo Direct3D 11 está diseñado para admitir hardware nuevo y existente, de DirectX 9 a DirectX 11.</span><span class="sxs-lookup"><span data-stu-id="2d7be-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="2d7be-105">En este diagrama se muestra cómo Direct3D 11 admite hardware nuevo y existente.</span><span class="sxs-lookup"><span data-stu-id="2d7be-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![diagrama del hardware que admite Direct3D 11](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="2d7be-107">Con Direct3D 11, se introduce un nuevo paradigma denominado niveles de características.</span><span class="sxs-lookup"><span data-stu-id="2d7be-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="2d7be-108">Un nivel de característica es un conjunto bien definido de funcionalidades de GPU.</span><span class="sxs-lookup"><span data-stu-id="2d7be-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="2d7be-109">Con un nivel de característica, puede dirigirse a una aplicación de Direct3D para que se ejecute en una versión de nivel inferior del hardware de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2d7be-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="2d7be-110">En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.</span><span class="sxs-lookup"><span data-stu-id="2d7be-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="2d7be-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="2d7be-111">In this section</span></span>



| <span data-ttu-id="2d7be-112">Tema</span><span class="sxs-lookup"><span data-stu-id="2d7be-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="2d7be-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d7be-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d7be-114">Niveles de característica de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d7be-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="2d7be-115">En este tema se describen los niveles de características de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2d7be-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="2d7be-116">Excepciones</span><span class="sxs-lookup"><span data-stu-id="2d7be-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="2d7be-117">En este tema se describen las excepciones cuando se usa Direct3D 11 en hardware de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="2d7be-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="2d7be-118">Sombreadores de cálculo en hardware de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="2d7be-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="2d7be-119">En este tema se describe cómo usar los [sombreadores de cálculo](direct3d-11-advanced-stages-compute-shader.md) en una aplicación de Direct3D 11 en hardware de Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="2d7be-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="2d7be-120">Prevención de SRVs de sombreador de píxeles NULOs no deseados</span><span class="sxs-lookup"><span data-stu-id="2d7be-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="2d7be-121">En este tema se describe cómo solucionar el controlador que recibe el sombreador **nulo** : vistas de recursos (SRVs) incluso cuando se enlazan SRVs que no son **null** a la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="2d7be-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="2d7be-122">Temas de procedimientos sobre los niveles de características</span><span class="sxs-lookup"><span data-stu-id="2d7be-122">How to topics about feature levels</span></span>



| <span data-ttu-id="2d7be-123">Tema</span><span class="sxs-lookup"><span data-stu-id="2d7be-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="2d7be-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d7be-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="2d7be-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Cómo: obtener el nivel de características del dispositivo](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="2d7be-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="2d7be-126">Cómo obtener un nivel de característica.</span><span class="sxs-lookup"><span data-stu-id="2d7be-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2d7be-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d7be-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d7be-128">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="2d7be-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 






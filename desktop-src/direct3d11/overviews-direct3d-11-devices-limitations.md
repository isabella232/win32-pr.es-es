---
title: Limitaciones al crear dewarp y dispositivos de referencia
description: Existen algunas limitaciones para crear dispositivos de hipervelocidad y de referencia en Direct3D 10,1 y Direct3D 11,0. En este tema se describen estas limitaciones.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358994"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="c01ac-104">Limitaciones al crear dewarp y dispositivos de referencia</span><span class="sxs-lookup"><span data-stu-id="c01ac-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="c01ac-105">Existen algunas limitaciones para crear dispositivos de hipervelocidad y de referencia en Direct3D 10,1 y Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="c01ac-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="c01ac-106">En este tema se describen estas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="c01ac-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="c01ac-107">Los tipos de controlador D3D10 \_ \_ Type \_ Warp y D3D10 de \_ referencia de tipo controlador \_ \_ no se admiten en los niveles de características \_ de D3D10 de nivel \_ \_ 9 \_ 1 a D3D10 \_ \_ \_ de nivel de característica 9 \_ 3 en Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="c01ac-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="c01ac-108">Además, el \_ tipo de \_ controlador D3D Type \_ Warp no se admite en el \_ nivel de característica de D3d \_ \_ 11 \_ 0 en Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="c01ac-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="c01ac-109">Es decir, cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10,1 o cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11,0, si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características en la llamada, la llamada no es válida.</span><span class="sxs-lookup"><span data-stu-id="c01ac-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="c01ac-110">Solo las siguientes combinaciones de niveles de características, tiempos de ejecución y tipos de controlador son válidas para los dispositivos WARP y Reference:</span><span class="sxs-lookup"><span data-stu-id="c01ac-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="c01ac-111">\_Tipo de controlador D3D \_ \_ Warp en todos los niveles de características de Direct3D 11,1, que incluye Windows 8</span><span class="sxs-lookup"><span data-stu-id="c01ac-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="c01ac-112">\_Referencia de \_ tipo de controlador D3D \_ en todos los niveles de características de Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="c01ac-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="c01ac-113">Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11,1, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.</span><span class="sxs-lookup"><span data-stu-id="c01ac-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="c01ac-114">\_ \_ Tipo de controlador D3D \_ Warp en el nivel de característica de D3D \_ \_ \_ 9 \_ 1 a \_ \_ \_ \_ los niveles de características de nivel de característica 10 1 de D3D en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c01ac-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="c01ac-115">\_ \_ \_ Referencia de tipo de controlador D3D en el nivel de característica de D3D de nivel \_ \_ \_ 9 \_ 1 a \_ \_ \_ \_ los niveles de características 11 0 de nivel de característica D3D en Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c01ac-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="c01ac-116">Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.</span><span class="sxs-lookup"><span data-stu-id="c01ac-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="c01ac-117">\_ \_ Tipo de controlador D3D10 \_ Warp y \_ \_ referencia de tipo de controlador D3D10 en el \_ nivel de características D3D10 de \_ \_ \_ 10 \_ 0 a D3D10 \_ \_ \_ de nivel de característica 10 \_ 1 en Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="c01ac-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="c01ac-118">Cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10,1, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.</span><span class="sxs-lookup"><span data-stu-id="c01ac-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c01ac-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c01ac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c01ac-120">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="c01ac-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="c01ac-121">Introducción a Direct3D 11 en el hardware de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="c01ac-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="c01ac-122">Cómo: crear un dispositivo WARP</span><span class="sxs-lookup"><span data-stu-id="c01ac-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="c01ac-123">Cómo: crear un dispositivo de referencia</span><span class="sxs-lookup"><span data-stu-id="c01ac-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="c01ac-124">**\_Tipo de controlador D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="c01ac-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="c01ac-125">**D3D10 \_ característica \_ Level1**</span><span class="sxs-lookup"><span data-stu-id="c01ac-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="c01ac-126">**\_Tipo de controlador D3D \_**</span><span class="sxs-lookup"><span data-stu-id="c01ac-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="c01ac-127">**\_Nivel de característica D3D \_**</span><span class="sxs-lookup"><span data-stu-id="c01ac-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 
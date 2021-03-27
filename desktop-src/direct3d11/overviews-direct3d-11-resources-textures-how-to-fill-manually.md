---
title: Cómo inicializar una textura mediante programación
description: En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas que se crean con distintos tipos de usos.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903614"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="935f0-103">Cómo: inicializar una textura mediante programación</span><span class="sxs-lookup"><span data-stu-id="935f0-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="935f0-104">Puede inicializar una textura durante la creación del objeto o puede rellenar el objeto mediante programación una vez creado.</span><span class="sxs-lookup"><span data-stu-id="935f0-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="935f0-105">En este tema se muestran varios ejemplos en los que se muestra cómo inicializar texturas que se crean con distintos tipos de usos.</span><span class="sxs-lookup"><span data-stu-id="935f0-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="935f0-106">En este ejemplo se da por supuesto que ya sabe cómo [crear una textura](overviews-direct3d-11-resources-textures-create.md).</span><span class="sxs-lookup"><span data-stu-id="935f0-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="935f0-107">Uso predeterminado</span><span class="sxs-lookup"><span data-stu-id="935f0-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="935f0-108">Uso dinámico</span><span class="sxs-lookup"><span data-stu-id="935f0-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="935f0-109">Uso del almacenamiento provisional</span><span class="sxs-lookup"><span data-stu-id="935f0-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="935f0-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="935f0-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="935f0-111">Uso predeterminado</span><span class="sxs-lookup"><span data-stu-id="935f0-111">Default Usage</span></span>

<span data-ttu-id="935f0-112">El tipo de uso más común es el uso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="935f0-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="935f0-113">Para rellenar una textura predeterminada (una creada con el **\_ \_ valor predeterminado de uso de D3D11**), puede:</span><span class="sxs-lookup"><span data-stu-id="935f0-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="935f0-114">Llame a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inicialice *pInitialData* para apuntar a los datos proporcionados por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="935f0-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="935f0-115">o</span><span class="sxs-lookup"><span data-stu-id="935f0-115">or</span></span>

-   <span data-ttu-id="935f0-116">Después de llamar a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para rellenar la textura predeterminada con los datos de un puntero proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="935f0-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="935f0-117">Uso dinámico</span><span class="sxs-lookup"><span data-stu-id="935f0-117">Dynamic Usage</span></span>

<span data-ttu-id="935f0-118">Para rellenar una textura dinámica (una creada con el **uso de D3D11 \_ \_ dinámica**):</span><span class="sxs-lookup"><span data-stu-id="935f0-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="935f0-119">Obtener un puntero a la memoria de textura pasando el **\_ \_ \_ descartado de escritura de asignación de D3D11** al llamar a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="935f0-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="935f0-120">Escribir datos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="935f0-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="935f0-121">Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar cuando termine de escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="935f0-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="935f0-122">Uso del almacenamiento provisional</span><span class="sxs-lookup"><span data-stu-id="935f0-122">Staging Usage</span></span>

<span data-ttu-id="935f0-123">Para rellenar una textura de ensayo (una creada con el **\_ \_ almacenamiento provisional del uso de D3D11**):</span><span class="sxs-lookup"><span data-stu-id="935f0-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="935f0-124">Obtenga un puntero a la memoria de textura pasando en la **D3D11 de \_ \_ escritura de asignación** al llamar a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="935f0-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="935f0-125">Escribir datos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="935f0-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="935f0-126">Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) desasignar cuando termine de escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="935f0-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="935f0-127">Después, se puede usar una textura de ensayo como parámetro de origen para [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) para rellenar un recurso predeterminado o dinámico.</span><span class="sxs-lookup"><span data-stu-id="935f0-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="935f0-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="935f0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="935f0-129">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="935f0-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="935f0-130">Texturas</span><span class="sxs-lookup"><span data-stu-id="935f0-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 





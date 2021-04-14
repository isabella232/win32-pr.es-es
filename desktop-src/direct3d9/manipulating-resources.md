---
description: La aplicación manipula los recursos para representar una escena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipular recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422730"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="2daba-103">Manipular recursos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2daba-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="2daba-104">La aplicación manipula los recursos para representar una escena.</span><span class="sxs-lookup"><span data-stu-id="2daba-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="2daba-105">En primer lugar, una aplicación debe crear un recurso de textura con uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2daba-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="2daba-106">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="2daba-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="2daba-107">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="2daba-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="2daba-108">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="2daba-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="2daba-109">En su lugar, se puede crear un recurso de textura con una de las funciones de texturización D3DXCreatexxx.</span><span class="sxs-lookup"><span data-stu-id="2daba-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="2daba-110">Los objetos de textura devueltos por los métodos de creación de texturas son contenedores de superficies o volúmenes; Estos contenedores se conocen genéricamente como búferes.</span><span class="sxs-lookup"><span data-stu-id="2daba-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="2daba-111">Los búferes que pertenecen al recurso heredan los usos, el formato y el grupo del recurso, pero tienen su propio tipo.</span><span class="sxs-lookup"><span data-stu-id="2daba-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="2daba-112">Para obtener más información, vea [propiedades de recursos (Direct3D 9)](resource-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2daba-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="2daba-113">La aplicación obtiene acceso a las superficies contenidas con el fin de cargar material gráfico mediante una llamada a los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2daba-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="2daba-114">Para obtener más información, consulte [bloqueo de recursos (Direct3D 9)](locking-resources.md).</span><span class="sxs-lookup"><span data-stu-id="2daba-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="2daba-115">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="2daba-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="2daba-116">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="2daba-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="2daba-117">**IDirect3DVolumeTexture9:: LockBox**</span><span class="sxs-lookup"><span data-stu-id="2daba-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="2daba-118">Los métodos de bloqueo toman argumentos que indican la superficie contenida; por ejemplo, el subnivel de mipmap o la cara del cubo de los punteros de textura y devuelven los píxeles.</span><span class="sxs-lookup"><span data-stu-id="2daba-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="2daba-119">La aplicación típica nunca utiliza directamente un objeto Surface.</span><span class="sxs-lookup"><span data-stu-id="2daba-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="2daba-120">Cree recursos orientados a geometría mediante una llamada a [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/desktop/api) o [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span><span class="sxs-lookup"><span data-stu-id="2daba-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="2daba-121">Bloquee y rellene los recursos de búfer mediante una llamada a [**IDirect3DIndexBuffer9:: Lock**](/windows/desktop/api) o [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), en función del recurso.</span><span class="sxs-lookup"><span data-stu-id="2daba-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="2daba-122">En el caso de los recursos de textura administrados, el proceso de creación de recursos finaliza aquí.</span><span class="sxs-lookup"><span data-stu-id="2daba-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="2daba-123">En el caso de los recursos de textura no administrados, una aplicación promueve los recursos de memoria del sistema a recursos accesibles desde el dispositivo (para la aceleración de hardware) mediante una llamada a [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="2daba-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="2daba-124">Para presentar imágenes representadas a partir de recursos, la aplicación también necesita búferes de estarcido de color y de profundidad.</span><span class="sxs-lookup"><span data-stu-id="2daba-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="2daba-125">En el caso de las aplicaciones típicas, el búfer de color es propiedad de la cadena de intercambio del dispositivo, que es una colección de superficies de búfer de reserva y se crea implícitamente con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2daba-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="2daba-126">Las superficies de la galería de símbolos de profundidad pueden crearse implícitamente o crearse explícitamente mediante el método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2daba-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2daba-127">La aplicación asocia un dispositivo y su búfer de profundidad y color con una llamada a [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) o [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="2daba-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="2daba-128">Para obtener más información sobre cómo presentar la imagen final, vea [presentar una escena (Direct3D 9)](presenting-a-scene.md).</span><span class="sxs-lookup"><span data-stu-id="2daba-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2daba-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2daba-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2daba-130">Recursos de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2daba-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 

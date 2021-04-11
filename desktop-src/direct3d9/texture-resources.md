---
description: 'Los recursos de textura se implementan en la interfaz IDirect3DTexture9. Para obtener un puntero a una interfaz de textura, llame al método IDirect3DDevice9:: CreateTexture o a cualquiera de las siguientes funciones de D3DX.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Recursos de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274781"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="47036-104">Recursos de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="47036-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="47036-105">Los recursos de textura se implementan en la interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="47036-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="47036-106">Para obtener un puntero a una interfaz de textura, llame al método [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o a cualquiera de las siguientes funciones de D3DX.</span><span class="sxs-lookup"><span data-stu-id="47036-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="47036-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="47036-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="47036-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="47036-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="47036-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="47036-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="47036-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="47036-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="47036-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="47036-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="47036-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="47036-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="47036-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="47036-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="47036-114">En el ejemplo de código siguiente se usa [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) para cargar una textura desde Tiger.bmp.</span><span class="sxs-lookup"><span data-stu-id="47036-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="47036-115">El primer parámetro que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) acepta es un puntero a una interfaz [**IDirect3DDevice9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="47036-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="47036-116">El segundo parámetro indica a Direct3D el nombre del archivo desde el que se va a cargar la textura.</span><span class="sxs-lookup"><span data-stu-id="47036-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="47036-117">El tercer parámetro toma la dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa el objeto de textura creado.</span><span class="sxs-lookup"><span data-stu-id="47036-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="47036-118">Representar con recursos de textura</span><span class="sxs-lookup"><span data-stu-id="47036-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="47036-119">Direct3D admite varias combinaciones de texturas mediante el concepto de fases de textura.</span><span class="sxs-lookup"><span data-stu-id="47036-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="47036-120">Cada fase de textura contiene una textura y las operaciones que se pueden realizar en la textura.</span><span class="sxs-lookup"><span data-stu-id="47036-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="47036-121">Las texturas de las fases de textura forman el conjunto de texturas actuales.</span><span class="sxs-lookup"><span data-stu-id="47036-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="47036-122">Para obtener más información, vea [Texture blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="47036-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="47036-123">El estado de cada textura se encapsula en su fase de textura.</span><span class="sxs-lookup"><span data-stu-id="47036-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="47036-124">En una aplicación de C++, el estado de cada textura debe establecerse con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="47036-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="47036-125">Pase el número de fase (0-7) como valor del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="47036-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="47036-126">Establezca el valor del segundo parámetro en un miembro del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="47036-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="47036-127">El último parámetro es el valor de estado para el estado de textura determinado.</span><span class="sxs-lookup"><span data-stu-id="47036-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="47036-128">Mediante el uso de punteros de interfaz de textura, la aplicación puede presentar una mezcla de hasta ocho texturas.</span><span class="sxs-lookup"><span data-stu-id="47036-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="47036-129">Establezca las texturas actuales invocando el método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="47036-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="47036-130">Direct3D combina todas las texturas actuales con las primitivas que representa.</span><span class="sxs-lookup"><span data-stu-id="47036-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="47036-131">El método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa el recuento de referencias de la superficie de textura que se está asignando.</span><span class="sxs-lookup"><span data-stu-id="47036-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="47036-132">Cuando ya no se necesite la textura, debe establecer la textura en la fase adecuada en **null**.</span><span class="sxs-lookup"><span data-stu-id="47036-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="47036-133">Si no lo hace, la superficie no se liberará, lo que producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="47036-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="47036-134">La aplicación puede establecer el estado de ajuste de textura para las texturas actuales llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) .</span><span class="sxs-lookup"><span data-stu-id="47036-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="47036-135">Pase un valor de D3DRS \_ WRAP0 a D3DRS \_ WRAP7 como valor del primer parámetro y use una combinación de las \_ marcas D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 y D3DWRAPCOORD \_ 3 para habilitar el ajuste en las direcciones u, v o w.</span><span class="sxs-lookup"><span data-stu-id="47036-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="47036-136">La aplicación también puede establecer los Estados de la perspectiva de textura y del filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="47036-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="47036-137">Vea [filtrado de textura (Direct3D 9)](texture-filtering.md).</span><span class="sxs-lookup"><span data-stu-id="47036-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47036-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47036-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47036-139">Texturas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="47036-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 

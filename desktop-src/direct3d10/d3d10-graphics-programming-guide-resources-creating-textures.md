---
description: Un recurso de textura es una colección estructurada de datos.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Crear recursos de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000632"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="f03db-103">Crear recursos de textura (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f03db-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="f03db-104">Un recurso de [textura](d3d10-graphics-programming-guide-resources-types.md) es una colección estructurada de datos.</span><span class="sxs-lookup"><span data-stu-id="f03db-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="f03db-105">Normalmente, los valores de color se almacenan en texturas y se obtiene acceso a ellos durante la representación por parte de la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) en varias fases para la entrada y la salida.</span><span class="sxs-lookup"><span data-stu-id="f03db-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="f03db-106">Crear texturas y definir cómo se usarán es una parte importante de la representación de escenas de aspecto interesante en Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="f03db-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="f03db-107">Aunque las texturas suelen contener información de color, la creación de texturas con un [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diferente les permite almacenar diferentes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="f03db-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="f03db-108">Estos datos pueden ser aprovechados por la canalización de Direct3D 10 de formas no tradicionales.</span><span class="sxs-lookup"><span data-stu-id="f03db-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="f03db-109">Todas las texturas tienen límites en la cantidad de memoria que consumen y el número de textura que contienen.</span><span class="sxs-lookup"><span data-stu-id="f03db-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="f03db-110">Estos límites se especifican mediante [constantes de recursos](d3d10-graphics-reference-resource-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f03db-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="f03db-111">Crear una textura a partir de un archivo</span><span class="sxs-lookup"><span data-stu-id="f03db-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="f03db-112">Crear textura y vista por separado</span><span class="sxs-lookup"><span data-stu-id="f03db-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="f03db-113">Crear textura y ver simultáneamente</span><span class="sxs-lookup"><span data-stu-id="f03db-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="f03db-114">Crear texturas vacías</span><span class="sxs-lookup"><span data-stu-id="f03db-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="f03db-115">Representar una textura</span><span class="sxs-lookup"><span data-stu-id="f03db-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="f03db-116">Rellenar las texturas manualmente</span><span class="sxs-lookup"><span data-stu-id="f03db-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="f03db-117">Varios Rendertargets</span><span class="sxs-lookup"><span data-stu-id="f03db-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="f03db-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f03db-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="f03db-119">Crear una textura a partir de un archivo</span><span class="sxs-lookup"><span data-stu-id="f03db-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="f03db-120">La [biblioteca de utilidades de D3DX](d3d10-graphics-reference-d3dx10.md) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="f03db-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f03db-121">Al crear una textura en Direct3D 10, también debe crear una [vista](d3d10-graphics-programming-guide-resources-access-views.md).</span><span class="sxs-lookup"><span data-stu-id="f03db-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="f03db-122">Una vista es un objeto que indica al dispositivo cómo se debe tener acceso a una textura durante la representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="f03db-123">La forma más común de obtener acceso a una textura es leer desde ella mediante un [sombreador](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="f03db-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="f03db-124">Una vista de recursos de sombreador indicará a un sombreador cómo leer de una textura durante la representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="f03db-125">El tipo de vista que utilizará una textura debe especificarse al crearla.</span><span class="sxs-lookup"><span data-stu-id="f03db-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="f03db-126">La creación de una textura y la carga de los datos iniciales se pueden realizar de dos maneras diferentes: crear una textura y una vista por separado, o bien crear la textura y la vista al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f03db-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="f03db-127">La API proporciona ambas técnicas para que pueda elegir lo que mejor se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="f03db-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="f03db-128">Crear textura y vista por separado</span><span class="sxs-lookup"><span data-stu-id="f03db-128">Create Texture and View Separately</span></span>

<span data-ttu-id="f03db-129">La forma más fácil de crear una textura es cargarla desde un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="f03db-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="f03db-130">Para crear la textura, solo tiene que rellenar una estructura y proporcionar el nombre de la textura a [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="f03db-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="f03db-131">La función de D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) realiza tres cosas: en primer lugar, crea un objeto de textura de Direct3D 10. en segundo lugar, lee el archivo de imagen de entrada; en tercer lugar, almacena los datos de la imagen en el objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="f03db-132">En el ejemplo anterior, se carga un archivo BMP, pero la función puede cargar diversos tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f03db-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="f03db-133">La marca de enlace indica que la textura se creará como un recurso de sombreador que permite que una fase del sombreador Lea la textura durante la representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="f03db-134">En el ejemplo anterior no se especifican todos los parámetros de carga.</span><span class="sxs-lookup"><span data-stu-id="f03db-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="f03db-135">De hecho, a menudo es beneficioso simplemente quitar los parámetros de carga, ya que permite a D3DX elegir los valores adecuados en función de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="f03db-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="f03db-136">Si desea que la imagen de entrada determine todos los parámetros con los que se crea la textura, simplemente especifique **null** para el parámetro **loadInfo** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f03db-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="f03db-137">Especificar **null** para la información de carga es un método abreviado sencillo pero eficaz.</span><span class="sxs-lookup"><span data-stu-id="f03db-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="f03db-138">Ahora que se ha creado una textura, debe crear una vista de recursos de sombreador para que la textura se pueda enlazar como entrada a un sombreador.</span><span class="sxs-lookup"><span data-stu-id="f03db-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="f03db-139">Puesto que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) devuelve un puntero a un recurso y no un puntero a una textura, tiene que determinar el tipo exacto de recurso que se ha cargado y, a continuación, puede crear una vista de recursos del sombreador mediante [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="f03db-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="f03db-140">Aunque en el ejemplo anterior se crea una vista de recursos de sombreador 2D, el código para crear otros tipos de vista de recursos de sombreador es muy similar.</span><span class="sxs-lookup"><span data-stu-id="f03db-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="f03db-141">Cualquier fase del sombreador ahora puede utilizar esta textura como entrada.</span><span class="sxs-lookup"><span data-stu-id="f03db-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="f03db-142">El uso de [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) para crear una textura y su vista asociada es una manera de preparar una textura que se va a enlazar a una fase de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f03db-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="f03db-143">Otra forma de hacerlo es crear tanto la textura como su vista al mismo tiempo, que se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="f03db-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="f03db-144">Crear textura y ver simultáneamente</span><span class="sxs-lookup"><span data-stu-id="f03db-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="f03db-145">Direct3D 10 requiere una textura y una vista de recursos del sombreador para leer de una textura durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f03db-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="f03db-146">Dado que la creación de una textura y una vista de recursos del sombreador es una tarea común, D3DX proporciona el [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) para que lo haga.</span><span class="sxs-lookup"><span data-stu-id="f03db-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="f03db-147">Con una única llamada de D3DX, se crean la vista de recursos y la textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="f03db-148">La funcionalidad del parámetro **loadInfo** no cambia; puede usarlo para personalizar cómo se crea la textura, o para derivar los parámetros necesarios del archivo de entrada especificando **null** para el parámetro **loadInfo** .</span><span class="sxs-lookup"><span data-stu-id="f03db-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="f03db-149">El objeto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) devuelto por la función [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) se puede usar más adelante para recuperar la interfaz [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) original si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f03db-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="f03db-150">Esto se puede hacer llamando al método [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .</span><span class="sxs-lookup"><span data-stu-id="f03db-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="f03db-151">D3DX proporciona una sola función para crear una vista de textura y de un sombreador de recursos como convienience; depende de usted decidir qué método de creación de una textura y vista se adapta mejor a las necesidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f03db-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="f03db-152">Ahora que sabe cómo crear una textura y su vista de recursos del sombreador, en la siguiente sección se muestra cómo se puede muestrear (leer) de esa textura mediante un sombreador.</span><span class="sxs-lookup"><span data-stu-id="f03db-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="f03db-153">Crear texturas vacías</span><span class="sxs-lookup"><span data-stu-id="f03db-153">Creating Empty Textures</span></span>

<span data-ttu-id="f03db-154">A veces, las aplicaciones querrán crear una textura y calcular los datos que se van a almacenar en la textura, o usar la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos para representar esta textura y, posteriormente, usar los resultados en otro procesamiento.</span><span class="sxs-lookup"><span data-stu-id="f03db-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="f03db-155">Estas texturas se pueden actualizar mediante la canalización de gráficos o la propia aplicación, en función del tipo de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) especificado para la textura cuando se creó.</span><span class="sxs-lookup"><span data-stu-id="f03db-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="f03db-156">Representar una textura</span><span class="sxs-lookup"><span data-stu-id="f03db-156">Rendering to a texture</span></span>

<span data-ttu-id="f03db-157">El caso más común de crear una textura vacía que se rellenará con datos durante el tiempo de ejecución es el caso en el que una aplicación desea representar en una textura y, a continuación, utilizar los resultados de la operación de representación en un paso posterior.</span><span class="sxs-lookup"><span data-stu-id="f03db-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="f03db-158">Las texturas creadas con este propósito deben especificar el [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f03db-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="f03db-159">En el ejemplo de código siguiente se crea una textura vacía que la canalización puede representar y que posteriormente se usa como entrada para un [sombreador](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span><span class="sxs-lookup"><span data-stu-id="f03db-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="f03db-160">La creación de la textura requiere que la aplicación especifique información sobre las propiedades que tendrá la textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="f03db-161">El ancho y el alto de la textura en textura se establece en 256.</span><span class="sxs-lookup"><span data-stu-id="f03db-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="f03db-162">Para este destino de representación, solo se necesita un único nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="f03db-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="f03db-163">Solo se requiere un destino de representación para que el tamaño de la matriz se establezca en 1.</span><span class="sxs-lookup"><span data-stu-id="f03db-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="f03db-164">Cada textura contiene valores de punto flotante de 4 32 bits, que se pueden usar para almacenar información muy precisa ( [**consulte \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="f03db-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="f03db-165">Una muestra por píxel es todo lo que se necesitará.</span><span class="sxs-lookup"><span data-stu-id="f03db-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="f03db-166">El uso se establece en el valor predeterminado porque permite la colocación más eficaz del destino de representación en la memoria.</span><span class="sxs-lookup"><span data-stu-id="f03db-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="f03db-167">Por último, el hecho de que la textura se enlace como destino de representación y se especifica un recurso de sombreador en distintos puntos en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="f03db-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="f03db-168">Las texturas no se pueden enlazar directamente a la representación de la canalización. Use una vista de representación y destino como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="f03db-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="f03db-169">El formato de la vista de representación-destino se establece simplemente en el formato de la textura original.</span><span class="sxs-lookup"><span data-stu-id="f03db-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="f03db-170">La información del recurso debe interpretarse como una textura 2D y solo queremos usar el primer nivel de mipmap del destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="f03db-171">De forma similar al modo en que se debe crear una vista de representación y destino para que el destino de representación se pueda enlazar para la salida a la canalización, se debe crear una vista de recursos del sombreador para que el destino de representación se pueda enlazar a la canalización como entrada.</span><span class="sxs-lookup"><span data-stu-id="f03db-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="f03db-172">En el ejemplo de código siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="f03db-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="f03db-173">Los parámetros de las descripciones de la vista de recursos y del sombreador son muy similares a los de las descripciones de vista de destino de representación y se eligieron por las mismas razones.</span><span class="sxs-lookup"><span data-stu-id="f03db-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="f03db-174">Rellenar las texturas manualmente</span><span class="sxs-lookup"><span data-stu-id="f03db-174">Filling Textures Manually</span></span>

<span data-ttu-id="f03db-175">A veces, las aplicaciones desean calcular valores en tiempo de ejecución, colocarlos en una textura manualmente y, a continuación, hacer que la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos use esta textura en operaciones de representación posteriores.</span><span class="sxs-lookup"><span data-stu-id="f03db-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="f03db-176">Para ello, la aplicación debe crear una textura vacía de tal forma que permita que la CPU tenga acceso a la memoria subyacente.</span><span class="sxs-lookup"><span data-stu-id="f03db-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="f03db-177">Esto se hace creando una textura dinámica y obteniendo acceso a la memoria subyacente llamando a un método determinado.</span><span class="sxs-lookup"><span data-stu-id="f03db-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="f03db-178">En el ejemplo de código siguiente se muestra cómo utilizar este recurso.</span><span class="sxs-lookup"><span data-stu-id="f03db-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="f03db-179">Tenga en cuenta que el formato se establece en 32 bits por píxel, donde cada componente se define mediante 8 bits.</span><span class="sxs-lookup"><span data-stu-id="f03db-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="f03db-180">El parámetro Usage se establece en Dynamic mientras que las marcas de enlace se establecen para especificar que un sombreador tendrá acceso a la textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="f03db-181">El resto de la descripción de la textura es similar a crear un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="f03db-182">La llamada a [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) permite que la aplicación tenga acceso a la memoria subyacente de la textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="f03db-183">A continuación, el puntero recuperado se usa para rellenar la textura con datos.</span><span class="sxs-lookup"><span data-stu-id="f03db-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="f03db-184">Esto puede verse en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="f03db-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="f03db-185">Varios Rendertargets</span><span class="sxs-lookup"><span data-stu-id="f03db-185">Multiple Rendertargets</span></span>

<span data-ttu-id="f03db-186">Se pueden enlazar hasta ocho vistas de destino de representación a la canalización a la vez (con [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span><span class="sxs-lookup"><span data-stu-id="f03db-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="f03db-187">Para cada píxel (o cada ejemplo si el muestreo múltiple está habilitado), la combinación se realiza de forma independiente para cada vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="f03db-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="f03db-188">Dos de las variables de estado de Blend-BlendEnable y RenderTargetWriteMask-son matrices de ocho, cada miembro de la matriz corresponde a una vista de representación-destino.</span><span class="sxs-lookup"><span data-stu-id="f03db-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="f03db-189">Cuando se usan varios destinos de representación, cada destino de representación debe ser del mismo [tipo de recurso](d3d10-graphics-programming-guide-resources-types.md) (búfer, textura 1D, matriz de textura 2D, etc.) y debe tener la misma dimensión (ancho, alto, profundidad para las texturas 3D y tamaño de la matriz para las matrices de texturas).</span><span class="sxs-lookup"><span data-stu-id="f03db-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="f03db-190">Si los destinos de representación tienen varias muestras, todos deben tener el mismo número de muestras por píxel.</span><span class="sxs-lookup"><span data-stu-id="f03db-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="f03db-191">Solo puede haber un búfer de estarcido de profundidad activo, independientemente del número de destinos de representación que estén activos.</span><span class="sxs-lookup"><span data-stu-id="f03db-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="f03db-192">Al usar matrices de textura como destinos de representación, todas las dimensiones de la vista deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="f03db-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="f03db-193">No es necesario que los destinos de representación tengan el mismo formato de textura.</span><span class="sxs-lookup"><span data-stu-id="f03db-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f03db-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f03db-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f03db-195">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="f03db-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 

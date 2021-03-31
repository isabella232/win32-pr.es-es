---
description: La creación de búferes requiere la definición de los datos que almacenará el búfer, el suministro de datos de inicialización y la configuración de las marcas de uso y enlace apropiadas. Para crear texturas, vea crear recursos de textura (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Crear recursos de búfer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807537"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="4920d-104">Crear recursos de búfer (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4920d-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="4920d-105">La creación de búferes requiere la definición de los datos que almacenará el búfer, el suministro de datos de inicialización y la configuración de las marcas de uso y enlace apropiadas.</span><span class="sxs-lookup"><span data-stu-id="4920d-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="4920d-106">Para crear texturas, vea [crear recursos de textura (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="4920d-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="4920d-107">Crear un búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="4920d-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="4920d-108">Crear una descripción de búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="4920d-109">Crear los datos de inicialización del búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="4920d-110">Crear el búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="4920d-111">Crear un búfer de índice</span><span class="sxs-lookup"><span data-stu-id="4920d-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="4920d-112">Crear un búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="4920d-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="4920d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4920d-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="4920d-114">Crear un búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="4920d-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="4920d-115">Los pasos para crear un [búfer de vértice](d3d10-graphics-programming-guide-resources-types.md) son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="4920d-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="4920d-116">Crear una descripción de búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="4920d-117">Crear los datos de inicialización del búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="4920d-118">Crear el búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="4920d-119">Crear una descripción de búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-119">Create a Buffer Description</span></span>

<span data-ttu-id="4920d-120">Al crear un búfer de vértices, se usa una descripción de búfer (vea [**D3D10 \_ buffer \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) para definir cómo se organizan los datos en el búfer, cómo la canalización puede tener acceso al búfer y cómo se usará el búfer.</span><span class="sxs-lookup"><span data-stu-id="4920d-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="4920d-121">En el ejemplo siguiente se muestra cómo crear una descripción de búfer para un solo triángulo con vértices que contienen valores de posición y color.</span><span class="sxs-lookup"><span data-stu-id="4920d-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="4920d-122">En este ejemplo, la descripción del búfer se inicializa con casi todos los valores predeterminados para el [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), el [**acceso a la CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) y las [**marcas misceláneas**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="4920d-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="4920d-123">Los demás valores son para el [**marcador de enlace**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) que identifica el recurso como solo un búfer de vértices y el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="4920d-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="4920d-124">Las marcas de acceso de uso y de CPU son importantes para el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4920d-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="4920d-125">Estas dos marcas determinan con qué frecuencia se obtiene acceso a un recurso, el tipo de memoria en el que se puede cargar el recurso y el procesador que necesita para tener acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="4920d-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="4920d-126">Uso predeterminado: este recurso no se actualizará con mucha frecuencia.</span><span class="sxs-lookup"><span data-stu-id="4920d-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="4920d-127">Establecer el acceso a la CPU en 0 significa que la CPU no necesitará leer ni escribir el recurso.</span><span class="sxs-lookup"><span data-stu-id="4920d-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="4920d-128">Tomadas en combinación, esto significa que el tiempo de ejecución puede cargar el recurso en la memoria de mayor rendimiento para la GPU, ya que el recurso no requiere acceso a la CPU.</span><span class="sxs-lookup"><span data-stu-id="4920d-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="4920d-129">Tal y como se espera, existe un equilibrio entre el mejor rendimiento y la accesibilidad en cualquier momento por cada procesador.</span><span class="sxs-lookup"><span data-stu-id="4920d-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="4920d-130">Por ejemplo, el uso predeterminado sin acceso a la CPU significa que el recurso se puede poner a disposición de la GPU exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="4920d-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="4920d-131">Esto podría incluir la carga del recurso en la memoria no accesible directamente por la CPU.</span><span class="sxs-lookup"><span data-stu-id="4920d-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="4920d-132">El recurso solo se puede modificar con [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span><span class="sxs-lookup"><span data-stu-id="4920d-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="4920d-133">Crear los datos de inicialización del búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="4920d-134">Un búfer es simplemente una colección de elementos y se coloca como una matriz 1D.</span><span class="sxs-lookup"><span data-stu-id="4920d-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="4920d-135">Como resultado, el paso de la memoria del sistema y el intervalo de la memoria del sistema son los mismos; tamaño de la declaración de datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="4920d-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="4920d-136">Una aplicación puede proporcionar datos de inicialización cuando se crea un búfer mediante una [**Descripción de subrecurso**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), que contiene un puntero a los datos de recursos reales y contiene información sobre el tamaño y el diseño de los datos.</span><span class="sxs-lookup"><span data-stu-id="4920d-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="4920d-137">Cualquier búfer creado con uso inmutable (consulte [**D3D10 \_ Usage \_ inmutable**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) debe inicializarse en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="4920d-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="4920d-138">Los búferes que usan cualquiera de las otras marcas de uso se pueden actualizar después de la inicialización con [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)y [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), o mediante el acceso a su memoria subyacente mediante el método [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .</span><span class="sxs-lookup"><span data-stu-id="4920d-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="4920d-139">Crear el búfer</span><span class="sxs-lookup"><span data-stu-id="4920d-139">Create the Buffer</span></span>

<span data-ttu-id="4920d-140">Con la descripción del búfer y los datos de inicialización (que es opcional), llame a [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) para crear un búfer de vértice.</span><span class="sxs-lookup"><span data-stu-id="4920d-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="4920d-141">El siguiente fragmento de código muestra cómo crear un búfer de vértices a partir de una matriz de datos de vértice declarada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4920d-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="4920d-142">Crear un búfer de índice</span><span class="sxs-lookup"><span data-stu-id="4920d-142">Create an Index Buffer</span></span>

<span data-ttu-id="4920d-143">Crear un búfer de índice es muy similar a crear un búfer de vértices. con dos diferencias.</span><span class="sxs-lookup"><span data-stu-id="4920d-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="4920d-144">Un búfer de índice solo contiene datos de 16 o 32 bits (en lugar de la amplia gama de formatos disponibles para un búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="4920d-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="4920d-145">Un búfer de índice también requiere una marca de enlace de búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="4920d-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="4920d-146">En el ejemplo siguiente se muestra cómo crear un búfer de índice a partir de una matriz de datos de índice.</span><span class="sxs-lookup"><span data-stu-id="4920d-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="4920d-147">Crear un búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="4920d-147">Create a Constant Buffer</span></span>

<span data-ttu-id="4920d-148">Direct3D 10 introduce un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="4920d-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="4920d-149">Un búfer de constantes o un búfer de constantes de sombreador es un búfer que contiene constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4920d-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="4920d-150">Este es un ejemplo de cómo crear un búfer de constantes, tomado del [ejemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4920d-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="4920d-151">Tenga en cuenta que cuando se usa la interfaz de [**interfaz ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , el proceso de creación, enlace y concesión de un búfer de constantes se controla mediante la instancia de la **interfaz ID3D10Effect** .</span><span class="sxs-lookup"><span data-stu-id="4920d-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="4920d-152">En ese caso, solo se nescesary para obtener la variable del efecto con uno de los métodos GetVariable como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) y actualizar la variable con uno de los métodos SetVariable como [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span><span class="sxs-lookup"><span data-stu-id="4920d-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="4920d-153">Para obtener un ejemplo del uso de la **interfaz ID3D10Effect** para administrar un búfer de constantes [, vea Tutorial 7: asignación de texturas y búferes de constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4920d-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4920d-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4920d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4920d-155">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4920d-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




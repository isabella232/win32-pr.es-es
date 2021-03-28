---
title: Cómo usar recursos dinámicos
description: Los recursos dinámicos se crean y se usan cuando la aplicación necesita cambiar los datos de esos recursos. Puede crear texturas y búferes para el uso dinámico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268383"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="4537d-104">Cómo: usar recursos dinámicos</span><span class="sxs-lookup"><span data-stu-id="4537d-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="4537d-105">**API importantes**</span><span class="sxs-lookup"><span data-stu-id="4537d-105">**Important APIs**</span></span>

-   [<span data-ttu-id="4537d-106">**ID3D11DeviceContext:: Map**</span><span class="sxs-lookup"><span data-stu-id="4537d-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="4537d-107">**ID3D11DeviceContext:: desasignar**</span><span class="sxs-lookup"><span data-stu-id="4537d-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="4537d-108">**Uso de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="4537d-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="4537d-109">Los recursos dinámicos se crean y se usan cuando la aplicación necesita cambiar los datos de esos recursos.</span><span class="sxs-lookup"><span data-stu-id="4537d-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="4537d-110">Puede crear texturas y búferes para el uso dinámico.</span><span class="sxs-lookup"><span data-stu-id="4537d-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4537d-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="4537d-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4537d-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="4537d-112">Technologies</span></span>

-   [<span data-ttu-id="4537d-113">Cómo: crear una textura</span><span class="sxs-lookup"><span data-stu-id="4537d-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="4537d-114">Cómo: inicializar una textura mediante programación</span><span class="sxs-lookup"><span data-stu-id="4537d-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="4537d-115">Cómo: crear un búfer de constantes</span><span class="sxs-lookup"><span data-stu-id="4537d-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="4537d-116">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4537d-116">Prerequisites</span></span>

<span data-ttu-id="4537d-117">Suponemos que estás familiarizado con C++.</span><span class="sxs-lookup"><span data-stu-id="4537d-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="4537d-118">También necesitas tener experiencia básica en los conceptos de programación de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="4537d-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="4537d-119">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="4537d-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="4537d-120">Paso 1: especificar el uso dinámico</span><span class="sxs-lookup"><span data-stu-id="4537d-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="4537d-121">Si desea que la aplicación pueda realizar cambios en los recursos, debe especificar esos recursos como dinámicos y que se pueden escribir al crearlos.</span><span class="sxs-lookup"><span data-stu-id="4537d-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="4537d-122">**Para especificar el uso dinámico**</span><span class="sxs-lookup"><span data-stu-id="4537d-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="4537d-123">Especifique el uso de recursos como dinámico.</span><span class="sxs-lookup"><span data-stu-id="4537d-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="4537d-124">Por ejemplo, especifique el [**valor \_ \_ dinámico D3D11 Usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) en el miembro **Usage** de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para un búfer de vértice o de constante y especifique el valor **\_ \_ dinámico de uso de D3D11** en el miembro **Usage** de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para una textura 2D.</span><span class="sxs-lookup"><span data-stu-id="4537d-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="4537d-125">Especifique el recurso como grabable.</span><span class="sxs-lookup"><span data-stu-id="4537d-125">Specify the resource as writable.</span></span> <span data-ttu-id="4537d-126">Por ejemplo, especifique el valor de [**D3D11 \_ CPU \_ Access \_ Write**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) en el miembro **CPUAccessFlags** de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) o [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span><span class="sxs-lookup"><span data-stu-id="4537d-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="4537d-127">Pase la descripción del recurso a la función de creación.</span><span class="sxs-lookup"><span data-stu-id="4537d-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="4537d-128">Por ejemplo, pase la dirección de [**D3D11 \_ buffer \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) y pase la dirección de [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="4537d-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="4537d-129">Este es un ejemplo de cómo crear un búfer de vértice dinámico:</span><span class="sxs-lookup"><span data-stu-id="4537d-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="4537d-130">Paso 2: cambiar un recurso dinámico</span><span class="sxs-lookup"><span data-stu-id="4537d-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="4537d-131">Si especificó un recurso como dinámico y grabable cuando lo creó, puede realizar cambios más adelante en ese recurso.</span><span class="sxs-lookup"><span data-stu-id="4537d-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="4537d-132">**Para cambiar los datos de un recurso dinámico**</span><span class="sxs-lookup"><span data-stu-id="4537d-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="4537d-133">Configure los nuevos datos para el recurso.</span><span class="sxs-lookup"><span data-stu-id="4537d-133">Set up the new data for the resource.</span></span> <span data-ttu-id="4537d-134">Declare una variable de tipo [**\_ \_ subrecurso D3D11 asignada**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialícela en cero.</span><span class="sxs-lookup"><span data-stu-id="4537d-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="4537d-135">Usará esta variable para cambiar el recurso.</span><span class="sxs-lookup"><span data-stu-id="4537d-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="4537d-136">Deshabilite el acceso de la unidad de procesamiento de gráficos (GPU) a los datos que desea cambiar y obtenga un puntero a la memoria que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="4537d-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="4537d-137">Para obtener este puntero, pase [**el \_ \_ \_ descartado de escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) al parámetro *mapType* cuando llame a [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="4537d-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="4537d-138">Establezca este puntero en la dirección de la variable de [**\_ \_ subrecurso asignada D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) del paso anterior.</span><span class="sxs-lookup"><span data-stu-id="4537d-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="4537d-139">Escriba los nuevos datos en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4537d-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="4537d-140">Llame a [**ID3D11DeviceContext::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) unwith para volver a habilitar el acceso de GPU a los datos cuando haya terminado de escribir los datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="4537d-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="4537d-141">Este es un ejemplo de cómo cambiar un búfer de vértice dinámico:</span><span class="sxs-lookup"><span data-stu-id="4537d-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="4537d-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4537d-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="4537d-143">Usar texturas dinámicas</span><span class="sxs-lookup"><span data-stu-id="4537d-143">Using dynamic textures</span></span>

<span data-ttu-id="4537d-144">Se recomienda crear solo una textura dinámica por formato y, posiblemente, por tamaño.</span><span class="sxs-lookup"><span data-stu-id="4537d-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="4537d-145">No se recomienda crear mapas de MIP, cubos y volúmenes dinámicos debido a la sobrecarga adicional en la asignación de todos los niveles.</span><span class="sxs-lookup"><span data-stu-id="4537d-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="4537d-146">En el caso de los mapas MIP, puede especificar el [**\_ \_ \_ descartado de escritura de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) solo en el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4537d-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="4537d-147">Todos los niveles se descartan asignando solo el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4537d-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="4537d-148">Este comportamiento es el mismo para los volúmenes y los cubos.</span><span class="sxs-lookup"><span data-stu-id="4537d-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="4537d-149">En el caso de los cubos, se asignan el nivel superior y la esfera 0.</span><span class="sxs-lookup"><span data-stu-id="4537d-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="4537d-150">Usar búferes dinámicos</span><span class="sxs-lookup"><span data-stu-id="4537d-150">Using dynamic buffers</span></span>

<span data-ttu-id="4537d-151">Cuando se llama a [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) en un búfer de vértices estático mientras la GPU usa el búfer, se obtiene una penalización significativa del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4537d-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="4537d-152">En esta situación, la **asignación** debe esperar hasta que la GPU termine de leer los datos de vértices o índices del búfer antes de que la **asignación** pueda volver a la aplicación que realiza la llamada, lo que produce un retraso significativo.</span><span class="sxs-lookup"><span data-stu-id="4537d-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="4537d-153">La llamada a la **asignación** y, a continuación, la representación de un búfer estático varias veces por fotograma también impide que la GPU almacene en búfer comandos de representación porque debe finalizar los comandos antes de devolver el puntero de mapa.</span><span class="sxs-lookup"><span data-stu-id="4537d-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="4537d-154">Sin comandos almacenados en búfer, la GPU permanece inactiva hasta que la aplicación termina de llenar el búfer de vértices o el búfer de índice y emite un comando de representación.</span><span class="sxs-lookup"><span data-stu-id="4537d-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="4537d-155">Idealmente, los datos de vértices o índices nunca cambiarían, pero esto no siempre es posible.</span><span class="sxs-lookup"><span data-stu-id="4537d-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="4537d-156">Hay muchas situaciones en las que la aplicación necesita cambiar los datos de vértices o índices en cada fotograma, quizás incluso varias veces por fotograma.</span><span class="sxs-lookup"><span data-stu-id="4537d-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="4537d-157">En estas situaciones, se recomienda crear el búfer de vértice o de índice con [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="4537d-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="4537d-158">Esta marca de uso hace que el tiempo de ejecución se optimice para las operaciones de asignación frecuentes.</span><span class="sxs-lookup"><span data-stu-id="4537d-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="4537d-159">**D3D11 \_ USAGE \_ Dynamic** solo es útil cuando el búfer se asigna con frecuencia; Si los datos van a permanecer constantes, coloque los datos en un vértice estático o en un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="4537d-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="4537d-160">Para obtener una mejora del rendimiento cuando se usan búferes de vértices dinámicos, la aplicación debe llamar a [**map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) con los valores de [**\_ asignación D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) adecuados.</span><span class="sxs-lookup"><span data-stu-id="4537d-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="4537d-161">[**D3D11 \_ \_ \_ Descartar escritura de asignación**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que la aplicación no necesita mantener los datos de índice o vértice antiguos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4537d-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="4537d-162">Si la GPU todavía usa el búfer al llamar a **map** con **D3D11 \_ map \_ Write \_ discard**, el tiempo de ejecución devuelve un puntero a una nueva región de memoria en lugar de los datos de búfer antiguos.</span><span class="sxs-lookup"><span data-stu-id="4537d-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="4537d-163">Esto permite que la GPU siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer.</span><span class="sxs-lookup"><span data-stu-id="4537d-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="4537d-164">No se requiere ninguna administración de memoria adicional en la aplicación; el búfer antiguo se reutiliza o se destruye automáticamente cuando la GPU finaliza con él.</span><span class="sxs-lookup"><span data-stu-id="4537d-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="4537d-165">Cuando se asigna un búfer con [**el \_ \_ \_ descartado de escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), el tiempo de ejecución siempre descarta todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="4537d-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="4537d-166">No se puede conservar la información en áreas sin asignar del búfer mediante la especificación de un campo de desplazamiento distinto de cero o de tamaño limitado.</span><span class="sxs-lookup"><span data-stu-id="4537d-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="4537d-167">Hay casos en los que la cantidad de datos que la aplicación necesita almacenar por asignación es pequeña, como agregar cuatro vértices para representar un Sprite.</span><span class="sxs-lookup"><span data-stu-id="4537d-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="4537d-168">[**D3D11 \_ La \_ escritura de asignación \_ no \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) sobrescribir indica que la aplicación no sobrescribirá los datos que ya se estén usando en el búfer dinámico.</span><span class="sxs-lookup"><span data-stu-id="4537d-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="4537d-169">La llamada de [**asignación**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) devolverá un puntero a los datos antiguos, lo que permitirá a la aplicación agregar nuevos datos en regiones no utilizadas del búfer de vértice o de índice.</span><span class="sxs-lookup"><span data-stu-id="4537d-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="4537d-170">La aplicación no debe modificar los vértices ni los índices que se usan en una operación de dibujo, ya que es posible que la GPU siga utilizándolos.</span><span class="sxs-lookup"><span data-stu-id="4537d-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="4537d-171">Se recomienda que la aplicación use [**\_ \_ \_ descartar escritura de asignación de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) después de que el búfer dinámico esté lleno para recibir una nueva región de memoria, que descarta los datos de vértice o de vértice antiguos una vez finalizada la GPU.</span><span class="sxs-lookup"><span data-stu-id="4537d-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="4537d-172">El mecanismo de consulta asincrónico es útil para determinar si la GPU todavía está usando los vértices.</span><span class="sxs-lookup"><span data-stu-id="4537d-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="4537d-173">Emita una consulta de tipo [**\_ \_ evento de consulta D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) después de la última llamada a Draw que use los vértices.</span><span class="sxs-lookup"><span data-stu-id="4537d-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="4537d-174">Los vértices ya no se usan cuando [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) devuelve S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="4537d-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="4537d-175">Cuando asigne un búfer con los [**valores \_ \_ \_ descartados de escritura de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) o sin valores de asignación, siempre se garantiza que los vértices se sincronizan correctamente con la GPU.</span><span class="sxs-lookup"><span data-stu-id="4537d-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="4537d-176">Sin embargo, cuando se asignan sin valores de mapa, se incurrirá en la penalización de rendimiento que se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4537d-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="4537d-177">El tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8, habilita la asignación de búferes de constantes dinámicos y vistas de recursos de sombreador (SRVs) de búferes dinámicos con D3D11 no se sobrescribe la [**\_ \_ escritura de \_ \_ asignación**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span><span class="sxs-lookup"><span data-stu-id="4537d-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="4537d-178">En los tiempos de ejecución de Direct3D 11 y versiones anteriores, la asignación de actualización parcial no se sobrescribe en los búferes de vértices o índices.</span><span class="sxs-lookup"><span data-stu-id="4537d-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="4537d-179">Para determinar si un dispositivo Direct3D admite estas características, llame a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones D3D11 de la característica D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="4537d-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="4537d-180">**CheckFeatureSupport** rellena los miembros de una estructura de [**\_ \_ \_ \_ Opciones D3D11 de datos de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) con las características del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4537d-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="4537d-181">Los miembros pertinentes aquí son **MapNoOverwriteOnDynamicConstantBuffer** y **MapNoOverwriteOnDynamicBufferSRV**.</span><span class="sxs-lookup"><span data-stu-id="4537d-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4537d-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4537d-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4537d-183">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4537d-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 





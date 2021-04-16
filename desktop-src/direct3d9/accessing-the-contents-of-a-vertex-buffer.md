---
description: Los objetos de búfer de vértice permiten a las aplicaciones acceder directamente a la memoria asignada para los datos de vértices.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Acceder al contenido de un búfer de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677225"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="e129c-103">Acceder al contenido de un búfer de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e129c-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="e129c-104">Los objetos de búfer de vértice permiten a las aplicaciones acceder directamente a la memoria asignada para los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="e129c-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="e129c-105">Puede recuperar un puntero a la memoria del búfer de vértices llamando al método [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) y, a continuación, accediendo a la memoria según sea necesario para rellenar el búfer con nuevos datos de vértice o para leer los datos que ya contiene.</span><span class="sxs-lookup"><span data-stu-id="e129c-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="e129c-106">El método **IDirect3DVertexBuffer9:: Lock** acepta cuatro parámetros.</span><span class="sxs-lookup"><span data-stu-id="e129c-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="e129c-107">El primero, *OffsetToLock*, es el desplazamiento en los datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="e129c-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="e129c-108">El segundo parámetro es el tamaño, medido en bytes, de los datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="e129c-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="e129c-109">El tercer parámetro aceptado es la dirección de un puntero que apunta a los datos del vértice, si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e129c-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="e129c-110">El último parámetro, *Flags*, indica al sistema cómo debe bloquearse la memoria.</span><span class="sxs-lookup"><span data-stu-id="e129c-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="e129c-111">Especifique las constantes del parámetro *Flags* según la forma en que se tendrá acceso a los datos de vértice.</span><span class="sxs-lookup"><span data-stu-id="e129c-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="e129c-112">Asegúrese de que el valor elegido para [**D3DUSAGE**](d3dusage.md) coincide con el valor elegido para [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="e129c-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="e129c-113">Por ejemplo, si va a crear un búfer de vértices solo con acceso de escritura, no tiene sentido intentar leer los datos mediante la especificación de D3DLOCK \_ ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="e129c-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="e129c-114">El uso de estas marcas permite que el controlador bloquee la memoria y proporcione el mejor rendimiento, dado el tipo de acceso solicitado.</span><span class="sxs-lookup"><span data-stu-id="e129c-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="e129c-115">Cuando termine de rellenar o leer los datos de los vértices, llame al método [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , tal como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="e129c-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="e129c-116">Si crea un búfer de vértice con la \_ marca WRITEONLY de D3DUSAGE, no use la \_ marca de bloqueo de solo lectura D3DLOCK.</span><span class="sxs-lookup"><span data-stu-id="e129c-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="e129c-117">Use la \_ marca ReadOnly de D3DLOCK si la aplicación solo va a leer desde la memoria del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="e129c-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="e129c-118">La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e129c-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="e129c-119">Vea [uso de los búferes de índice y vértices dinámicos](performance-optimizations.md) para obtener información sobre el uso de D3DLOCK \_ discard o D3DLOCK \_ NOOVERWRITE para el parámetro flags de [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span><span class="sxs-lookup"><span data-stu-id="e129c-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="e129c-120">En C++, dado que tiene acceso directo a la memoria asignada para el búfer de vértices, asegúrese de que la aplicación tenga acceso correctamente a la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="e129c-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="e129c-121">De lo contrario, se arriesga a representar que la memoria no es válida.</span><span class="sxs-lookup"><span data-stu-id="e129c-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="e129c-122">Use el paso del formato de vértice que usa la aplicación para pasar de un vértice del búfer asignado a otro.</span><span class="sxs-lookup"><span data-stu-id="e129c-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="e129c-123">La memoria del búfer de vértices es una matriz simple de vértices especificada en FVF.</span><span class="sxs-lookup"><span data-stu-id="e129c-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="e129c-124">Use el paso de cualquier estructura de formato de vértice que defina.</span><span class="sxs-lookup"><span data-stu-id="e129c-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="e129c-125">Puede calcular el paso de cada vértice en tiempo de ejecución examinando el [D3DFVF](d3dfvf.md) contenido en la descripción del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="e129c-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="e129c-126">En la tabla siguiente se muestra el tamaño de cada componente de vértice.</span><span class="sxs-lookup"><span data-stu-id="e129c-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="e129c-127">Marca de formato de vértice</span><span class="sxs-lookup"><span data-stu-id="e129c-127">Vertex Format Flag</span></span> | <span data-ttu-id="e129c-128">Tamaño</span><span class="sxs-lookup"><span data-stu-id="e129c-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="e129c-129">\_Difusión D3DFVF</span><span class="sxs-lookup"><span data-stu-id="e129c-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="e129c-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e129c-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="e129c-131">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="e129c-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="e129c-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="e129c-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="e129c-133">\_Reflejo D3DFVF</span><span class="sxs-lookup"><span data-stu-id="e129c-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="e129c-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="e129c-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="e129c-135">D3DFVF \_ TEXn</span><span class="sxs-lookup"><span data-stu-id="e129c-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="e129c-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="e129c-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="e129c-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="e129c-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="e129c-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="e129c-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="e129c-139">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="e129c-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="e129c-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="e129c-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="e129c-141">El número de coordenadas de textura presente en el formato de vértice se describe mediante las \_ marcas D3DFVF Tex n (donde n es un valor comprendido entre 0 y 8).</span><span class="sxs-lookup"><span data-stu-id="e129c-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="e129c-142">Multiplicar el número de conjuntos de coordenadas de textura por el tamaño de un conjunto de coordenadas de textura, que puede oscilar entre uno y cuatro valores flotantes, para calcular la memoria necesaria para ese número de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="e129c-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="e129c-143">Use el intervalo total de vértices para aumentar y disminuir el puntero de memoria según sea necesario para tener acceso a vértices determinados.</span><span class="sxs-lookup"><span data-stu-id="e129c-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="e129c-144">Recuperar descripciones del búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="e129c-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="e129c-145">Puede recuperar información sobre un búfer de vértice llamando al método [**IDirect3DVertexBuffer9:: GetDesc**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e129c-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e129c-146">Este método rellena los miembros de la estructura [**D3DVERTEXBUFFER \_ DESC**](d3dvertexbuffer-desc.md) con información sobre el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="e129c-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e129c-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e129c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e129c-148">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="e129c-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 

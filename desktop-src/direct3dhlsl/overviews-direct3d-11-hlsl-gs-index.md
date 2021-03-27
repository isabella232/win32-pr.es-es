---
title: Cómo indizar varios flujos de salida
description: En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 flujos independientes. Esto significa que un solo sombreador puede generar un resultado entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075195"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="f0b3a-104">Cómo: indizar varios flujos de salida</span><span class="sxs-lookup"><span data-stu-id="f0b3a-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="f0b3a-105">En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 flujos independientes.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="f0b3a-106">Esto significa que un solo sombreador puede generar un resultado entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="f0b3a-107">Para indizar varios flujos de salida</span><span class="sxs-lookup"><span data-stu-id="f0b3a-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="f0b3a-108">Defina un flujo de datos mediante un tipo de plantilla de flujo.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="f0b3a-109">Defina un segundo flujo de datos mediante un tipo de plantilla de flujo.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="f0b3a-110">Los datos se envían a las secuencias (o ambas) mediante las funciones intrínsecas del objeto de salida de flujo (como Append o RestartStrip).</span><span class="sxs-lookup"><span data-stu-id="f0b3a-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="f0b3a-111">Al usar un solo flujo de salida, puede emitir tiras de triángulo, tiras de líneas o listas de puntos.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="f0b3a-112">Cuando se almacenan bandas de triángulo y de línea en el búfer de flujo de salida, se expanden a listas de triángulos y líneas, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="f0b3a-113">También puede rasterizar una secuencia y no enviarla a un búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="f0b3a-114">Cuando se usan varios flujos de salida, todos los flujos deben contener puntos y hasta un flujo de salida se puede enviar al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="f0b3a-115">Lo más habitual es que una aplicación no rasterizará ningún flujo.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="f0b3a-116">Después de transmitir los datos a un búfer, puede usar esos datos para representar cualquier tipo primitivo, no solo el tipo primitivo que usó para rellenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="f0b3a-117">La salida total del sombreador de geometría está limitada a 1024 escalares.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="f0b3a-118">Cuando existen varias secuencias, el número de escalares se calcula a partir del tipo de flujo más grande multiplicado por el número máximo de vértices.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0b3a-119">Diferencias entre el modelo de sombreador 4 y el modelo de sombreador 5:</span><span class="sxs-lookup"><span data-stu-id="f0b3a-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="f0b3a-120">Modelo de sombreador 4:</span><span class="sxs-lookup"><span data-stu-id="f0b3a-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="f0b3a-121">El número máximo de escalas para la salida de flujo es 64.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="f0b3a-122">La máscara de registro por componente debe coincidir en el intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="f0b3a-123">Modelo de sombreador 5:</span><span class="sxs-lookup"><span data-stu-id="f0b3a-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="f0b3a-124">El número máximo de escalas para la salida de flujo es 128.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="f0b3a-125">No es necesario que la máscara de registro por componente coincida en el intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="f0b3a-126">La indexación dinámica de salidas debe ser válida en todas las secuencias.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="f0b3a-127">No es necesario que los modos de interpolación coincidan con las secuencias.</span><span class="sxs-lookup"><span data-stu-id="f0b3a-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f0b3a-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f0b3a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b3a-129">Características del sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f0b3a-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 






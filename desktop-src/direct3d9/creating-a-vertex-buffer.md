---
description: 'Cree un objeto de búfer de vértices llamando al método IDirect3DDevice9:: CreateVertexBuffer, que acepta cinco parámetros.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Crear un búfer de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714877"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="652ca-103">Crear un búfer de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="652ca-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="652ca-104">Cree un objeto de búfer de vértices llamando al método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , que acepta cinco parámetros.</span><span class="sxs-lookup"><span data-stu-id="652ca-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="652ca-105">El primer parámetro especifica la longitud del búfer de vértices, en bytes.</span><span class="sxs-lookup"><span data-stu-id="652ca-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="652ca-106">Use el operador sizeof para determinar el tamaño de un formato de vértice, en bytes.</span><span class="sxs-lookup"><span data-stu-id="652ca-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="652ca-107">Tenga en cuenta el siguiente formato de vértice personalizado.</span><span class="sxs-lookup"><span data-stu-id="652ca-107">Consider the following custom vertex format.</span></span>


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



<span data-ttu-id="652ca-108">Para crear un búfer de vértices que contenga cuatro estructuras CUSTOMVERTEX, especifique \[ 4 \* SIZEOF (CUSTOMVERTEX) \] para el parámetro de *longitud* .</span><span class="sxs-lookup"><span data-stu-id="652ca-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="652ca-109">El segundo parámetro es un conjunto de controles de uso.</span><span class="sxs-lookup"><span data-stu-id="652ca-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="652ca-110">Entre otras cosas, su valor determina si el búfer de vértices es capaz de contener información de recorte, en forma de marcas de recorte, para los vértices que existen fuera del área de visualización.</span><span class="sxs-lookup"><span data-stu-id="652ca-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="652ca-111">Para crear un búfer de vértices que no puede contener marcas de recorte, incluya la \_ marca D3DUSAGE DONOTCLIP para el parámetro *Usage* .</span><span class="sxs-lookup"><span data-stu-id="652ca-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="652ca-112">La \_ marca D3DUSAGE DONOTCLIP solo se aplica si también indica que el búfer de vértice contendrá vértices transformados \_ . la marca D3DFVF XYZRHW se incluye en el parámetro *FVF* .</span><span class="sxs-lookup"><span data-stu-id="652ca-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="652ca-113">El método [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) omite la marca D3DUSAGE \_ DONOTCLIP si indica que el búfer contendrá vértices sin transformar (la marca de D3DFVF \_ XYZ).</span><span class="sxs-lookup"><span data-stu-id="652ca-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="652ca-114">Las marcas de recorte ocupan memoria adicional, lo que permite que un búfer de vértice compatible con el recorte sea ligeramente mayor que un búfer de vértices que no puede contener marcas de recorte.</span><span class="sxs-lookup"><span data-stu-id="652ca-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="652ca-115">Dado que estos recursos se asignan al crear el búfer de vértices, debe solicitar un búfer de vértice compatible con el recorte con anterioridad.</span><span class="sxs-lookup"><span data-stu-id="652ca-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="652ca-116">El tercer parámetro, *FVF*, es una combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértices del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="652ca-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="652ca-117">Si especifica 0 para este parámetro, el búfer de vértices es un búfer de vértices que no es FVF.</span><span class="sxs-lookup"><span data-stu-id="652ca-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="652ca-118">Para obtener más información, vea [búferes de vértices de FVF (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="652ca-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="652ca-119">El cuarto parámetro describe la clase de memoria en la que se coloca el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="652ca-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="652ca-120">El último parámetro que [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) acepta es la dirección de una variable que se rellenará con un puntero a la nueva interfaz [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) del objeto de búfer de vértices si la llamada se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="652ca-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="652ca-121">No se pueden generar marcas de recorte para un búfer de vértice creado sin su compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="652ca-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="652ca-122">En el ejemplo de código de C++ siguiente se muestra cómo la creación de un búfer de vértices podría ser similar en el código.</span><span class="sxs-lookup"><span data-stu-id="652ca-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a><span data-ttu-id="652ca-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="652ca-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="652ca-124">Búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="652ca-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 

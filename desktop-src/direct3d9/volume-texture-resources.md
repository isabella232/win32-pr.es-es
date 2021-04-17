---
description: Las texturas de volumen son colecciones tridimensionales de píxeles (textura) que se pueden usar para pintar un primitivo bidimensional, como un triángulo o una línea.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Recursos de textura de volumen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564695"
---
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="b603a-103">Recursos de textura de volumen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b603a-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="b603a-104">Las texturas de volumen son colecciones tridimensionales de píxeles (textura) que se pueden usar para pintar un primitivo bidimensional, como un triángulo o una línea.</span><span class="sxs-lookup"><span data-stu-id="b603a-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="b603a-105">Se requieren coordenadas de textura de tres elementos para cada vértice de una primitiva que se va a texturar con un volumen.</span><span class="sxs-lookup"><span data-stu-id="b603a-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="b603a-106">A medida que se dibuja el primitivo, cada píxel contenido se rellena con el valor de color de algún píxel dentro del volumen, de acuerdo con las reglas análogas al caso de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="b603a-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="b603a-107">Los volúmenes no se representan directamente porque no hay primitivas tridimensionales que se puedan pintar con ellos.</span><span class="sxs-lookup"><span data-stu-id="b603a-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="b603a-108">Puede usar texturas de volumen para efectos especiales como la niebla de revisión, las explosiones, etc.</span><span class="sxs-lookup"><span data-stu-id="b603a-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="b603a-109">Los volúmenes se organizan en segmentos y se pueden considerar como superficies 2D de alto ancho x apiladas para crear un volumen x alto x de profundidad.</span><span class="sxs-lookup"><span data-stu-id="b603a-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="b603a-110">Cada segmento es una sola fila.</span><span class="sxs-lookup"><span data-stu-id="b603a-110">Each slice is a single row.</span></span> <span data-ttu-id="b603a-111">Los volúmenes pueden tener niveles posteriores en los que las dimensiones de cada nivel se truncan a la mitad de las dimensiones del nivel anterior.</span><span class="sxs-lookup"><span data-stu-id="b603a-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="b603a-112">En el diagrama siguiente se muestra el aspecto de una textura de volumen con varios niveles.</span><span class="sxs-lookup"><span data-stu-id="b603a-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![diagrama de una textura de volumen con representaciones de cubo 8x2x4, 4x1x2 y 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="b603a-114">Crear una textura de volumen</span><span class="sxs-lookup"><span data-stu-id="b603a-114">Creating a Volume Texture</span></span>

<span data-ttu-id="b603a-115">En los ejemplos de código siguientes se muestran los pasos necesarios para usar una textura de volumen.</span><span class="sxs-lookup"><span data-stu-id="b603a-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="b603a-116">En primer lugar, especifique un tipo de vértice personalizado que tenga tres coordenadas de textura para cada vértice, tal como se muestra en este ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b603a-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



<span data-ttu-id="b603a-117">A continuación, rellene los vértices con datos.</span><span class="sxs-lookup"><span data-stu-id="b603a-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="b603a-118">Ahora, cree un búfer de vértices y rellénelo con los datos de los vértices.</span><span class="sxs-lookup"><span data-stu-id="b603a-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="b603a-119">El siguiente paso consiste en usar el método [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para crear una textura de volumen, tal como se muestra en este ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="b603a-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="b603a-120">Antes de representar el primitivo, establezca la textura actual en la textura de volumen creada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b603a-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="b603a-121">En el ejemplo de código siguiente se muestra todo el proceso de representación de una franja de triángulos.</span><span class="sxs-lookup"><span data-stu-id="b603a-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a><span data-ttu-id="b603a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b603a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b603a-123">Texturas de Direct3D</span><span class="sxs-lookup"><span data-stu-id="b603a-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 

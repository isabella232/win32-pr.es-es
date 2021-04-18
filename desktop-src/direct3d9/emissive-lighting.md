---
description: La iluminación emisor se describe en un único término.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Iluminación emisor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714658"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="d0851-103">Iluminación emisor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0851-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="d0851-104">La iluminación emisor se describe en un único término.</span><span class="sxs-lookup"><span data-stu-id="d0851-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="d0851-105">Iluminación emisor = C ₑ</span><span class="sxs-lookup"><span data-stu-id="d0851-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="d0851-106">Donde:</span><span class="sxs-lookup"><span data-stu-id="d0851-106">Where:</span></span>



| <span data-ttu-id="d0851-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d0851-107">Parameter</span></span> | <span data-ttu-id="d0851-108">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d0851-108">Default value</span></span> | <span data-ttu-id="d0851-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0851-109">Type</span></span>          | <span data-ttu-id="d0851-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0851-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="d0851-111">C ₑ</span><span class="sxs-lookup"><span data-stu-id="d0851-111">Cₑ</span></span>        | <span data-ttu-id="d0851-112">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="d0851-112">(0,0,0,0)</span></span>     | <span data-ttu-id="d0851-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="d0851-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="d0851-114">Color de emisor.</span><span class="sxs-lookup"><span data-stu-id="d0851-114">Emissive color.</span></span> |



 

<span data-ttu-id="d0851-115">El valor de C ₑ es:</span><span class="sxs-lookup"><span data-stu-id="d0851-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="d0851-116">Vertex color1, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color1, y el primer color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="d0851-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="d0851-117">Vertex color2, si EMISSIVEMATERIALSOURCE = D3DMCS \_ color2, y el segundo color de vértice se proporciona en la declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="d0851-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="d0851-118">color de emisor de materiales</span><span class="sxs-lookup"><span data-stu-id="d0851-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="d0851-119">Si se usa la opción EMISSIVEMATERIALSOURCE y no se proporciona el color del vértice, se usa el color de emisor del material.</span><span class="sxs-lookup"><span data-stu-id="d0851-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="d0851-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0851-120">Example</span></span>

<span data-ttu-id="d0851-121">En este ejemplo, el objeto se colorea utilizando la luz ambiente de la escena y un color ambiente de material.</span><span class="sxs-lookup"><span data-stu-id="d0851-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="d0851-122">A continuación se muestra el código.</span><span class="sxs-lookup"><span data-stu-id="d0851-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="d0851-123">Según la ecuación, el color resultante para los vértices del objeto es el color del material.</span><span class="sxs-lookup"><span data-stu-id="d0851-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="d0851-124">En la ilustración siguiente se muestra el color del material, que es verde.</span><span class="sxs-lookup"><span data-stu-id="d0851-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="d0851-125">Emisor light ilumina todos los vértices de objeto con el mismo color.</span><span class="sxs-lookup"><span data-stu-id="d0851-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="d0851-126">No depende de la dirección de la luz o del vértice normal.</span><span class="sxs-lookup"><span data-stu-id="d0851-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="d0851-127">Como resultado, la esfera tiene el aspecto de un círculo 2D porque no hay ninguna diferencia en el sombreado en torno a la superficie del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0851-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![Ilustración de una esfera verde](images/lighte.jpg)

<span data-ttu-id="d0851-129">En la ilustración siguiente se muestra cómo la luz emisor se combina con los otros tres tipos de luces, en los ejemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="d0851-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="d0851-130">En el lado derecho de la esfera, hay una mezcla de los emisor verdes y la luz ambiental roja.</span><span class="sxs-lookup"><span data-stu-id="d0851-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="d0851-131">En el lado izquierdo de la esfera, la luz verde emisor se combina con ambiente rojo y luz difusa que produce un degradado rojo.</span><span class="sxs-lookup"><span data-stu-id="d0851-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="d0851-132">El resaltado especular está en blanco en el centro y crea un anillo amarillo a medida que el valor de la luz especular cae claramente al salir de los valores de la luz ambiente, difusos y emisors que se mezclan para hacer amarillo.</span><span class="sxs-lookup"><span data-stu-id="d0851-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![Ilustración de una esfera verde con emisor claro](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="d0851-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0851-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0851-135">Matemáticas de iluminación</span><span class="sxs-lookup"><span data-stu-id="d0851-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 




---
title: Coordenadas de textura generadas automáticamente (Direct3D 9)
description: El sistema puede usar la posición de espacio de cámara transformada o la normal de un vértice como coordenadas de textura, o bien puede calcular los tres vectores de elemento utilizados para abordar un mapa de entorno cúbico.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01addbe354fb910ef68e1fc693e7dfffb1ceacf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843296"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a><span data-ttu-id="3cb78-103">Coordenadas de textura generadas automáticamente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3cb78-103">Auto-generated texture coordinates (Direct3D 9)</span></span>

<span data-ttu-id="3cb78-104">El sistema puede usar la posición de espacio de cámara transformada o la normal de un vértice como coordenadas de textura, o bien puede calcular los tres vectores de elemento utilizados para abordar un mapa de entorno cúbico.</span><span class="sxs-lookup"><span data-stu-id="3cb78-104">The system can use the transformed camera-space position or the normal from a vertex as texture coordinates, or it can compute the three element vectors used to address a cubic environment map.</span></span> <span data-ttu-id="3cb78-105">Al igual que las coordenadas de textura que se especifican explícitamente en un vértice, puede usar coordenadas de textura generadas automáticamente como entrada para las transformaciones de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3cb78-105">Like texture coordinates that you explicitly specify in a vertex, you can use automatically generated texture coordinates as input for texture coordinate transformations.</span></span>

<span data-ttu-id="3cb78-106">Las coordenadas de textura generadas automáticamente pueden reducir significativamente el ancho de banda necesario para los datos de geometría al eliminar la necesidad de coordenadas de textura explícitas en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="3cb78-106">Automatically generated texture coordinates can significantly reduce the bandwidth required for geometry data by eliminating the need for explicit texture coordinates in the vertex format.</span></span> <span data-ttu-id="3cb78-107">En muchos casos, las coordenadas de textura que genera el sistema se pueden usar con transformaciones para producir efectos especiales.</span><span class="sxs-lookup"><span data-stu-id="3cb78-107">In many cases, the texture coordinates that the system generates can be used with transformations to produce special effects.</span></span> <span data-ttu-id="3cb78-108">Por supuesto, se trata de una característica de propósito especial y usará coordenadas de textura explícitas en muchas ocasiones.</span><span class="sxs-lookup"><span data-stu-id="3cb78-108">Of course, this is a special-purpose feature, and you will use explicit texture coordinates for many occasions.</span></span>

## <a name="configuring-automatically-generated-texture-coordinates"></a><span data-ttu-id="3cb78-109">Configuración de coordenadas de textura generadas automáticamente</span><span class="sxs-lookup"><span data-stu-id="3cb78-109">Configuring Automatically Generated Texture Coordinates</span></span>

<span data-ttu-id="3cb78-110">En C++, el estado de la fase de textura D3DTSS \_ TEXCOORDINDEX (del tipo enumerado [**D3DTEXTURESTAGESTATETYPE)**](./d3dtexturestagestatetype.md) controla cómo el sistema genera coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3cb78-110">In C++, the D3DTSS\_TEXCOORDINDEX texture-stage state (from the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type) controls how the system generates texture coordinates.</span></span>

<span data-ttu-id="3cb78-111">Normalmente, este estado indica al sistema que use un conjunto determinado de coordenadas de textura codificadas en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="3cb78-111">Normally, this state instructs the system to use a particular set of texture coordinates encoded in the vertex format.</span></span> <span data-ttu-id="3cb78-112">Cuando se incluyen las marcas \_ \_ CAMERASPACENORMAL, D3DTSS \_ TCI CAMERASPACEPOSITION o \_ D3DTSS \_ TCI CAMERASPACEREFLECTIONVECTOR de D3DTSS \_ en el valor que se asigna a este estado, el comportamiento del sistema es bastante diferente.</span><span class="sxs-lookup"><span data-stu-id="3cb78-112">When you include the D3DTSS\_TCI\_CAMERASPACENORMAL, D3DTSS\_TCI\_CAMERASPACEPOSITION, or D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR flags in the value that you assign to this state, the system behavior is quite different.</span></span> <span data-ttu-id="3cb78-113">Si alguna de estas marcas está presente, la fase de textura omite las coordenadas de textura dentro del formato de vértice en favor de las coordenadas que genera el sistema.</span><span class="sxs-lookup"><span data-stu-id="3cb78-113">If any of these flags are present, the texture stage ignores the texture coordinates within the vertex format in favor of coordinates that the system generates.</span></span> <span data-ttu-id="3cb78-114">Los significados de cada marca se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="3cb78-114">The meanings for each flag are shown in the following list.</span></span>

-   <span data-ttu-id="3cb78-115">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="3cb78-115">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>

    <span data-ttu-id="3cb78-116">Use el vértice normal, transformado en espacio de la cámara, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="3cb78-116">Use the vertex normal, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="3cb78-117">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="3cb78-117">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>

    <span data-ttu-id="3cb78-118">Use la posición del vértice, transformada en espacio de la cámara, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="3cb78-118">Use the vertex position, transformed to camera space, as input texture coordinates.</span></span>

-   <span data-ttu-id="3cb78-119">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="3cb78-119">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span>

    <span data-ttu-id="3cb78-120">Use el vector de reflexión, transformado en espacio de la cámara, como coordenadas de textura de entrada.</span><span class="sxs-lookup"><span data-stu-id="3cb78-120">Use the reflection vector, transformed to camera space, as input texture coordinates.</span></span> <span data-ttu-id="3cb78-121">El vector de reflexión se calcula a partir de la posición del vértice de entrada y el vector normal.</span><span class="sxs-lookup"><span data-stu-id="3cb78-121">The reflection vector is computed from the input vertex position and normal vector.</span></span>

<span data-ttu-id="3cb78-122">Las marcas de índice de coordenadas de textura son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="3cb78-122">The texture coordinate index flags are mutually exclusive.</span></span> <span data-ttu-id="3cb78-123">En este ejemplo se usa:</span><span class="sxs-lookup"><span data-stu-id="3cb78-123">This example uses:</span></span>

-   <span data-ttu-id="3cb78-124">Posición del vértice (en el espacio de la cámara) como coordenadas de textura de entrada para esta fase de textura</span><span class="sxs-lookup"><span data-stu-id="3cb78-124">The vertex position (in camera-space) as the input texture coordinates for this texture stage</span></span>
-   <span data-ttu-id="3cb78-125">El modo de encapsulado establecido en el estado de representación D3DRENDERSTATE \_ WRAP1</span><span class="sxs-lookup"><span data-stu-id="3cb78-125">The wrap mode set in the D3DRENDERSTATE\_WRAP1 render state</span></span>


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



<span data-ttu-id="3cb78-126">Las coordenadas de textura generadas automáticamente son más útiles como valores de entrada para una transformación de coordenadas de textura o para eliminar la necesidad de que la aplicación calcule vectores de tres elementos para mapas de entorno cúbica.</span><span class="sxs-lookup"><span data-stu-id="3cb78-126">Automatically generated texture coordinates are most useful as input values for a texture coordinate transformation, or to eliminate the need for your application to compute three-element vectors for cubic-environment maps.</span></span>

<span data-ttu-id="3cb78-127">La asignación de esferas usa un mapa de textura precalutizado (en tiempo de modelo) que contiene todo el entorno tal y como se refleja en una esfera de chrome.</span><span class="sxs-lookup"><span data-stu-id="3cb78-127">Sphere-mapping uses a precomputed (at model time) texture map that contains the entire environment as reflected by a chrome sphere.</span></span> <span data-ttu-id="3cb78-128">Direct3D tiene una característica de generación de coordenadas de textura mediante el estado de representación D3DTSS \_ TCI CAMERASPACENORMAL, que toma la normalidad del vértice en el espacio de la cámara y la coloca a través de una transformación de textura para generar coordenadas de \_ textura.</span><span class="sxs-lookup"><span data-stu-id="3cb78-128">Direct3D has a texture-coordinate generation feature using render state D3DTSS\_TCI\_CAMERASPACENORMAL, which takes the normal of the vertex in camera space and puts it through a texture transform to generate texture coordinates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3cb78-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3cb78-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cb78-130">Procesamiento de coordenadas de textura</span><span class="sxs-lookup"><span data-stu-id="3cb78-130">Texture Coordinate Processing</span></span>](texture-coordinate-processing.md)
</dt> <dt>

[<span data-ttu-id="3cb78-131">Transformaciones de coordenadas de textura (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3cb78-131">Texture Coordinate Transformations (Direct3D 9)</span></span>](texture-coordinate-transformations.md)
</dt> <dt>

[<span data-ttu-id="3cb78-132">Asignación de entorno cúbica (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3cb78-132">Cubic Environment Mapping (Direct3D 9)</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 

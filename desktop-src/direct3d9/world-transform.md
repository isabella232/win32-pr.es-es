---
description: La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación universal.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformación universal (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422795"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="cacdb-103">Transformación universal (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cacdb-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="cacdb-104">La explicación de la transformación mundial presenta conceptos básicos y proporciona detalles sobre cómo configurar una transformación universal.</span><span class="sxs-lookup"><span data-stu-id="cacdb-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="cacdb-105">¿Qué es una transformación mundial?</span><span class="sxs-lookup"><span data-stu-id="cacdb-105">What Is a World Transform?</span></span>

<span data-ttu-id="cacdb-106">Una transformación de mundo cambia las coordenadas del espacio del modelo, donde los vértices se definen en relación con el origen local de un modelo, en el espacio universal, donde se definen los vértices en relación con un origen común a todos los objetos de una escena.</span><span class="sxs-lookup"><span data-stu-id="cacdb-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="cacdb-107">En esencia, la transformación mundial coloca un modelo en el mundo; por lo tanto, su nombre.</span><span class="sxs-lookup"><span data-stu-id="cacdb-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="cacdb-108">En el diagrama siguiente se muestra la relación entre el sistema de coordenadas universal y el sistema de coordenadas local de un modelo.</span><span class="sxs-lookup"><span data-stu-id="cacdb-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![diagrama de cómo se relacionan las coordenadas del mundo y las coordenadas locales](images/worldcrd.png)

<span data-ttu-id="cacdb-110">La transformación del mundo puede incluir cualquier combinación de traducciones, giros y escalado.</span><span class="sxs-lookup"><span data-stu-id="cacdb-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="cacdb-111">Configuración de una matriz mundial</span><span class="sxs-lookup"><span data-stu-id="cacdb-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="cacdb-112">Como con cualquier otra transformación, cree la transformación universal mediante la concatenación de una serie de matrices en una matriz única que contenga la suma total de sus efectos.</span><span class="sxs-lookup"><span data-stu-id="cacdb-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="cacdb-113">En el caso más simple, cuando un modelo está en el origen del mundo y sus ejes de coordenadas locales están orientados igual que el espacio del mundo, la matriz mundial es la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="cacdb-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="cacdb-114">Normalmente, la matriz mundial es una combinación de una traducción en el espacio universal y, posiblemente, una o más rotaciones para convertir el modelo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cacdb-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="cacdb-115">En el ejemplo siguiente, de una clase de modelo 3D ficticia escrita en C++, se usan las funciones auxiliares incluidas en la biblioteca de utilidades de D3DX para crear una matriz universal que incluye tres giros para orientar un modelo y una traslación para reubicarlo en relación con su posición en el espacio universal.</span><span class="sxs-lookup"><span data-stu-id="cacdb-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="cacdb-116">Después de preparar la matriz universal, llame al método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) para establecerla, especificando la macro [**D3DTS \_ World**](d3dts-world.md) para el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="cacdb-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="cacdb-117">Direct3D usa el mundo y las matrices de vistas que se establecen para configurar varias estructuras de datos internas.</span><span class="sxs-lookup"><span data-stu-id="cacdb-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="cacdb-118">Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas.</span><span class="sxs-lookup"><span data-stu-id="cacdb-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="cacdb-119">Establecer estas matrices con frecuencia (por ejemplo, miles de veces por fotograma) es un proceso que consume mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="cacdb-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="cacdb-120">Puede minimizar el número de cálculos necesarios concatenando el mundo y ver las matrices en una matriz de vista mundial que establezca como la matriz universal y, a continuación, estableciendo la matriz de la vista en la identidad.</span><span class="sxs-lookup"><span data-stu-id="cacdb-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="cacdb-121">Mantenga copias en caché de matrices de todo el mundo y vistas para que pueda modificar, concatenar y restablecer la matriz universal según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cacdb-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="cacdb-122">Para mayor claridad, en esta documentación los ejemplos de Direct3D raramente emplean esta optimización.</span><span class="sxs-lookup"><span data-stu-id="cacdb-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cacdb-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cacdb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cacdb-124">Transformaciones</span><span class="sxs-lookup"><span data-stu-id="cacdb-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 




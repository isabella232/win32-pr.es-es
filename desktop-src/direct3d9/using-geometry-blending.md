---
description: La siguiente estructura definida por el usuario se puede usar para los vértices que se combinarán entre dos matrices.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Usar la combinación de geometría (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705195"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="f7e6c-103">Usar la combinación de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7e6c-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="f7e6c-104">La siguiente estructura definida por el usuario se puede usar para los vértices que se combinarán entre dos matrices.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="f7e6c-105">El peso de la mezcla debe aparecer después de la posición y RHW los datos en el FVF y antes de que el vértice sea normal.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="f7e6c-106">Observe que el formato de vértice anterior solo contiene un valor de peso de fusión.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="f7e6c-107">Esto se debe a que habrá dos matrices mundiales, definidas en los Estados de transformación [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) y **D3DTS \_ WORLDMATRIX**(1).</span><span class="sxs-lookup"><span data-stu-id="f7e6c-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="f7e6c-108">El sistema combina cada vértice entre estas dos matrices usando el valor de peso único.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="f7e6c-109">En el caso de tres matrices, solo se requieren dos pesos, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="f7e6c-110">Es fácil definir pesos de la máscara.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-110">Defining skin weights is easy.</span></span> <span data-ttu-id="f7e6c-111">El uso de una función lineal de la distancia entre uniones es un buen inicio, pero una función sigmoidea más suave es mejor.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="f7e6c-112">La elección de una función de distribución de la ponderación de la piel puede producir arrugas nítidas en uniones, si es necesario, mediante una gran variación en el peso de la piel en una distancia corta.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="f7e6c-113">Establecer matrices de mezcla</span><span class="sxs-lookup"><span data-stu-id="f7e6c-113">Setting Blending Matrices</span></span>

<span data-ttu-id="f7e6c-114">Establezca las matrices de transformación entre las que el sistema se mezcla llamando al método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="f7e6c-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="f7e6c-115">Establezca el primer parámetro en un valor definido por la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) y establezca el segundo parámetro en la dirección de la matriz que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="f7e6c-116">En el siguiente ejemplo de código de C++ se establecen dos matrices mundiales, entre las que se combina la geometría para crear la ilusión de un brazo Unido.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="f7e6c-117">La configuración de una matriz de mezcla simplemente hace que el sistema almacene en caché la matriz para su uso posterior. no indica al sistema que empiece a fusionar vértices.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="f7e6c-118">Habilitar la combinación de geometría</span><span class="sxs-lookup"><span data-stu-id="f7e6c-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="f7e6c-119">La combinación de geometría está deshabilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="f7e6c-120">Para habilitar la combinación de geometría, llame al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) para establecer el \_ Estado de representación de D3DRS VERTEXBLEND en un valor del tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e6c-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="f7e6c-121">En el ejemplo de código siguiente se muestra el aspecto que podría tener esta llamada al establecer el estado de representación de una mezcla entre dos matrices del mundo.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="f7e6c-122">Cuando D3DRS \_ VERTEXBLEND se establece en cualquier valor distinto de D3DVBF \_ disable, el sistema asume que el número adecuado de pesos de fusión se incluirá en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="f7e6c-123">Es su responsabilidad proporcionar un formato de vértice compatible y proporcionar una descripción adecuada de ese formato a los métodos de representación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="f7e6c-124">Cuando está habilitado, el sistema realiza la combinación de geometría para todos los objetos representados por los métodos de representación de DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="f7e6c-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7e6c-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7e6c-125">See Also</span></span>

[<span data-ttu-id="f7e6c-126">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7e6c-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="f7e6c-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7e6c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7e6c-128">Combinación de geometría</span><span class="sxs-lookup"><span data-stu-id="f7e6c-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 

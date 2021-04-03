---
description: La niebla de píxeles obtiene su nombre del hecho de que se calcula por píxel en el controlador de dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Niebla de píxeles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906325"
---
# <a name="pixel-fog-direct3d-9"></a><span data-ttu-id="39673-103">Niebla de píxeles (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="39673-103">Pixel Fog (Direct3D 9)</span></span>

<span data-ttu-id="39673-104">La niebla de píxeles obtiene su nombre del hecho de que se calcula por píxel en el controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39673-104">Pixel fog gets its name from the fact that it is calculated on a per-pixel basis in the device driver.</span></span> <span data-ttu-id="39673-105">Esto es diferente del niebla de vértices, que es calculado por la canalización durante los cálculos de transformación e iluminación.</span><span class="sxs-lookup"><span data-stu-id="39673-105">This is different from vertex fog, which is computed by the pipeline during transformation and lighting calculations.</span></span> <span data-ttu-id="39673-106">La niebla de píxeles a veces se denomina niebla de tabla porque algunos controladores usan una tabla de búsqueda precalculada para determinar el factor de niebla, usando la profundidad de cada píxel que se va a aplicar a los cálculos de mezcla.</span><span class="sxs-lookup"><span data-stu-id="39673-106">Pixel fog is sometimes called table fog because some drivers use a precalculated lookup table to determine the fog factor, using the depth of each pixel to apply in blending computations.</span></span> <span data-ttu-id="39673-107">Se puede aplicar mediante cualquier fórmula de niebla identificada por los miembros del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="39673-107">It can be applied using any fog formula identified by members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="39673-108">Las implementaciones de estas fórmulas son específicas del controlador.</span><span class="sxs-lookup"><span data-stu-id="39673-108">The implementations of these formulas are driver-specific.</span></span> <span data-ttu-id="39673-109">Si un controlador no es compatible con una fórmula de niebla compleja, se debe degradar a una fórmula menos compleja.</span><span class="sxs-lookup"><span data-stu-id="39673-109">If a driver doesn't support a complex fog formula, it should degrade to a less complex formula.</span></span>

## <a name="eye-relative-vs-z-based-depth"></a><span data-ttu-id="39673-110">Profundidad basada en Eye-Relative frente a Z</span><span class="sxs-lookup"><span data-stu-id="39673-110">Eye-Relative vs. Z-Based Depth</span></span>

<span data-ttu-id="39673-111">Para aliviar los artefactos gráficos relacionados con la niebla causados por la distribución desigual de los valores z en un búfer de profundidad, la mayoría de los dispositivos de hardware usan la profundidad relativa a la vista en lugar de los valores de profundidad basados en z para la niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39673-111">To alleviate fog-related graphic artifacts caused by uneven distribution of z-values in a depth buffer, most hardware devices use eye-relative depth instead of z-based depth values for pixel fog.</span></span> <span data-ttu-id="39673-112">La profundidad relativa a la vista es esencialmente el elemento w de un conjunto de coordenadas homogéneo.</span><span class="sxs-lookup"><span data-stu-id="39673-112">Eye-relative depth is essentially the w element from a homogeneous coordinate set.</span></span> <span data-ttu-id="39673-113">Microsoft Direct3D toma el recíproco del elemento RHW de un conjunto de coordenadas de espacio de dispositivo para reproducir true.</span><span class="sxs-lookup"><span data-stu-id="39673-113">Microsoft Direct3D takes the reciprocal of the RHW element from a device space coordinate set to reproduce true w.</span></span> <span data-ttu-id="39673-114">Si un dispositivo admite la niebla relativa a la vista, establece la marca **D3DPRASTERCAPS \_ WFOG** en el miembro RasterCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) cuando se llama al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="39673-114">If a device supports eye-relative fog, it sets the **D3DPRASTERCAPS\_WFOG** flag in the RasterCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="39673-115">A excepción del rasterizador de referencia, los dispositivos de software siempre utilizan z para calcular los efectos de niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="39673-115">With the exception of the reference rasterizer, software devices always use z to calculate pixel fog effects.</span></span>

<span data-ttu-id="39673-116">Cuando se admite la niebla relativa a la vista, el sistema utiliza automáticamente la profundidad relativa a la vista en lugar de la profundidad basada en z si la matriz de proyección proporcionada genera valores z en el espacio universal que son equivalentes a los valores w en el espacio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39673-116">When eye-relative fog is supported, the system automatically uses eye-relative depth rather than z-based depth if the provided projection matrix produces z-values in world space that are equivalent to w-values in device space.</span></span> <span data-ttu-id="39673-117">La matriz de proyección se establece llamando al método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) , utilizando el \_ valor de proyección D3DTS y pasando una estructura [**D3DMATRIX**](d3dmatrix.md) que representa la matriz deseada.</span><span class="sxs-lookup"><span data-stu-id="39673-117">You set the projection matrix by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method, using the D3DTS\_PROJECTION value and passing a [**D3DMATRIX**](d3dmatrix.md) structure that represents the desired matrix.</span></span> <span data-ttu-id="39673-118">Si la matriz de proyección no es compatible con este requisito, los efectos de niebla no se aplican correctamente.</span><span class="sxs-lookup"><span data-stu-id="39673-118">If the projection matrix isn't compliant with this requirement, fog effects are not applied properly.</span></span> <span data-ttu-id="39673-119">Para obtener más información sobre cómo generar una matriz compatible, vea [transformación de proyección (Direct3D 9)](projection-transform.md).</span><span class="sxs-lookup"><span data-stu-id="39673-119">For details about producing a compliant matrix, see [Projection Transform (Direct3D 9)](projection-transform.md).</span></span>

<span data-ttu-id="39673-120">Direct3D usa la matriz de proyección establecida actualmente en los cálculos de profundidad basados en w.</span><span class="sxs-lookup"><span data-stu-id="39673-120">Direct3D uses the currently set projection matrix in its w-based depth calculations.</span></span> <span data-ttu-id="39673-121">Como resultado, una aplicación debe establecer una matriz de proyección compatible para recibir las características basadas en w deseadas, incluso si no usa la canalización de transformación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="39673-121">As a result, an application must set a compliant projection matrix to receive the desired w-based features, even if it does not use the Direct3D transformation pipeline.</span></span>

<span data-ttu-id="39673-122">Direct3D comprueba la cuarta columna de la matriz de proyección.</span><span class="sxs-lookup"><span data-stu-id="39673-122">Direct3D checks the fourth column of the projection matrix.</span></span> <span data-ttu-id="39673-123">Si los coeficientes son \[ 0, 0, 0, 1 \] (para una proyección afín), el sistema usará valores de profundidad basados en z para la niebla.</span><span class="sxs-lookup"><span data-stu-id="39673-123">If the coefficients are \[0,0,0,1\] (for an affine projection) the system will use z-based depth values for fog.</span></span> <span data-ttu-id="39673-124">En este caso, también debe especificar las distancias de inicio y finalización de los efectos de niebla lineal en el espacio del dispositivo, que va desde 0,0 en el punto más cercano al usuario y 1,0 en el punto más lejano.</span><span class="sxs-lookup"><span data-stu-id="39673-124">In this case, you must also specify the start and end distances for linear fog effects in device space, which ranges from 0.0 at the nearest point to the user, and 1.0 at the farthest point.</span></span>

## <a name="using-pixel-fog"></a><span data-ttu-id="39673-125">Usar la niebla de píxeles</span><span class="sxs-lookup"><span data-stu-id="39673-125">Using Pixel Fog</span></span>

<span data-ttu-id="39673-126">Siga los pasos que se indican a continuación para habilitar la niebla de píxeles en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39673-126">Use the following steps to enable pixel fog in your application.</span></span>

1.  <span data-ttu-id="39673-127">Habilite la combinación de niebla mediante el establecimiento del estado de representación de FOGENABLE de D3DRS \_ en **true**.</span><span class="sxs-lookup"><span data-stu-id="39673-127">Enable fog blending by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span>
2.  <span data-ttu-id="39673-128">Establezca el color de niebla deseado en el \_ Estado de representación de D3DRS FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="39673-128">Set the desired fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="39673-129">Elija la fórmula de niebla que se va a usar estableciendo el \_ Estado de representación de D3DRS FOGTABLEMODE en el miembro correspondiente del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="39673-129">Choose the fog formula to use by setting the D3DRS\_FOGTABLEMODE render state to the corresponding member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="39673-130">Establezca los parámetros de niebla como desee para el modo de niebla seleccionado en los Estados de representación asociados.</span><span class="sxs-lookup"><span data-stu-id="39673-130">Set the fog parameters as desired for the selected fog mode in the associated render states.</span></span> <span data-ttu-id="39673-131">Esto incluye las distancias de inicio y finalización para la niebla lineal y la densidad de niebla para el modo de niebla exponencial.</span><span class="sxs-lookup"><span data-stu-id="39673-131">This includes the start and end distances for linear fog, and fog density for exponential fog mode.</span></span>

<span data-ttu-id="39673-132">En el ejemplo siguiente se muestra el aspecto de estos pasos en el código.</span><span class="sxs-lookup"><span data-stu-id="39673-132">The following example shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



<span data-ttu-id="39673-133">Algunos parámetros de niebla son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="39673-133">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts only DWORD values in the second parameter.</span></span> <span data-ttu-id="39673-134">En el ejemplo anterior se proporcionan los valores de punto flotante a **IDirect3DDevice9:: SetRenderState** sin conversión de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y, a continuación, desreferenciarlas.</span><span class="sxs-lookup"><span data-stu-id="39673-134">The preceding example provides the floating-point values to **IDirect3DDevice9::SetRenderState** without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39673-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="39673-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39673-136">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="39673-136">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 

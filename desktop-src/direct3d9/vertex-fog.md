---
description: Cuando el sistema realiza la luneta térmica de los vértices, aplica los cálculos de niebla en cada vértice de un polígono y, a continuación, interpola los resultados a lo largo de la superficie del polígono durante la rasterización.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Niebla de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151941"
---
# <a name="vertex-fog-direct3d-9"></a><span data-ttu-id="8cdce-103">Niebla de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8cdce-103">Vertex Fog (Direct3D 9)</span></span>

<span data-ttu-id="8cdce-104">Cuando el sistema realiza la luneta térmica de los vértices, aplica los cálculos de niebla en cada vértice de un polígono y, a continuación, interpola los resultados a lo largo de la superficie del polígono durante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="8cdce-104">When the system performs vertex fogging, it applies fog calculations at each vertex in a polygon, and then interpolates the results across the face of the polygon during rasterization.</span></span> <span data-ttu-id="8cdce-105">Los efectos de la niebla de vértice se calculan mediante el motor de luz y transformación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8cdce-105">Vertex fog effects are computed by the Direct3D lighting and transformation engine.</span></span> <span data-ttu-id="8cdce-106">Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8cdce-106">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="8cdce-107">Si la aplicación no usa Direct3D para la transformación y la iluminación, la aplicación debe realizar cálculos de niebla.</span><span class="sxs-lookup"><span data-stu-id="8cdce-107">If your application does not use Direct3D for transformation and lighting, the application must perform fog calculations.</span></span> <span data-ttu-id="8cdce-108">En este caso, coloque el factor de niebla que se calcula en el componente alfa del color especular para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="8cdce-108">In this case, place the fog factor that is computed in the alpha component of the specular color for each vertex.</span></span> <span data-ttu-id="8cdce-109">Puede usar las fórmulas que desee: basadas en intervalos, volumétricas o de otro modo.</span><span class="sxs-lookup"><span data-stu-id="8cdce-109">You are free to use whatever formulas you want - range-based, volumetric, or otherwise.</span></span> <span data-ttu-id="8cdce-110">Direct3D usa el factor de niebla proporcionado para interpolar en la superficie de cada polígono.</span><span class="sxs-lookup"><span data-stu-id="8cdce-110">Direct3D uses the supplied fog factor to interpolate across the face of each polygon.</span></span> <span data-ttu-id="8cdce-111">Las aplicaciones que realizan su propia transformación e iluminación también deben realizar sus propios cálculos de niebla de vértices.</span><span class="sxs-lookup"><span data-stu-id="8cdce-111">Applications that perform their own transformation and lighting must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="8cdce-112">Como resultado, este tipo de aplicación solo necesita habilitar la combinación de niebla y establecer el color de la niebla a través de los Estados de representación asociados, como se describe en el [apartado de combinación de niebla (Direct3D 9)](fog-blending.md) y en el [color de niebla (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="8cdce-112">As a result, such an application need only enable fog blending and set the fog color through the associated render states, as described in [Fog Blending (Direct3D 9)](fog-blending.md) and [Fog Color (Direct3D 9)](fog-color.md).</span></span>

> [!Note]  
> <span data-ttu-id="8cdce-113">Cuando se usa un sombreador de vértices, debe usar la niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="8cdce-113">When using a vertex shader, you must use vertex fog.</span></span> <span data-ttu-id="8cdce-114">Esto se logra mediante el sombreador de vértices para escribir la intensidad de la niebla por vértices en el registro oFog.</span><span class="sxs-lookup"><span data-stu-id="8cdce-114">This is accomplished by using the vertex shader to write the per-vertex fog intensity to the oFog register.</span></span> <span data-ttu-id="8cdce-115">Una vez completado el sombreador de píxeles, los datos de oFog se usan para interpolar linealmente con el color de niebla.</span><span class="sxs-lookup"><span data-stu-id="8cdce-115">After the pixel shader completes, the oFog data is used to linearly interpolate with the fog color.</span></span> <span data-ttu-id="8cdce-116">Esta intensidad no está disponible en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="8cdce-116">This intensity is not available in a pixel shader.</span></span>

 

## <a name="range-based-fog"></a><span data-ttu-id="8cdce-117">Niebla de Range-Based</span><span class="sxs-lookup"><span data-stu-id="8cdce-117">Range-Based Fog</span></span>

> [!Note]  
> <span data-ttu-id="8cdce-118">Direct3D usa cálculos de niebla basados en intervalos solo cuando se usa la niebla de vértices con el motor de transformación y iluminación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8cdce-118">Direct3D uses range-based fog calculations only when using vertex fog with the Direct3D transformation and lighting engine.</span></span> <span data-ttu-id="8cdce-119">Esto se debe a que la niebla de píxeles se implementa en el controlador de dispositivo y no existe ningún hardware actualmente para admitir la niebla basada en intervalos por píxel.</span><span class="sxs-lookup"><span data-stu-id="8cdce-119">This is because pixel fog is implemented in the device driver, and no hardware currently exists to support per-pixel range-based fog.</span></span> <span data-ttu-id="8cdce-120">Si la aplicación realiza su propia transformación e iluminación, debe realizar sus propios cálculos de niebla, basados en intervalos o en cualquier otro caso.</span><span class="sxs-lookup"><span data-stu-id="8cdce-120">If your application performs its own transformation and lighting, it must perform its own fog calculations, range-based or otherwise.</span></span>

 

<span data-ttu-id="8cdce-121">A veces, el uso de niebla puede introducir artefactos gráficos que hacen que los objetos se mezclen con el color de niebla de maneras no intuitivas.</span><span class="sxs-lookup"><span data-stu-id="8cdce-121">Sometimes, using fog can introduce graphic artifacts that cause objects to be blended with the fog color in nonintuitive ways.</span></span> <span data-ttu-id="8cdce-122">Por ejemplo, imagine una escena en la que hay dos objetos visibles: uno lo suficientemente lejano como para que se vea afectado por la niebla y el otro cerca de lo suficiente como para no verse afectado.</span><span class="sxs-lookup"><span data-stu-id="8cdce-122">For example, imagine a scene in which there are two visible objects: one distant enough to be affected by fog, and the other near enough to be unaffected.</span></span> <span data-ttu-id="8cdce-123">Si el área de visualización gira en su lugar, los efectos de niebla aparentes pueden cambiar, aunque los objetos sean estacionarios.</span><span class="sxs-lookup"><span data-stu-id="8cdce-123">If the viewing area rotates in place, the apparent fog effects can change, even if the objects are stationary.</span></span> <span data-ttu-id="8cdce-124">En el diagrama siguiente se muestra una vista de la parte superior de esta situación.</span><span class="sxs-lookup"><span data-stu-id="8cdce-124">The following diagram shows a top-down view of such a situation.</span></span>

![diagrama de dos puntos de vista y cómo afectan a la niebla para dos objetos](images/artifog.png)

<span data-ttu-id="8cdce-126">La niebla basada en intervalos es otra, más precisa, para determinar los efectos de niebla.</span><span class="sxs-lookup"><span data-stu-id="8cdce-126">Range-based fog is another, more accurate, way to determine the fog effects.</span></span> <span data-ttu-id="8cdce-127">En la niebla basada en intervalo, Direct3D usa la distancia real desde el punto de vista a un vértice para los cálculos de niebla.</span><span class="sxs-lookup"><span data-stu-id="8cdce-127">In range-based fog, Direct3D uses the actual distance from the viewpoint to a vertex for its fog calculations.</span></span> <span data-ttu-id="8cdce-128">Direct3D aumenta el efecto de la niebla a medida que aumenta la distancia entre los dos puntos, en lugar de la profundidad del vértice dentro de la escena, con lo que se evitan los artefactos de rotación.</span><span class="sxs-lookup"><span data-stu-id="8cdce-128">Direct3D increases the effect of fog as the distance between the two points increases, rather than the depth of the vertex within in the scene, thereby avoiding rotational artifacts.</span></span>

<span data-ttu-id="8cdce-129">Si el dispositivo actual admite la niebla basada en intervalos, establecerá el \_ valor de FOGRANGE de D3DPRASTERCAPS en el miembro RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) al llamar al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) .</span><span class="sxs-lookup"><span data-stu-id="8cdce-129">If the current device supports range-based fog, it will set the D3DPRASTERCAPS\_FOGRANGE value in the RasterCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) when you call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method.</span></span> <span data-ttu-id="8cdce-130">Para habilitar la niebla basada en intervalos, establezca el \_ Estado de representación de D3DRS RANGEFOGENABLE en **true**.</span><span class="sxs-lookup"><span data-stu-id="8cdce-130">To enable range-based fog, set the D3DRS\_RANGEFOGENABLE render state to **TRUE**.</span></span>

<span data-ttu-id="8cdce-131">Direct3D calcula la niebla basada en intervalo durante la transformación y la iluminación.</span><span class="sxs-lookup"><span data-stu-id="8cdce-131">Range-based fog is computed by Direct3D during transformation and lighting.</span></span> <span data-ttu-id="8cdce-132">Las aplicaciones que no usan el motor de transformación y iluminación de Direct3D también deben realizar sus propios cálculos de niebla de vértices.</span><span class="sxs-lookup"><span data-stu-id="8cdce-132">Applications that don't use the Direct3D transformation and lighting engine must also perform their own vertex fog calculations.</span></span> <span data-ttu-id="8cdce-133">En este caso, proporcione el factor de niebla basado en el intervalo en el componente alfa del componente especular para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="8cdce-133">In this case, provide the range-based fog factor in the alpha component of the specular component for each vertex.</span></span>

## <a name="using-vertex-fog"></a><span data-ttu-id="8cdce-134">Usar la niebla de vértice</span><span class="sxs-lookup"><span data-stu-id="8cdce-134">Using Vertex Fog</span></span>

<span data-ttu-id="8cdce-135">Siga los pasos que se indican a continuación para habilitar la niebla de vértices en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cdce-135">Use the following steps to enable vertex fog in your application.</span></span>

1.  <span data-ttu-id="8cdce-136">Habilite la combinación de niebla estableciendo D3DRS \_ FOGENABLE en **true**.</span><span class="sxs-lookup"><span data-stu-id="8cdce-136">Enable fog blending by setting D3DRS\_FOGENABLE to **TRUE**.</span></span>
2.  <span data-ttu-id="8cdce-137">Establezca el color de niebla en el \_ Estado de representación de FOGCOLOR de D3DRS.</span><span class="sxs-lookup"><span data-stu-id="8cdce-137">Set the fog color in the D3DRS\_FOGCOLOR render state.</span></span>
3.  <span data-ttu-id="8cdce-138">Elija la fórmula de niebla deseada estableciendo el estado de representación de D3DRS \_ FOGVERTEXMODE en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdce-138">Choose the desired fog formula by setting the D3DRS\_FOGVERTEXMODE render state to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span>
4.  <span data-ttu-id="8cdce-139">Establezca los parámetros de niebla como desee para la fórmula de niebla seleccionada en los Estados de representación.</span><span class="sxs-lookup"><span data-stu-id="8cdce-139">Set the fog parameters as desired for the selected fog formula in the render states.</span></span>

<span data-ttu-id="8cdce-140">En el ejemplo siguiente, escrito en C++, se muestra el aspecto que podrían tener estos pasos en el código.</span><span class="sxs-lookup"><span data-stu-id="8cdce-140">The following example, written in C++, shows what these steps might look like in code.</span></span>


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



<span data-ttu-id="8cdce-141">Algunos parámetros de niebla son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="8cdce-141">Some fog parameters are required as floating-point values, even though the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method only accepts DWORD values in the second parameter.</span></span> <span data-ttu-id="8cdce-142">En este ejemplo se proporcionan correctamente los valores de punto flotante a estos métodos sin conversión de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y después desreferenciarlas.</span><span class="sxs-lookup"><span data-stu-id="8cdce-142">This example successfully provides the floating-point values to these methods without data translation by casting the addresses of the floating-point variables as DWORD pointers, and then dereferencing them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cdce-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cdce-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cdce-144">Tipos de niebla</span><span class="sxs-lookup"><span data-stu-id="8cdce-144">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 

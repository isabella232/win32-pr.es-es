---
description: Usar la asignación de rugosidad (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Usar la asignación de rugosidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495760"
---
# <a name="using-bump-mapping-direct3d-9"></a><span data-ttu-id="bd989-103">Usar la asignación de rugosidad (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bd989-103">Using Bump Mapping (Direct3D 9)</span></span>

## <a name="detecting-support-for-bump-mapping"></a><span data-ttu-id="bd989-104">Detección de la compatibilidad con la asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="bd989-104">Detecting Support for Bump Mapping</span></span>

<span data-ttu-id="bd989-105">Un dispositivo puede realizar la asignación de rugosidad si admite la \_ operación de fusión mediante combinación de texturas D3DTOP BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE.</span><span class="sxs-lookup"><span data-stu-id="bd989-105">A device can perform bump mapping if it supports either the D3DTOP\_BUMPENVMAP or D3DTOP\_BUMPENVMAPLUMINANCE texture blending operation.</span></span> <span data-ttu-id="bd989-106">Use [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ consulta \_ LEGACYBUMPMAP para ver si se admite un formato para la asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-106">Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_LEGACYBUMPMAP to see if a format is supported for bump mapping.</span></span>

<span data-ttu-id="bd989-107">Además, las aplicaciones deben comprobar las capacidades del dispositivo para asegurarse de que el dispositivo admite un número adecuado de fases de fusión, normalmente al menos tres, y expone al menos un formato de píxel de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-107">Additionally, applications should check the device capabilities to make sure the device supports an appropriate number of blending stages, usually at least three, and exposes at least one bump-mapping pixel format.</span></span>

<span data-ttu-id="bd989-108">En el siguiente ejemplo de código se comprueban las funcionalidades del dispositivo para detectar la compatibilidad con la asignación de rugosidad en el dispositivo actual, con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="bd989-108">The following code example checks device capabilities to detect support for bump mapping in the current device, using the given criteria.</span></span>


```
BOOL SupportsBumpMapping()
{
    D3DCAPS9 d3dCaps;

    d3dDevice->GetDeviceCaps( &d3dCaps );

    // Does this device support the two bump mapping blend operations?
    if ( 0 == d3dCaps.TextureOpCaps & ( D3DTEXOPCAPS_BUMPENVMAP |
                                            D3DTEXOPCAPS_BUMPENVMAPLUMINANCE ))
        return FALSE;

    // Does this device support up to three blending stages?
    if( d3dCaps.MaxTextureBlendStages < 3 )
        return FALSE;

    return TRUE;
}
```



## <a name="creating-a-bump-map-texture"></a><span data-ttu-id="bd989-109">Crear una textura de mapa de rugosidad</span><span class="sxs-lookup"><span data-stu-id="bd989-109">Creating a Bump Map Texture</span></span>

<span data-ttu-id="bd989-110">Cree una textura de mapa de rugosidad como cualquier otra textura.</span><span class="sxs-lookup"><span data-stu-id="bd989-110">You create a bump map texture like any other texture.</span></span> <span data-ttu-id="bd989-111">La aplicación comprueba la compatibilidad con la asignación de rugosidad y recupera un formato de píxel válido, como se describe en detección de la compatibilidad con la asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-111">Your application verifies support for bump mapping and retrieves a valid pixel format, as discussed in Detecting Support for Bump Mapping.</span></span>

<span data-ttu-id="bd989-112">Una vez creada la superficie, puede cargar cada píxel con los valores Delta adecuados y luminancia, si el formato de la superficie incluye luminancia.</span><span class="sxs-lookup"><span data-stu-id="bd989-112">After the surface is created, you can load each pixel with the appropriate delta values, and luminance, if the surface format includes luminance.</span></span> <span data-ttu-id="bd989-113">Los valores de cada componente de píxel se describen en [formatos de píxeles de mapa de rugosidad (Direct3D 9)](bump-map-pixel-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bd989-113">The values for each pixel component are described in [Bump Map Pixel Formats (Direct3D 9)](bump-map-pixel-formats.md).</span></span>

## <a name="configuring-bump-mapping-parameters"></a><span data-ttu-id="bd989-114">Configuración de parámetros de asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="bd989-114">Configuring Bump Mapping Parameters</span></span>

<span data-ttu-id="bd989-115">Cuando la aplicación haya creado un mapa de rugosidad y establecido el contenido de cada píxel, puede preparar la representación mediante la configuración de los parámetros de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-115">When your application has created a bump map and set the contents of each pixel, you can prepare for rendering by configuring bump mapping parameters.</span></span> <span data-ttu-id="bd989-116">Los parámetros de asignación de rugosidad incluyen el establecimiento de las texturas necesarias y sus operaciones de fusión, así como los controles de transformación y luminancia del propio mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-116">Bump mapping parameters include setting the required textures and their blending operations, as well as the transformation and luminance controls for the bump map itself.</span></span>

1.  <span data-ttu-id="bd989-117">Establezca el mapa de textura base si se usan, el mapa de rugosidad y las texturas del mapa de entorno en fases de fusión de texturas.</span><span class="sxs-lookup"><span data-stu-id="bd989-117">Set the base texture map if used, bump map, and environment map textures into texture blending stages.</span></span>
2.  <span data-ttu-id="bd989-118">Establezca las operaciones de combinación de color y alfa para cada fase de textura.</span><span class="sxs-lookup"><span data-stu-id="bd989-118">Set the color and alpha blending operations for each texture stage.</span></span>
3.  <span data-ttu-id="bd989-119">Establezca la matriz de transformación mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-119">Set the bump map transformation matrix.</span></span>
4.  <span data-ttu-id="bd989-120">Establezca la escala de luminancia y los valores de desplazamiento según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bd989-120">Set the luminance scale and offset values as needed.</span></span>

<span data-ttu-id="bd989-121">En el ejemplo de código siguiente se establecen tres texturas (el mapa de textura base, el mapa de rugosidad y un mapa de entorno especular) en las fases de mezcla de textura adecuadas.</span><span class="sxs-lookup"><span data-stu-id="bd989-121">The following code example sets three textures (the base texture map, the bump map, and a specular environment map) to the appropriate texture blending stages.</span></span>


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



<span data-ttu-id="bd989-122">Después de establecer las texturas en las fases de fusión, en el ejemplo de código siguiente se preparan las operaciones de combinación y los argumentos de cada fase.</span><span class="sxs-lookup"><span data-stu-id="bd989-122">After setting the textures to their blending stages, the following code example prepares the blending operations and arguments for each stage.</span></span>


```
// Set the color operations and arguments to prepare for
//   bump mapping.

// Stage 0: The base texture
d3dDevice->SetTextureStageState( 0, D3DTSS_COLOROP, D3DTOP_MODULATE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAOP, D3DTOP_SELECTARG1 );
d3dDevice->SetTextureStageState( 0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE ); 
d3dDevice->SetTextureStageState( 0, D3DTSS_TEXCOORDINDEX, 1 );

// Stage 1: The bump map - Use luminance for this example.
d3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_BUMPENVMAPLUMINANCE);
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );

// Stage 2: A specular environment map
d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX, 0 );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLOROP, D3DTOP_ADD );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG1, D3DTA_TEXTURE );
d3dDevice->SetTextureStageState( 2, D3DTSS_COLORARG2, D3DTA_CURRENT );
```



<span data-ttu-id="bd989-123">Cuando se establecen las operaciones y los argumentos de combinación, el ejemplo de código siguiente establece la matriz de asignación de rugosidad de 2x2 en la matriz de identidad mediante el establecimiento de D3DTSS \_ BUMPENVMAPMAT00 y los \_ miembros D3DTSS BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) en 1,0.</span><span class="sxs-lookup"><span data-stu-id="bd989-123">When the blending operations and arguments are set, the following code example sets the 2x2 bump mapping matrix to the identity matrix by setting the D3DTSS\_BUMPENVMAPMAT00 and the D3DTSS\_BUMPENVMAPMAT11 members of [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) to 1.0.</span></span> <span data-ttu-id="bd989-124">Si se establece la matriz en la identidad, el sistema usará los valores Delta del mapa de rugosidad sin modificar, pero esto no es un requisito.</span><span class="sxs-lookup"><span data-stu-id="bd989-124">Setting the matrix to the identity causes the system to use the delta values in the bump map unmodified, but this is not a requirement.</span></span>


```
// Set the bump mapping matrix.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT00, F2DW(1.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT01, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT10, F2DW(0.0f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVMAT11, F2DW(1.0f) );
```



<span data-ttu-id="bd989-125">Si establece la operación de asignación de rugosidad para incluir la luminancia (D3DTOP \_ BUMPENVMAPLUMINANCE), debe establecer los controles de luminancia.</span><span class="sxs-lookup"><span data-stu-id="bd989-125">If you set the bump mapping operation to include luminance (D3DTOP\_BUMPENVMAPLUMINANCE), you must set the luminance controls.</span></span> <span data-ttu-id="bd989-126">Los controles de luminancia configuran cómo calcula la luminancia el sistema antes de modulating el color de la textura en la siguiente fase.</span><span class="sxs-lookup"><span data-stu-id="bd989-126">The luminance controls configure how the system computes luminance before modulating the color from the texture in the next stage.</span></span> <span data-ttu-id="bd989-127">Para obtener más información, vea [fórmulas de asignación de rugosidad (Direct3D 9)](bump-mapping-formulas.md).</span><span class="sxs-lookup"><span data-stu-id="bd989-127">For details, see [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md).</span></span>


```
// Set luminance controls. This is only needed when using
// a bump map that contains luminance, and when the 
// D3DTOP_BUMPENVMAPLUMINANCE texture blending operation is
// being used.
//
// Note  These calls rely on the following inline shortcut function:
//   inline DWORD F2DW( FLOAT f ) { return *((DWORD*)&f); }
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLSCALE, F2DW(0.5f) );
d3dDevice->SetTextureStageState( 1, D3DTSS_BUMPENVLOFFSET, F2DW(0.0f) );
```



<span data-ttu-id="bd989-128">Una vez que la aplicación configura parámetros de asignación de rugosidad, puede representarse como normal y los polígonos representados reciben efectos de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="bd989-128">After your application configures bump mapping parameters, it can render as normal, and the rendered polygons receive bump mapping effects.</span></span>

<span data-ttu-id="bd989-129">Tenga en cuenta que en el ejemplo anterior se muestran los parámetros establecidos para la asignación del entorno especular.</span><span class="sxs-lookup"><span data-stu-id="bd989-129">Note that the preceding example shows parameters set for specular environment mapping.</span></span> <span data-ttu-id="bd989-130">Al realizar la asignación de luz difusa, las aplicaciones establecen la operación de combinación de texturas de la última fase en D3DTOP \_ modular.</span><span class="sxs-lookup"><span data-stu-id="bd989-130">When performing diffuse light mapping, applications set the texture blending operation for the last stage to D3DTOP\_MODULATE.</span></span> <span data-ttu-id="bd989-131">Para obtener más información, vea [mapas ligeros difusos (Direct3D 9)](diffuse-light-maps.md).</span><span class="sxs-lookup"><span data-stu-id="bd989-131">For more information, see [Diffuse Light Maps (Direct3D 9)](diffuse-light-maps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd989-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd989-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd989-133">Asignación de rugosidad</span><span class="sxs-lookup"><span data-stu-id="bd989-133">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 

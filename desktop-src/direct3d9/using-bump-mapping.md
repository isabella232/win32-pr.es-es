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
# <a name="using-bump-mapping-direct3d-9"></a>Usar la asignación de rugosidad (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Detección de la compatibilidad con la asignación de rugosidad

Un dispositivo puede realizar la asignación de rugosidad si admite la \_ operación de fusión mediante combinación de texturas D3DTOP BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE. Use [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ consulta \_ LEGACYBUMPMAP para ver si se admite un formato para la asignación de rugosidad.

Además, las aplicaciones deben comprobar las capacidades del dispositivo para asegurarse de que el dispositivo admite un número adecuado de fases de fusión, normalmente al menos tres, y expone al menos un formato de píxel de asignación de rugosidad.

En el siguiente ejemplo de código se comprueban las funcionalidades del dispositivo para detectar la compatibilidad con la asignación de rugosidad en el dispositivo actual, con los criterios especificados.


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



## <a name="creating-a-bump-map-texture"></a>Crear una textura de mapa de rugosidad

Cree una textura de mapa de rugosidad como cualquier otra textura. La aplicación comprueba la compatibilidad con la asignación de rugosidad y recupera un formato de píxel válido, como se describe en detección de la compatibilidad con la asignación de rugosidad.

Una vez creada la superficie, puede cargar cada píxel con los valores Delta adecuados y luminancia, si el formato de la superficie incluye luminancia. Los valores de cada componente de píxel se describen en [formatos de píxeles de mapa de rugosidad (Direct3D 9)](bump-map-pixel-formats.md).

## <a name="configuring-bump-mapping-parameters"></a>Configuración de parámetros de asignación de rugosidad

Cuando la aplicación haya creado un mapa de rugosidad y establecido el contenido de cada píxel, puede preparar la representación mediante la configuración de los parámetros de asignación de rugosidad. Los parámetros de asignación de rugosidad incluyen el establecimiento de las texturas necesarias y sus operaciones de fusión, así como los controles de transformación y luminancia del propio mapa de rugosidad.

1.  Establezca el mapa de textura base si se usan, el mapa de rugosidad y las texturas del mapa de entorno en fases de fusión de texturas.
2.  Establezca las operaciones de combinación de color y alfa para cada fase de textura.
3.  Establezca la matriz de transformación mapa de rugosidad.
4.  Establezca la escala de luminancia y los valores de desplazamiento según sea necesario.

En el ejemplo de código siguiente se establecen tres texturas (el mapa de textura base, el mapa de rugosidad y un mapa de entorno especular) en las fases de mezcla de textura adecuadas.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Después de establecer las texturas en las fases de fusión, en el ejemplo de código siguiente se preparan las operaciones de combinación y los argumentos de cada fase.


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



Cuando se establecen las operaciones y los argumentos de combinación, el ejemplo de código siguiente establece la matriz de asignación de rugosidad de 2x2 en la matriz de identidad mediante el establecimiento de D3DTSS \_ BUMPENVMAPMAT00 y los \_ miembros D3DTSS BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) en 1,0. Si se establece la matriz en la identidad, el sistema usará los valores Delta del mapa de rugosidad sin modificar, pero esto no es un requisito.


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



Si establece la operación de asignación de rugosidad para incluir la luminancia (D3DTOP \_ BUMPENVMAPLUMINANCE), debe establecer los controles de luminancia. Los controles de luminancia configuran cómo calcula la luminancia el sistema antes de modulating el color de la textura en la siguiente fase. Para obtener más información, vea [fórmulas de asignación de rugosidad (Direct3D 9)](bump-mapping-formulas.md).


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



Una vez que la aplicación configura parámetros de asignación de rugosidad, puede representarse como normal y los polígonos representados reciben efectos de asignación de rugosidad.

Tenga en cuenta que en el ejemplo anterior se muestran los parámetros establecidos para la asignación del entorno especular. Al realizar la asignación de luz difusa, las aplicaciones establecen la operación de combinación de texturas de la última fase en D3DTOP \_ modular. Para obtener más información, vea [mapas ligeros difusos (Direct3D 9)](diffuse-light-maps.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de rugosidad](bump-mapping.md)
</dt> </dl>

 

 

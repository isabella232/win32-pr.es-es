---
description: Uso de la asignación de protuberancias (Direct3D 9)
ms.assetid: ded07764-1a11-42df-9a16-e4c3a328fb23
title: Uso de la asignación de protuberancias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4bc96f78ffb19dda04ff6b2bc3d0e46800b04b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473240"
---
# <a name="using-bump-mapping-direct3d-9"></a>Uso de la asignación de protuberancias (Direct3D 9)

## <a name="detecting-support-for-bump-mapping"></a>Detección de compatibilidad con la asignación de cambios

Un dispositivo puede realizar la asignación de protuberancias si admite la operación de mezcla de textura D3DTOP \_ BUMPENVMAP o D3DTOP \_ BUMPENVMAPLUMINANCE. Use [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE QUERY LEGACYBUMPMAP para ver si se admite un formato para la asignación \_ de \_ protuberancias.

Además, las aplicaciones deben comprobar las funcionalidades del dispositivo para asegurarse de que el dispositivo admite un número adecuado de fases de mezcla, normalmente al menos tres, y expone al menos un formato de píxeles de asignación de cambios.

En el ejemplo de código siguiente se comprueban las funcionalidades del dispositivo para detectar la compatibilidad con la asignación de cambios en el dispositivo actual, con los criterios especificados.


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



## <a name="creating-a-bump-map-texture"></a>Crear una textura de mapa de protuberancia

Se crea una textura de mapa de protuberancias como cualquier otra textura. La aplicación comprueba la compatibilidad con la asignación de protuberancias y recupera un formato de píxel válido, como se describe en Detección de compatibilidad con la asignación de cambios.

Una vez creada la superficie, puede cargar cada píxel con los valores delta adecuados y la luminosidad, si el formato de superficie incluye luminosidad. Los valores de cada componente de píxel se describen en Formatos de píxeles de mapa de protuberancia [(Direct3D 9).](bump-map-pixel-formats.md)

## <a name="configuring-bump-mapping-parameters"></a>Configuración de parámetros de asignación de protuberancias

Cuando la aplicación ha creado un mapa de protuberancias y ha establecido el contenido de cada píxel, puede prepararse para la representación mediante la configuración de parámetros de asignación de protuberancias. Los parámetros de asignación de cambios incluyen el establecimiento de las texturas necesarias y sus operaciones de combinación, así como los controles de transformación y luminosidad para el propio mapa de cambios.

1.  Establezca el mapa de textura base si se usa, el mapa de protuberancias y las texturas del mapa de entorno en fases de mezcla de texturas.
2.  Establezca las operaciones de combinación de color y alfa para cada fase de textura.
3.  Establezca la matriz de transformación del mapa de cambios.
4.  Establezca los valores de escala de luminosidad y desplazamiento según sea necesario.

En el ejemplo de código siguiente se establecen tres texturas (el mapa de textura base, el mapa de protuberancias y un mapa de entorno especular) en las fases de mezcla de textura adecuadas.


```
// Set the three textures.
d3dDevice->SetTexture( 0, d3dBaseTexture );
d3dDevice->SetTexture( 1, d3dBumpMap );
d3dDevice->SetTexture( 2, d3dEnvMap );
```



Después de establecer las texturas en sus fases de mezcla, el ejemplo de código siguiente prepara las operaciones de combinación y los argumentos para cada fase.


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



Cuando se establecen las operaciones de combinación y los argumentos, en el ejemplo de código siguiente se establece la matriz de asignación de cambios 2x2 en la matriz de identidad estableciendo D3DTSS \_ BUMPENVMAPMAT00 y los miembros D3DTSS \_ BUMPENVMAPMAT11 de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) en 1.0. Establecer la matriz en la identidad hace que el sistema use los valores delta en el mapa de incrementos sin modificar, pero esto no es un requisito.


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



Si establece la operación de asignación de protuberancias para incluir la luminosidad (D3DTOP \_ BUMPENVMAPLUMINANCE), debe establecer los controles de luminosidad. Los controles de luminosidad configuran cómo el sistema calcula la luminosidad antes de modular el color de la textura en la fase siguiente. Para obtener más información, vea Fórmulas de asignación [de protuberancias (Direct3D 9).](bump-mapping-formulas.md)


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



Una vez que la aplicación configura los parámetros de asignación de protuberancias, se puede representar de forma normal y los polígonos representados reciben efectos de asignación de protuberancias.

Tenga en cuenta que en el ejemplo anterior se muestran los parámetros establecidos para la asignación de entorno especular. Al realizar la asignación de luz difusa, las aplicaciones establecen la operación de mezcla de texturas de la última fase en D3DTOP \_ MODULARTE. Para obtener más información, vea [Difuso de Mapas (Direct3D 9).](diffuse-light-maps.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación de protuberancias](bump-mapping.md)
</dt> </dl>

 

 

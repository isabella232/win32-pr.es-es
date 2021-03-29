---
description: Los Estados de efecto se utilizan para inicializar los Estados de la canalización como preparación para el procesamiento de vértices y píxeles.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efectos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080004"
---
# <a name="effect-states-direct3d-9"></a>Estados de efectos (Direct3D 9)

Los Estados de efecto se utilizan para inicializar los Estados de la canalización como preparación para el procesamiento de vértices y píxeles.


```
effect state [ [index] ] = expression;
```



Donde:

-   Estado del efecto: similar a los Estados de canalización de funciones fijas tradicionales. A continuación se proporciona una lista completa de Estados.
-   \[\[ \] Índice \] de : Índice de entero opcional. El Índice identifica un estado determinado dentro de una matriz de Estados de efecto. Los corchetes externos indican que un índice es opcional. Si se usa un índice, asegúrese de usar los corchetes internos.
-   expresión de asignación de estado de expresión. Vea [expresiones (Direct3D 9)](expressions.md).

Cada Estado tiene un tipo de datos nativo. Este es el tipo de datos en el que el estado espera que los valores estén en cuando el efecto los asigna. A continuación se enumeran los tipos de datos que espera cada Estado.

Tenga en cuenta que la interfaz de efecto intentará convertir los valores al tipo adecuado lo antes posible. Los valores literales se pueden convertir en tiempo de compilación. Los no literales (es decir, las variables regulares) deben convertirse cuando se llama a los métodos de conjunto adecuados. Por ejemplo, la interfaz de efecto convertirá los valores establecidos mediante [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)y otras funciones similares, si es necesario. Para mejorar el rendimiento, asegúrese de que los valores que se pasan a la interfaz de efecto ya son del tipo correcto y no necesitan conversión. Si el tiempo de ejecución no puede convertir un valor, se devuelve un error.

Los Estados de efecto se pueden dividir en las siguientes categorías:

-   [Estados claros](#light-states)
-   [Estados de materiales](#material-states)
-   [Estados de representación](#render-states)
    -   [Estados de representación de canalización de píxeles](#pixel-pipe-render-states)
    -   [Estados de representación de canalización de vértices](#vertex-pipe-render-states)
-   [Estados de muestra](#sampler-states)
-   [Estados de la fase de muestra](#sampler-stage-states)
-   [Estados del sombreador](#shader-states)
-   [Estados de constantes del sombreador](#shader-constant-states)
-   [Estados de textura](#texture-states)
-   [Estados de la fase de textura](#texture-stage-states)
-   [Estados de transformación](#transform-states)

## <a name="light-states"></a>Estados claros

Para permitir el mejor rendimiento para aplicar un efecto, se deben especificar todos los componentes de una luz o un material en el archivo de efectos. Indica que no se puede declarar que se establece en un valor predeterminado porque no hay ninguna manera de que Direct3D establezca los Estados de luz individualmente.



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| Estado claro            | Tipo   | Valores                                                                                                              |
| LightAmbient \[ n\]      | float4 | Vea el miembro de ambiente de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | FLOAT  | Vea el miembro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation1 \[ n\] | FLOAT  | Vea el miembro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation2 \[ n\] | FLOAT  | Vea el miembro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightDiffuse \[ n\]      | float4 | Vea el miembro difuso de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightDirection \[ n\]    | float3 | Vea el miembro Direction de [**D3DLIGHT9**](d3dlight9.md).                                                         |
| LightEnable \[ n\]       | bool   | **True** o **false**. Vea el argumento bEnable en [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | FLOAT  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Vea el miembro de difuminación de [**D3DLIGHT9**](d3dlight9.md).                   |
| LightPhi \[ n\]          | FLOAT  | Vea el miembro de la PHI de [**D3DLIGHT9**](d3dlight9.md).                                                               |
| LightPosition \[ n\]     | float3 | Vea el miembro Position de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightRange \[ n\]        | FLOAT  | Vea el miembro de intervalo de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightSpecular \[ n\]     | float4 | Vea el miembro especular de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightTheta \[ n\]        | FLOAT  | Vea el miembro theta de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightType \[ n\]         | dword  | El mismo valor que la matriz de hasta n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sin el \_ prefijo D3DLIGHT. |



 

Ejemplo:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Esto habilitará la iluminación, hará la iluminación puntual del tipo, establecerá la posición de la luz en float3<10.0 f, 1,0 f, 23.0 f> y establecerá el color ambiente en FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f>.

## <a name="material-states"></a>Estados de materiales

Indica que no se puede declarar que se establece en un valor predeterminado porque no hay ninguna manera de que Direct3D establezca los Estados de material de forma individual.



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| Estado de materiales   | Tipo   | Valores                                         |
| MaterialAmbient  | float4 | Mismo valor que el [ **ambiente**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | El mismo valor que el [ **difuso**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Mismo valor que [ **emisor**](d3dmaterial9.md) |
| MaterialPower    | FLOAT  | El mismo valor que [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Mismo valor que [ **especular**](d3dmaterial9.md) |



 

Ejemplo:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Esto establecerá el color difuso en FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f> y tomar la eficacia del material 3.0 f.

## <a name="render-states"></a>Estados de representación

Hay dos tipos de Estados de representación:

-   [Estados de representación de canalización de píxeles](#pixel-pipe-render-states)
-   [Estados de representación de canalización de vértices](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Estados de representación de canalización de píxeles

Los Estados de representación del archivo de efectos tienen nombres similares a los Estados de canalización de funciones fijas, a menudo con el prefijo quitado.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Estado de representación</td>
<td>Tipo</td>
<td>Valores</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>Verdadero o Falso. Los mismos valores que D3DRS_ALPHABLENDENABLE en <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_. Vea D3DRS_ALPHAFUNC.</td>
</tr>
<tr class="even">
<td>AlphaRef</td>
<td>dword</td>
<td>Los mismos valores que D3DRS_ALPHAREF.</td>
</tr>
<tr class="odd">
<td>AlphaTestEnable</td>
<td>dword</td>
<td>Verdadero o Falso. Vea D3DRS_ALPHATESTENABLE.</td>
</tr>
<tr class="even">
<td>BlendOp</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sin el prefijo D3DBLENDOP_.</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>dword</td>
<td>Combinación bit a bit de rojo | VERDE | AZUL | Canal. Vea D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>FLOAT</td>
<td>Los mismos valores que D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sin el prefijo D3DBLEND_.</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>Verdadero o Falso. Los mismos valores que D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>FillMode</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sin el prefijo D3DFILL_.</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>dword</td>
<td>Verdadero o Falso. Vea D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>ShadeMode</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sin el prefijo D3DSHADE_.</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>FLOAT</td>
<td>Los mismos valores que D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sin el prefijo D3DBLEND_.</td>
</tr>
<tr class="even">
<td>StencilEnable</td>
<td>bool</td>
<td>Verdadero o Falso. Los mismos valores que D3DRS_STENCILENABLE.</td>
</tr>
<tr class="odd">
<td>StencilFail</td>
<td>dword</td>
<td>Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_. Vea D3DRS_STENCILFAIL.</td>
</tr>
<tr class="even">
<td>StencilFunc</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_. Vea D3DRS_STENCILFUNC.</td>
</tr>
<tr class="odd">
<td>StencilMask</td>
<td>dword</td>
<td>Los mismos valores que D3DRS_STENCILMASK.</td>
</tr>
<tr class="even">
<td>StencilPass</td>
<td>dword</td>
<td>Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_. Vea D3DRS_STENCILPASS.</td>
</tr>
<tr class="odd">
<td>StencilRef</td>
<td>int</td>
<td>Los mismos valores que D3DRS_STENCILREF.</td>
</tr>
<tr class="even">
<td>StencilWriteMask</td>
<td>dword</td>
<td>Los mismos valores que D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="odd">
<td>StencilZFail</td>
<td>dword</td>
<td>Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_. Vea D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="even">
<td>TextureFactor</td>
<td>dword</td>
<td>Los mismos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Los mismos valores que D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="odd">
<td>Wrap0 - Wrap15</td>
<td>dword</td>
<td>Los valores son los mismos que los utilizados por D3DRS_WRAP0. Los valores válidos son:
<ul>
<li>COORD0 (que corresponde a D3DWRAPCOORD_0)</li>
<li>COORD1 (que corresponde a D3DWRAPCOORD_1)</li>
<li>COORD2 (que corresponde a D3DWRAPCOORD_2)</li>
<li>COORD3 (que corresponde a D3DWRAPCOORD_3)</li>
<li>U (que corresponde a D3DWRAP_U)</li>
<li>V (que corresponde a D3DWRAP_V)</li>
<li>W (que corresponde a D3DWRAP_W)</li>
</ul></td>
</tr>
<tr class="even">
<td>ZEnable</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sin el prefijo D3DZB_.</td>
</tr>
<tr class="odd">
<td>ZFunc</td>
<td>dword</td>
<td>Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_. Vea D3DRS_ZFUNC.</td>
</tr>
<tr class="even">
<td>ZWriteEnable</td>
<td>bool</td>
<td>Verdadero o Falso. Vea D3DRS_ZWRITEENABLE.</td>
</tr>
</tbody>
</table>



 

Ejemplo:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Esto habilitará la combinación alfa y hará que todas las geometrías se representen en el alambre.

### <a name="vertex-pipe-render-states"></a>Estados de representación de canalización de vértices

Los Estados de representación del archivo de efectos tienen nombres similares a los Estados de canalización de funciones fijas, a menudo con el prefijo quitado.



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Estado de representación             | Tipo   | Valores                                                                                                                                        |
| Ambiente                  | float4 | Los mismos valores que D3DRS \_ ambiente.                                                                                                                |
| AmbientMaterialSource    | dword  | Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS. Vea D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Recorte                 | bool   | Verdadero o Falso. Los mismos valores que el \_ recorte D3DRS.                                                                                                |
| ClipPlaneEnable          | dword  | Combinación bit a bit de las macros D3DCLIPPLANE0-D3DCLIPPLANE5. Vea [**D3DCLIPPLANEn**](d3dclipplanen.md) y D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Los mismos valores que [**D3DCULL**](./d3dcull.md) sin el \_ prefijo D3DCULL.                                                                 |
| DiffuseMaterialSource    | dword  | Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS. Vea D3DRS \_ DIFFUSEMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS. Vea D3DRS \_ EMISSIVEMATERIALSOURCE. |
| FogColor                 | dword  | Los mismos valores que [**D3DCOLOR**](d3dcolor.md). Vea D3DRS \_ FOGCOLOR.                                                                             |
| FogDensity               | FLOAT  | Los mismos valores que D3DRS \_ FOGDENSITY.                                                                                                             |
| FogEnable                | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ FOGENABLE.                                                                                               |
| FogEnd                   | FLOAT  | Los mismos valores que D3DRS \_ FOGEND.                                                                                                                 |
| FogStart                 | FLOAT  | Los mismos valores que D3DRS \_ FOGSTART.                                                                                                               |
| FogTableMode             | dword  | Los mismos valores que [**D3DFOGMODE**](./d3dfogmode.md). Consulte D3DRS \_ FOGTABLEMODE en [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| FogVertexMode            | dword  | Los mismos valores que [**D3DFOGMODE**](./d3dfogmode.md) sin el \_ prefijo D3DFOG.                                                            |
| IndexedVertexBlendEnable | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Iluminación                 | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ Lighting.                                                                                                |
| LocalViewer              | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Los mismos valores que D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Los mismos valores que D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | FLOAT  | Los mismos valores que nSegments en [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Los mismos valores que D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | FLOAT  | Los mismos valores que D3DRS \_ .                                                                                                              |
| Puntuación \_ mínima           | FLOAT  | Los mismos valores que D3DRS se \_ puntuación \_ min.                                                                                                         |
| Puntuación \_ máxima           | FLOAT  | Los mismos valores que D3DRSan \_ \_ Max sin el \_ prefijo D3DRS.                                                                              |
| PointSpriteEnable        | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | dword  | Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS. Vea D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | FLOAT  | Los mismos valores que D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Los mismos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sin el \_ prefijo D3DVBF. Vea D3DRS \_ VERTEXBLEND.                  |



 

Ejemplo:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Esto hará que el color ambiente FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f>, establezca el modo de selección de la cara del aire en el sentido contrario a las agujas del reloj y establezca el color de niebla en rojo.

## <a name="sampler-states"></a>Estados de muestra

Un estado de muestra representa un objeto de muestra.



|         |         |                                     |
|---------|---------|-------------------------------------|
| State   | Tipo    | Valores                              |
| Muestra | muestras | **Null** o un bloque de estado de muestra. |



 

## <a name="sampler-stage-states"></a>Estados de la fase de muestra

Los Estados de la fase de muestra se utilizan para muestrear las texturas. El estado de muestra determina los tipos de filtrado y los modos de direccionamiento de textura.



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Estado de muestra       | Tipo                         | Valores                                                                                                                            |
| AddressU \[ 16\]      | dword                        | Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS. Vea D3DSAMP \_ ADDRESSU.      |
| AddressV \[ 16\]      | dword                        | Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS. Vea D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS. Vea D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Los mismos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el \_ prefijo D3DTEXF. Vea D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | dword                        | Los mismos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el \_ prefijo D3DTEXF. Vea D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | dword                        | Los mismos valores que D3DSAMP \_ MAXANISOTROPY sin el \_ prefijo D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | int                          | Los mismos valores que D3DSAMP \_ MAXMIPLEVEL sin el \_ prefijo D3DSAMP.                                                                 |
| MinFilter \[ 16\]     | dword                        | Los mismos valores que D3DSAMP \_ MINFILTER sin el \_ prefijo D3DSAMP.                                                                   |
| MipFilter \[ 16\]     | dword                        | Los mismos valores que D3DSAMP \_ MIPFILTER sin el \_ prefijo D3DSAMP.                                                                   |
| MipMapLodBias \[ 16\] | FLOAT                        | Los mismos valores que D3DSAMP \_ MIPMAPLODBIAS sin el \_ prefijo D3DSAMP.                                                               |
| SRGBTexture         | FLOAT                        | El mismo valor que D3DSAMP \_ SRGBTEXTURE sin el \_ prefijo D3DSAMP.                                                                  |



 

Ejemplo:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Esto fija los valores de UVW para que estén entre 0 y 1.

## <a name="shader-states"></a>Estados del sombreador

Solo hay dos Estados de sombreador de efectos: uno asociado a un objeto de sombreador de vértices y el otro asociado a un objeto de sombreador de píxeles.



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| Estado del sombreador | Tipo         | Valores                                                                      |
| U  | u  | **Null**, un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles. |
| VertexShader | vertexshader | **Null**, un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles. |



 

Ejemplo:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Esto compilará VSTexture, un sombreador de vértices definido anteriormente en el archivo. FX, en la versión 1,1 del sombreador de vértices y, a continuación, establecerá ese sombreador compilado como sombreador de vértices. El sombreador de píxeles se asigna a **null**.

## <a name="shader-constant-states"></a>Estados de constantes del sombreador

Los Estados de constantes del sombreador se usan para tener acceso a los parámetros constantes del sombreador.



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| Estado constante del sombreador | Tipo            | Valores                                       |
| PixelShaderConstant   | Float \[ m \[ n\]\] | m x n matriz de flotantes; m y n son opcionales. |
| PixelShaderConstant1  | float4          | Un valor de 4D float.                                |
| PixelShaderConstant2  | float4x2        | Dos floats de 4D.                               |
| PixelShaderConstant3  | float4x3        | Tres flotantes de 4D.                             |
| PixelShaderConstant4  | float4x4        | Cuatro flotantes de 4D.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | matriz de booleanos de m x n; m y n son opcionales.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | matriz de ints m x n. m y n son opcionales.   |
| PixelShaderConstantF  | Float \[ m \[ n\]\] | m x n matriz de flotantes. m y n son opcionales. |
| VertexShaderConstant  | Float \[ m \[ n\]\] | m x n matriz de flotantes. m y n son opcionales. |
| VertexShaderConstant1 | float4          | Un valor de 4D float.                                |
| VertexShaderConstant2 | float4x2        | Dos floats de 4D.                               |
| VertexShaderConstant3 | float4x3        | Tres flotantes de 4D.                             |
| VertexShaderConstant4 | float4x4        | Cuatro flotantes de 4D.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | matriz de booleanos de m x n. m y n son opcionales.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | matriz de ints m x n. m y n son opcionales.   |
| VertexShaderConstantF | Float \[ m \[ n\]\] | m x n matriz de flotantes. m y n son opcionales. |



 

## <a name="texture-states"></a>Estados de textura

Los Estados de textura inicializan las texturas utilizadas por el mezclador multitexture.



|               |         |                                   |
|---------------|---------|-----------------------------------|
| Estado de textura | Tipo    | Valores                            |
| Textura \[ 8\]  | textura | **Null** o un parámetro de textura. |



 

## <a name="texture-stage-states"></a>Estados de la fase de textura

Los Estados de la fase de textura establecen texturas y las fases de textura en el mezclador multitextura.



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Estado de la fase de textura        | Tipo  | Valores                                                                                                                                                    |
| AlphaOp \[ 8\]               | dword | Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el \_ prefijo D3DTOP. Vea D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el \_ prefijo D3DTOP. Vea D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVLSCALE sin el \_ prefijo D3DTSS TCI.                                                                                      |
| BumpEnvLOffset \[ 8\]        | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVLOFFSET sin el \_ prefijo D3DTSS TCI.                                                                                     |
| BumpEnvMat00 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA. Vea D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Los mismos valores que D3DTSS \_ TEXCOORDINDEX sin el \_ prefijo D3DTSS TCI.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Los mismos valores que los valores de [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sin el \_ prefijo D3DTTFF. Vea D3DTSS \_ TEXTURETRANSFORMFLAGS. |



 

## <a name="transform-states"></a>Estados de transformación

Establezca los Estados de transformación para inicializar las matrices de transformación. Los efectos usan matrices transpuestas para mejorar la eficacia. Puede proporcionar matrices transpuestas a un efecto o un efecto transformará automáticamente las matrices antes de utilizarlas.



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Estado de transformación       | Tipo     | Valores                                                                                                                          |
| ProjectionTransform   | float4x4 | Matriz 4x4 de flotantes. Los mismos valores que \_ la proyección D3DTS sin el \_ prefijo D3DTS.                                            |
| TextureTransform \[ 8\] | float4x4 | Matriz 4x4 de flotantes. Los mismos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sin el \_ prefijo D3DTS. |
| ViewTransform         | float4x4 | Matriz 4x4 de flotantes. Los mismos valores que D3DTS \_ vista sin el \_ prefijo D3DTS.                                                  |
| WorldTransform        | float4x4 | Matriz 4x4 de flotantes.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 

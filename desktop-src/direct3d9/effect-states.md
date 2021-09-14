---
description: Los estados de efecto se usan para inicializar los estados de canalización como preparación para el procesamiento de vértices y píxeles.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02cafd3bbd603716da99f5de613f06014a70f77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072761"
---
# <a name="effect-states-direct3d-9"></a>Estados de efecto (Direct3D 9)

Los estados de efecto se usan para inicializar los estados de canalización como preparación para el procesamiento de vértices y píxeles.


```
effect state [ [index] ] = expression;
```



Donde:

-   estado de efecto: similar a los estados tradicionales de canalización de función fija. A continuación se proporciona una lista completa de estados.
-   \[\[ \] index \] : índice entero opcional. El índice identifica un estado determinado dentro de una matriz de estados de efecto. Los corchetes externos indican que un índice es opcional. Si se usa un índice, asegúrese de usar los corchetes internos.
-   expression: expresión de asignación de estado. Vea [Expresiones (Direct3D 9).](expressions.md)

Cada estado tiene un tipo de datos nativo. Este es el tipo de datos en el que el estado espera que los valores tengan lugar cuando el efecto los asigne. A continuación se enumeran los tipos de datos que espera cada estado.

Tenga en cuenta que la interfaz de efecto intentará convertir los valores al tipo adecuado lo antes posible. Los valores literales se pueden convertir en tiempo de compilación. Los no literales (es decir, las variables normales) deben convertirse cuando se llama a los métodos Set adecuados. Por ejemplo, la interfaz de efecto convierte los valores establecidos mediante [**SetBool,**](id3dxbaseeffect--setbool.md) [**SetValue**](id3dxbaseeffect--setvalue.md)y otras funciones similares si es necesario. Para mejorar el rendimiento, asegúrese de que los valores pasados a la interfaz de efecto ya son el tipo correcto y no necesitarán conversión. Si el tiempo de ejecución no puede convertir un valor, se devuelve un error.

Los estados de efecto se pueden dividir en las siguientes categorías:

-   [Estados claros](#light-states)
-   [Estados de material](#material-states)
-   [Representar estados](#render-states)
    -   [Estados de representación de la canalización de píxeles](#pixel-pipe-render-states)
    -   [Estados de representación de la canalización de vértices](#vertex-pipe-render-states)
-   [Estados del muestreador](#sampler-states)
-   [Estados de la fase del muestreador](#sampler-stage-states)
-   [Estados del sombreador](#shader-states)
-   [Estados constantes del sombreador](#shader-constant-states)
-   [Estados de textura](#texture-states)
-   [Estados de la fase de textura](#texture-stage-states)
-   [Transformar estados](#transform-states)

## <a name="light-states"></a>Estados claros

Para habilitar el mejor rendimiento para aplicar un efecto, se deben especificar todos los componentes de una luz o un material en el archivo de efecto. Los estados que no se pueden declarar se establecen en algún valor predeterminado porque no hay ninguna manera de que Direct3D establezca estados claros individualmente.



| Estado de luz            | Tipo   | Valores                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| LightAmbient \[ n\]      | float4 | Consulte el miembro Ambient de [**D3DLIGHT9.**](d3dlight9.md)                                                           |
| LightAttenuation0 \[ n\] | FLOAT  | Vea el miembro Desatenciones0 [**de D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightAttenuation1 \[ n\] | FLOAT  | Vea el miembro Atenuación1 de [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightAttenuation2 \[ n\] | FLOAT  | Vea el miembro Desatenciones2 de [**D3DLIGHT9.**](d3dlight9.md)                                                      |
| LightDiffuse \[ n\]      | float4 | Vea el miembro Difuso [**de D3DLIGHT9.**](d3dlight9.md)                                                           |
| LightDirection \[ n\]    | float3 | Vea el miembro Direction de [**D3DLIGHT9.**](d3dlight9.md)                                                         |
| LightEnable \[ n\]       | bool   | **TRUE** o **FALSE**. Vea el argumento bEnable en [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | FLOAT  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Vea el miembro Falloff de [**D3DLIGHT9.**](d3dlight9.md)                   |
| LightLf \[ n\]          | FLOAT  | Consulte el miembro de Phi [**de D3DLIGHT9.**](d3dlight9.md)                                                               |
| LightPosition \[ n\]     | float3 | Vea el miembro Position de [**D3DLIGHT9.**](d3dlight9.md)                                                          |
| LightRange \[ n\]        | FLOAT  | Vea el miembro Range de [**D3DLIGHT9.**](d3dlight9.md)                                                             |
| LightSpecular \[ n\]     | float4 | Vea el miembro especular de [**D3DLIGHT9.**](d3dlight9.md)                                                          |
| LightTheta \[ n\]        | FLOAT  | Vea el miembro Theta de [**D3DLIGHT9.**](d3dlight9.md)                                                             |
| LightType \[ n\]         | dword  | El mismo valor que la matriz de hasta n [**valores D3DLIGHTTYPE**](./d3dlighttype.md) sin el prefijo D3DLIGHT. \_ |



 

Ejemplo:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Esto habilitará la iluminación, hará que la iluminación de punto sea el tipo, establecerá la posición de la luz en float3<10.0f, 1.0f, 23.0f> y establecerá el color ambiente en float4<0.7f, 0.0f, 0.0f, 1.0f>.

## <a name="material-states"></a>Estados de material

Los estados que no se pueden declarar se establecen en algún valor predeterminado porque no hay ninguna manera de que Direct3D establezca los estados de material individualmente.



| Estado del material   | Tipo   | Valores                                         |
|------------------|--------|------------------------------------------------|
| MaterialAmbient  | float4 | El mismo valor que [ **Ambient**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Mismo valor que [ **Difuso**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Mismo valor [ **que Emissive**](d3dmaterial9.md) |
| MaterialPower    | FLOAT  | El mismo valor que [ **Power**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | El mismo valor que [ **Specular**](d3dmaterial9.md) |



 

Ejemplo:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Esto establecerá el color difuso en float4<0.7f, 0.0f, 0.0f, 1.0f> y hará que la potencia del material sea 3.0f.

## <a name="render-states"></a>Representar estados

Hay dos tipos de estados de representación:

-   [Estados de representación de la canalización de píxeles](#pixel-pipe-render-states)
-   [Estados de representación de la canalización de vértices](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Estados de representación de la canalización de píxeles

Los estados de representación del archivo de efecto tienen nombres similares a los estados de canalización de función fija, a menudo con el prefijo quitado.




| | | Representación del estado | Tipo | Valores | | AlphaBlendEnable | bool | True o False. Los mismos valores que D3DRS_ALPHABLENDENABLE <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>en D3DRENDERSTATETYPE</strong></a>. | | AlphaFunc | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>que D3DCMPFUNC</strong></a> sin el D3DCMP_ predeterminado. Consulte D3DRS_ALPHAFUNC. | | AlphaRef | dword | Los mismos valores que D3DRS_ALPHAREF. | | AlphaTestEnable | dword | True o False. Consulte D3DRS_ALPHATESTENABLE. | | BlendOp | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dblendop"><strong>que D3DBLENDOP</strong></a> sin el D3DBLENDOP_ predeterminado. | | ColorWriteEnable | dword | Combinación bit a bit de RED| VERDE| BLUE| ALFA. Consulte D3DRS_COLORWRITEENABLE. | | DepthBias | float | Los mismos valores que D3DRS_DEPTHBIAS. | | DestBlend | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dblend"><strong>que D3DBLEND</strong></a> sin el D3DBLEND_ predeterminado. | | DitherEnable | bool | True o False. Los mismos valores que D3DRS_DITHERENABLE. | | FillMode | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>que D3DFILLMODE</strong></a> sin el D3DFILL_ predeterminado. | | LastPixel | dword | True o False. Consulte D3DRS_LASTPIXEL. | | ShadeMode | dword | Los mismos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sin el D3DSHADE_ predeterminado. | | PendienteEscalaDepthBias | float | Los mismos valores que D3DRS_SLOPESCALEDEPTHBIAS. | | SrcBlend | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dblend"><strong>que D3DBLEND</strong></a> sin el D3DBLEND_ predeterminado. | | SRGBWriteEnable | bool | True o False. Los mismos valores que D3DRS_SRGBWRITEENABLE. | | Galería de símbolosEnable | bool | True o False. Los mismos valores que D3DRS_STENCILENABLE. | | StencilFail | dword | Los mismos valores <a href="d3dstencilcaps.md">que D3DSTENCILCAPS</a> sin el D3DSTENCILCAP_ predeterminado. Consulte D3DRS_STENCILFAIL. | | StencilFunc | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>que D3DCMPFUNC</strong></a> sin el D3DCMP_ predeterminado. Consulte D3DRS_STENCILFUNC. | | StencilMask | dword | Los mismos valores que D3DRS_STENCILMASK. | | StencilPass | dword | Los mismos valores <a href="d3dstencilcaps.md">que D3DSTENCILCAPS</a> sin el D3DSTENCILCAP_ predeterminado. Consulte D3DRS_STENCILPASS. | | StencilRef | int | Los mismos valores que D3DRS_STENCILREF. | | StencilWriteMask | dword | Los mismos valores que D3DRS_STENCILWRITEMASK. | | StencilZFail | dword | Los mismos valores <a href="d3dstencilcaps.md">que D3DSTENCILCAPS</a> sin el D3DSTENCILCAP_ predeterminado. Consulte D3DRS_STENCILZFAIL. | | TextureFactor | dword | Los mismos valores <a href="d3dcolor.md"><strong>que D3DCOLOR</strong></a>. Los mismos valores que D3DRS_TEXTUREFACTOR. | | Wrap0- Wrap15 | dword | Los valores son los mismos que los que usa D3DRS_WRAP0. Los valores válidos son:<ul><li>COORD0 (que corresponde a D3DWRAPCOORD_0)</li><li>COORD1 (que corresponde a D3DWRAPCOORD_1)</li><li>COORD2 (que corresponde a D3DWRAPCOORD_2)</li><li>COORD3 (que corresponde a D3DWRAPCOORD_3)</li><li>U (que corresponde a D3DWRAP_U)</li><li>V (que corresponde a D3DWRAP_V)</li><li>W (que corresponde a D3DWRAP_W)</li></ul> | | ZEnable | dword | Los mismos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3BUFFERTYPE</strong></a> sin el D3DZB_ predeterminado. | | ZFunc | dword | Los mismos valores <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>que D3DCMPFUNC</strong></a> sin el D3DCMP_ predeterminado. Consulte D3DRS_ZFUNC. | | ZWriteEnable | bool | True o False. Consulte D3DRS_ZWRITEENABLE. | 




 

Ejemplo:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Esto habilitará la combinación alfa y hará que todas las geometrías se representen en wireframe.

### <a name="vertex-pipe-render-states"></a>Estados de representación de la canalización de vértices

Los estados de representación del archivo de efecto tienen nombres similares a los estados de canalización de función fija, a menudo con el prefijo quitado.



| Estado de representación             | Tipo   | Valores                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Ambiente                  | float4 | Los mismos valores que D3DRS \_ AMBIENT.                                                                                                                |
| AmbientMaterialSource    | dword  | Los mismos valores [**que D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el prefijo D3DMCS. \_ Consulte D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Recorte                 | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ CLIPPING.                                                                                                |
| ClipPlaneEnable          | dword  | Combinación bit a bit de macros D3DCLIPPLANE0 - D3DCLIPPLANE5. Consulte [**D3DCLIPPLANEn**](d3dclipplanen.md) y D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ COLORVERTEX.                                                                                             |
| CullMode                 | dword  | Los mismos valores que [**D3DCULL**](./d3dcull.md) sin el prefijo D3DCULL. \_                                                                 |
| DifusoMaterialSource    | dword  | Los mismos valores [**que D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el prefijo D3DMCS. \_ Consulte D3DRS \_ DIFUSMATERIALSOURCE.  |
| EmissiveMaterialSource   | dword  | Los mismos valores [**que D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el prefijo D3DMCS. \_ Consulte D3DRS \_ EMISSIVEMATERIALSOURCE. |
| ColorColor                 | dword  | Los mismos valores [**que D3DCOLOR**](d3dcolor.md). Consulte \_ D3DRSCOLOR.                                                                             |
| DadDensity               | FLOAT  | Los mismos valores que \_ D3DRSRDDENSITY.                                                                                                             |
| AnómaloEnable                | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ RAGENABLE.                                                                                               |
| Endend                   | FLOAT  | Los mismos valores que \_ D3DRSRDEND.                                                                                                                 |
| Startstart deStart                 | FLOAT  | Los mismos valores que D3DRSSTART \_ DESTART.                                                                                                               |
| ModeTablaTabla             | dword  | Los mismos valores [**que D3DFOGMODE.**](./d3dfogmode.md) Vea \_ D3DRSRENDERTABLEMODE en [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| VertexMode deVertex            | dword  | Los mismos valores que [**D3DFOGMODE**](./d3dfogmode.md) sin el prefijo D3DFOG. \_                                                            |
| IndexedVertexBlendEnable | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Iluminación                 | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ LIGHTING.                                                                                                |
| LocalViewer              | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Los mismos valores que D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | dword  | Los mismos valores que D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | FLOAT  | Los mismos valores que nSegments [**en SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | FLOAT  | Los mismos valores que D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Los mismos valores que D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| PointSize                | FLOAT  | Los mismos valores que D3DRS \_ POINTSIZE.                                                                                                              |
| PointSize \_ Min           | FLOAT  | Los mismos valores que D3DRS \_ POINTSIZE \_ MIN.                                                                                                         |
| PointSize \_ Max           | FLOAT  | Los mismos valores que D3DRS \_ POINTSIZE \_ MAX sin el prefijo D3DRS. \_                                                                              |
| PointSpriteEnable        | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Verdadero o Falso. Los mismos valores que D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | dword  | Los mismos valores [**que D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el prefijo D3DMCS. \_ Consulte D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | FLOAT  | Los mismos valores que D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | dword  | Los mismos valores [**que D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sin el prefijo D3DVBF. \_ Consulte D3DRS \_ VERTEXBLEND.                  |



 

Ejemplo:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Esto hará que el color ambiente float4<0.7f, 0.0f, 0.0f, 1.0f>, establezca el modo de selección de la cara posterior en el sentido contrario a las agujas del reloj y establezca el color de la paleta en rojo.

## <a name="sampler-states"></a>Estados del muestreador

Un estado de sampler representa un objeto sampler.



| State   | Tipo    | Valores                              |
|---------|---------|-------------------------------------|
| Muestra | Sampler | **NULL** o un bloque de estado de muestreador. |



 

## <a name="sampler-stage-states"></a>Estados de la fase del muestreador

Los estados de la fase del muestreador se usan para muestrear texturas. El estado del muestreador determina los tipos de filtrado y los modos de direccionamiento de textura.



| Estado del muestreador       | Tipo                         | Valores                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| AddressU \[ 16\]      | dword                        | Los mismos valores [**que D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el prefijo D3DTADDRESS. \_ Consulte D3DSAMP \_ ADDRESSU.      |
| AddressV \[ 16\]      | dword                        | Los mismos valores [**que D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el prefijo D3DTADDRESS. \_ Consulte D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | dword                        | Los mismos valores [**que D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el prefijo D3DTADDRESS. \_ Consulte D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Los mismos valores [**que D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el prefijo D3DTEXF. \_ Consulte D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | dword                        | Los mismos valores [**que D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el prefijo D3DTEXF. \_ Consulte D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | dword                        | Los mismos valores que D3DSAMP \_ MAXANISOTROPY sin el prefijo \_ D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | int                          | Los mismos valores que D3DSAMP \_ MAXMIPLEVEL sin el prefijo D3DSAMP. \_                                                                 |
| MinFilter \[ 16\]     | dword                        | Los mismos valores que D3DSAMP \_ MINFILTER sin el prefijo D3DSAMP. \_                                                                   |
| MipFilter \[ 16\]     | dword                        | Los mismos valores que D3DSAMP \_ MIPFILTER sin el prefijo D3DSAMP. \_                                                                   |
| MipMapLodBias \[ 16\] | FLOAT                        | Los mismos valores que D3DSAMP \_ MIPMAPLODBIAS sin el prefijo \_ D3DSAMP.                                                               |
| SRGBTexture         | bool                         | El mismo valor que D3DSAMP \_ SRGBTEXTURE sin el prefijo D3DSAMP. \_                                                                   |



 

Ejemplo:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Esto fija los valores UVW entre 0 y 1.

## <a name="shader-states"></a>Estados del sombreador

Solo hay dos estados de sombreador de efectos: uno asociado a un objeto de sombreador de vértices y otro asociado a un objeto de sombreador de píxeles.



| Estado del sombreador | Tipo         | Valores                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| PixelShader  | pixelshader  | **NULL,** un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles. |
| VertexShader | vertexshader | **NULL,** un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles. |



 

Ejemplo:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Esto compilará VSTexture, un sombreador de vértices definido anteriormente en el archivo .fx, en la versión 1.1 del sombreador de vértices y, a continuación, establecerá ese sombreador compilado como sombreador de vértices. El sombreador de píxeles se asigna a **NULL.**

## <a name="shader-constant-states"></a>Estados constantes del sombreador

Los estados constantes del sombreador se usan para tener acceso a los parámetros constantes del sombreador.



| Estado constante del sombreador | Tipo            | Valores                                       |
|-----------------------|-----------------|----------------------------------------------|
| PixelShaderConstant   | float \[ m \[ n\]\] | m x n matriz de floats; m y n son opcionales. |
| PixelShaderConstant1  | float4          | Un flotante 4D.                                |
| PixelShaderConstant2  | float4x2        | Dos flotantes 4D.                               |
| PixelShaderConstant3  | float4x3        | Tres flotantes 4D.                             |
| PixelShaderConstant4  | float4x4        | Cuatro flotantes 4D.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | m x n matriz de bools; m y n son opcionales.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | Matriz m x n de ints. m y n son opcionales.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | Matriz m x n de floats. m y n son opcionales. |
| VertexShaderConstant  | float \[ m \[ n\]\] | Matriz m x n de floats. m y n son opcionales. |
| VertexShaderConstant1 | float4          | Un flotante 4D.                                |
| VertexShaderConstant2 | float4x2        | Dos flotantes 4D.                               |
| VertexShaderConstant3 | float4x3        | Tres flotantes 4D.                             |
| VertexShaderConstant4 | float4x4        | Cuatro flotantes 4D.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | m x n matriz de bools. m y n son opcionales.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | Matriz m x n de ints. m y n son opcionales.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | Matriz m x n de floats. m y n son opcionales. |



 

## <a name="texture-states"></a>Estados de textura

Los estados de textura inicializan texturas usadas por el combinador de varios texto.



| Estado de textura | Tipo    | Valores                            |
|---------------|---------|-----------------------------------|
| Textura \[ 8\]  | textura | **NULL** o un parámetro de textura. |



 

## <a name="texture-stage-states"></a>Estados de la fase de textura

Los estados de la fase de textura establecen texturas y las fases de textura en el combinador de varios texto.



| Estado de la fase de textura        | Tipo  | Valores                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlphaOp \[ 8\]               | dword | Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el prefijo D3DTOP. \_ Consulte D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | dword | Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el prefijo D3DTOP. \_ Consulte COLOROP de D3DTSS. \_                                                      |
| BumpEnvLScale \[ 8\]         | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVLSCALE sin el prefijo TCI de D3DTSS. \_                                                                                      |
| BumpEnvLOffset \[ 8\]        | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVLOFFSET sin el prefijo TCI de D3DTSS. \_                                                                                     |
| BumpEnvMat00 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | FLOAT | Los mismos valores que D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | dword | Igual que [D3DTA](d3dta.md) sin el prefijo D3DTA. \_ Consulte D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | dword | Los mismos valores que D3DTSS \_ TEXCOORDINDEX sin el prefijo \_ TCI D3DTSS.                                                                                      |
| TextureTransformFlags \[ 8\] | dword | Los mismos valores [**que los valores D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sin el prefijo D3DTTFF. \_ Vea TEXTURATRANSFORMFLAGS de \_ D3DTSS. |



 

## <a name="transform-states"></a>Transformar estados

Establezca los estados de transformación para inicializar matrices de transformación. Los efectos usan matrices transpuestas para mejorar la eficacia. Puede proporcionar matrices transpuestas a un efecto o un efecto transpone automáticamente las matrices antes de usarlos.



| Estado de transformación       | Tipo     | Valores                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| ProjectionTransform   | float4x4 | Matriz de flotantes de 4x4. Los mismos valores que D3DTS \_ PROJECTION sin el prefijo D3DTS. \_                                            |
| TextureTransform \[ 8\] | float4x4 | Matriz de flotantes de 4x4. Los mismos valores [**que D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sin el prefijo D3DTS. \_ |
| ViewTransform         | float4x4 | Matriz de flotantes de 4x4. Los mismos valores que D3DTS \_ VIEW sin el prefijo D3DTS. \_                                                  |
| WorldTransform        | float4x4 | Matriz de flotantes de 4x4.                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 

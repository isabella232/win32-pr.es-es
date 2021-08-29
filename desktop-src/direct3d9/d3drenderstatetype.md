---
description: Los estados de representación definen estados de configuración para todos los tipos de procesamiento de vértices y píxeles.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeración D3DRENDERSTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4678a31d53fa11dbc61788afd7f59df79a41ae67cb60c5e178a021d9737b7d0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096325"
---
# <a name="d3drenderstatetype-enumeration"></a>D3DRENDERSTATETYPE (enumeración)

Los estados de representación definen estados de configuración para todos los tipos de procesamiento de vértices y píxeles. Algunos estados de representación configuraron el procesamiento de vértices y otros configuraron el procesamiento de píxeles (consulte Estados de representación [(Direct3D 9)](render-states.md)). Los estados de representación se pueden guardar y restaurar mediante bloques de estado (vea Bloques de estado Guardar y restaurar estado [(Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

Estado de almacenamiento en búfer de profundidad como un miembro del tipo enumerado [**D3BUFFERBUFFERTYPE.**](./d3dzbuffertype.md) Establezca este estado en D3D AHORA TRUE para habilitar el almacenamiento en búfer \_ z, D3D BUFFER USEW para habilitar \_ w-buffering o D3D DOMAIN FALSE para deshabilitar el almacenamiento en búfer de \_ profundidad.

El valor predeterminado para este estado de representación es D3DIVER TRUE si se creó una galería de símbolos de profundidad junto con la cadena de intercambio estableciendo el miembro \_ EnableAutoDepthStencil de la estructura [**PARAMETERS \_ D3DPRESENT**](d3dpresent-parameters.md) en **TRUE** y D3DOXI FALSE en caso \_ contrario.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

Uno o varios miembros del [**tipo enumerado D3DFILLMODE.**](./d3dfillmode.md) El valor predeterminado es D3DFILL \_ SOLID.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Uno o varios miembros del [**tipo enumerado D3DSHADEMODE.**](./d3dshademode.md) El valor predeterminado es D3DSHADE \_ GOURAUD.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**TRUE** para permitir que la aplicación escriba en el búfer de profundidad. El valor predeterminado es **TRUE.** Este miembro permite que una aplicación impida que el sistema actualice el búfer de profundidad con nuevos valores de profundidad. Si **es FALSE,** las comparaciones de profundidad se siguen haciendo según el estado de representación D3DRS RAGUNC, suponiendo que se está llevando a cabo el almacenamiento en búfer de profundidad, pero los valores de profundidad no se escriben en el \_ búfer.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**TRUE** para habilitar las pruebas alfa por píxel. Si la prueba se supera, el búfer de fotogramas procesa el píxel. De lo contrario, se omite todo el procesamiento del búfer de fotogramas para el píxel.

La prueba se realiza comparando el valor alfa entrante con el valor alfa de referencia, mediante la función de comparación proporcionada por el estado de representación de D3DRS \_ ALPHAFUNC. El valor alfa de referencia viene determinado por el valor establecido para D3DRS \_ ALPHAREF. Para obtener más información, vea [Alpha Testing State (Direct3D 9).](alpha-testing-state.md)

El valor predeterminado de este parámetro es **FALSE.**

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

El valor predeterminado es **TRUE,** que permite dibujar el último píxel de una línea. Para evitar el dibujo del último píxel, establezca este valor en **FALSE.** Para obtener más información, vea [Esquema y estado de relleno (Direct3D 9).](outline-and-fill-state.md)

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md) El valor predeterminado es D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md) El valor predeterminado es D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

Especifica cómo se culled los triángulos orientados hacia atrás, si es posible. Se puede establecer en un miembro del [**tipo enumerado D3DCULL.**](./d3dcull.md) El valor predeterminado es D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRSUNC \_**
</dt> <dd>

Un miembro del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) El valor predeterminado es D3DCMP \_ LESSEQUAL. Este miembro permite que una aplicación acepte o rechace un píxel, en función de su distancia desde la cámara.

El valor de profundidad del píxel se compara con el valor de búfer de profundidad. Si el valor de profundidad del píxel pasa la función de comparación, se escribe el píxel.

El valor de profundidad se escribe en el búfer de profundidad solo si el estado de representación es **TRUE.**

Los rasterizadores de software y muchos aceleradores de hardware funcionan más rápido si se produce un error en la prueba de profundidad, ya que no es necesario filtrar y modular la textura si el píxel no se va a representar.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

Valor que especifica un valor alfa de referencia con el que se prueban los píxeles cuando se habilitan las pruebas alfa. Se trata de un valor de 8 bits colocado en los 8 bits inferiores del valor de estado de representación DWORD. Los valores pueden oscilar entre 0x00000000 a 0x000000FF. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

Un miembro del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) El valor predeterminado es D3DCMP \_ ALWAYS. Este miembro permite que una aplicación acepte o rechace un píxel, en función de su valor alfa.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**TRUE** para habilitar la dithering. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**TRUE** para habilitar la transparencia mezclada alfa. El valor predeterminado es **FALSE**.

El tipo de combinación alfa viene determinado por los estados de representación D3DRS \_ SRCBLEND y D3DRS \_ DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ RAGENABLE**
</dt> <dd>

**TRUE** para habilitar la mezcla de mezcla. El valor predeterminado es **FALSE**. Para obtener más información sobre el uso de la mezcla de fusión, vea [Verón .](fog.md)

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**TRUE** para habilitar los resaltados especulares. El valor predeterminado es **FALSE**.

Los resaltados especulares se calculan como si cada vértice del objeto que se enciende se encuentra en el origen del objeto. Esto proporciona los resultados esperados siempre que el objeto se modele alrededor del origen y la distancia entre la luz y el objeto sea relativamente grande. En otros casos, los resultados son indefinidos.

Cuando este miembro se establece en **TRUE,** el color especular se agrega al color base después de la cascada de textura, pero antes de la mezcla alfa.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**
</dt> <dd>

Valor cuyo tipo es [**D3DCOLOR.**](d3dcolor.md) El valor predeterminado es 0. Para obtener más información sobre el color blanco, vea [Color de color blanco (Direct3D 9).](fog-color.md)

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ CONFIGURABLEMODE**
</dt> <dd>

Fórmula de matriz que se va a usar para píxeles de píxeles. Establezca en uno de los miembros del [**tipo enumerado D3DFOGMODE.**](./d3dfogmode.md) El valor predeterminado es D3DFOG \_ NONE. Para obtener más información sobre píxeles de píxeles, vea [Pixel Pixel (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRSSTART \_**
</dt> <dd>

Profundidad a la que comienzan los efectos de vértice o píxel para el modo de velocidad lineal. El valor predeterminado es 0,0f. La profundidad se especifica en el espacio mundial para el vértice de vértices y el espacio del dispositivo \[ 0,0, 1,0 o el espacio del mundo para el \] ángulo de píxeles. En el caso de píxeles de píxeles, estos valores están en el espacio del dispositivo cuando el sistema usa z para los cálculos de cálculos de cálculo y el espacio mundial cuando el sistema usa la zona relativa a los ojos (w-wu). Para obtener más información, vea [Parámetros de parámetros de parámetro de vuelo (Direct3D 9)](fog-parameters.md) y Relación con los ojos frente a profundidad basada en [Z.](pixel-fog.md)

Los valores para este estado de representación son valores de punto flotante. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRSEND \_**
</dt> <dd>

Profundidad a la que finalizan los efectos de vértice o píxel para el modo de velocidad lineal. El valor predeterminado es 1,0f. La profundidad se especifica en el espacio del mundo para el vértice y el espacio del dispositivo \[ 0,0, 1,0 o el espacio del mundo para el \] ángulo de píxeles. En el caso de píxeles, estos valores están en el espacio del dispositivo cuando el sistema usa z para los cálculos de cálculos de cálculo y en el espacio del mundo cuando el sistema usa el ojo relativo a los ojos (w-wu). Para obtener más información, vea [Parámetros de parámetros de parámetro (Direct3D 9)](fog-parameters.md) y Relación con los ojos frente a profundidad basada en [Z.](pixel-fog.md)

Los valores de este estado de representación son valores de punto flotante. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRSRDDENSITY**
</dt> <dd>

Densidad de densidad de píxeles o vértices usada en los modos de curva exponencial (D3DFOG \_ EXP y D3DFOG \_ EXP2). Los valores de densidad válidos oscilan entre 0,0 y 1,0. El valor predeterminado es 1,0. Para obtener más información, vea [Parámetros de Parámetros de parámetros de parámetros de Parámetros de parámetros (Direct3D 9)](fog-parameters.md).

Los valores de este estado de representación son valores de punto flotante. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**TRUE** para habilitar el vértice basado en intervalos. El valor predeterminado es **FALSE,** en cuyo caso el sistema usa el sistema basado en profundidad. En los intervalos basados en intervalos, la distancia de un objeto desde el visor se usa para calcular los efectos de los sonidos, no la profundidad del objeto (es decir, la coordenada z) de la escena. En los intervalos basados en intervalos, todos los métodos de métodos de distribución funcionan como de costumbre, excepto que usan el intervalo en lugar de la profundidad en los cálculos.

El intervalo es el factor correcto que se debe usar para los cálculos de cálculos de computación, pero la profundidad se usa normalmente en su lugar porque el intervalo tarda mucho tiempo en calcularse y la profundidad ya está disponible con carácter general. El uso de profundidad para calcular la profundidad tiene el efecto no deseado de que la disponibilidad de los objetos periféricos cambie a medida que se mueve el ojo del visor; en este caso, la profundidad cambia y el intervalo permanece constante.

Dado que actualmente ningún hardware admite el rango por píxel basado en el rango, la corrección del intervalo solo se ofrece para vértices.

Para obtener más información, vea [Vértices de vértice (Direct3D 9).](vertex-fog.md)

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**TRUE** para habilitar la galería de símbolos o **FALSE para** deshabilitar la galería de símbolos. El valor predeterminado es **FALSE**. Para obtener más información, vea Técnicas de búfer de galería [de símbolos (Direct3D 9).](stencil-buffer-techniques.md)

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCINCIIL**
</dt> <dd>

Operación de galería de símbolos que se realizará si se produce un error en la prueba de galería de símbolos. Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Operación de galería de símbolos que se realizará si se supera la prueba de galería de símbolos y se produce un error en la prueba de profundidad (z-test). Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Operación de galería de símbolos que se realizará si se supera la galería de símbolos y las pruebas de profundidad (z). Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Función de comparación para la prueba de galería de símbolos. Los valores son del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) El valor predeterminado es D3DCMP \_ ALWAYS.

La función de comparación se usa para comparar el valor de referencia con una entrada de búfer de galería de símbolos. Esta comparación solo se aplica a los bits del valor de referencia y la entrada del búfer de galería de símbolos que se establecen en la máscara de galería de símbolos (establecida por el estado de representación \_ STENCILMASK de D3DRS). Si **es TRUE,** se supera la prueba de galería de símbolos.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Valor de referencia int para la prueba de galería de símbolos. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Máscara aplicada al valor de referencia y a cada entrada de búfer de galería de símbolos para determinar los bits significativos de la prueba de galería de símbolos. La máscara predeterminada es 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

Máscara de escritura aplicada a los valores escritos en el búfer de galería de símbolos. La máscara predeterminada es 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

Color que se usa para la combinación de varias texturas con el argumento de mezcla de textura de TFACTOR D3DTA o la operación de mezcla de \_ texturas D3DTOP \_ BLENDFACTORALPHA. El valor asociado es una variable [**D3DCOLOR.**](d3dcolor.md) El valor predeterminado es blanco opaco (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Comportamiento de ajuste de textura para varios conjuntos de coordenadas de textura. Los valores válidos para este estado de representación pueden ser cualquier combinación de las marcas D3DWRAPCOORD \_ 0 (o D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP W) y \_ D3DWRAPCOORD \_ 3. Esto hace que el sistema se ajuste en la dirección de las dimensiones primera, segunda, tercera y cuarta, a veces denominadas direcciones s, t, r y q, para una textura determinada. El valor predeterminado para este estado de representación es 0 (ajuste deshabilitado en todas las direcciones).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**RECORTE DE \_ D3DRS**
</dt> <dd>

**TRUE** para habilitar el recorte primitivo por Direct3D o **FALSE** para deshabilitarlo. El valor predeterminado es **TRUE.**

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**ILUMINACIÓN D3DRS \_**
</dt> <dd>

**TRUE** para habilitar la iluminación de Direct3D o **FALSE** para deshabilitarla. El valor predeterminado es **TRUE.** Solo los vértices que incluyen un vértice normal se encienden correctamente; Los vértices que no contienen un normal emplean un producto de punto de 0 en todos los cálculos de iluminación.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**
</dt> <dd>

Color claro ambiente. Este valor es de tipo [**D3DCOLOR.**](d3dcolor.md) El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_D3DRSVERTEXMODE**
</dt> <dd>

Fórmula de ángulo que se va a usar para vértices. Se establece en un miembro del [**tipo enumerado D3DFOGMODE.**](./d3dfogmode.md) El valor predeterminado es D3DFOG \_ NONE.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**TRUE** para habilitar el color por vértice o **FALSE** para deshabilitarlo. El valor predeterminado es **TRUE.** Al habilitar el color por vértice, el sistema puede incluir el color definido para los vértices individuales en sus cálculos de iluminación.

Para obtener más información, vea los siguientes estados de representación:

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**TRUE** para habilitar los resaltados especulares relativos a la cámara o **FALSE** para usar resaltados ortogonales especulares. El valor predeterminado es **TRUE.** Las aplicaciones que usan proyección ortogonal deben especificar **FALSE.**

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**TRUE** para habilitar la normalización automática de normales de vértices o **FALSE** para deshabilitarla. El valor predeterminado es **FALSE**. Al habilitar esta característica, el sistema normaliza los normales de vértice para los vértices después de transformarlos en espacio de la cámara, lo que puede llevar mucho tiempo.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

Origen de color difuso para cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) El valor predeterminado es D3DMCS \_ COLOR1. El valor de este estado de representación solo se usa si el estado de representación COLORVERTEX de D3DRS \_ está establecido en **TRUE.**

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Origen de color especular para cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) El valor predeterminado es D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Origen de color ambiente para cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) El valor predeterminado es D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Origen de color emisivo para los cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) El valor predeterminado es D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

Número de matrices que se usarán para realizar la combinación de geometría, si hay alguna. Los valores válidos son miembros del [**tipo enumerado D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) El valor predeterminado es D3DVBF \_ DISABLE.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**CLIPPLANEENABLE DE D3DRS \_**
</dt> <dd>

Habilita o deshabilita los planos de recorte definidos por el usuario. Los valores válidos son cualquier DWORD en el que el estado de cada bit (establecido o no establecido) alterna el estado de activación de un plano de recorte definido por el usuario correspondiente. El bit menos significativo (bit 0) controla el primer plano de recorte en el índice 0 y los bits posteriores controlan la activación de los planos de recorte en índices más altos. Si se establece un bit, el sistema aplica el plano de recorte adecuado durante la representación de la escena. El valor predeterminado es 0.

Las macros [**D3DCLIPPLANEn**](d3dclipplanen.md) se definen para proporcionar una manera cómoda de habilitar los planos de recorte.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**
</dt> <dd>

Valor float que especifica el tamaño que se va a usar para el cálculo de tamaño de punto en casos en los que no se especifica el tamaño de punto para cada vértice. Este valor no se usa cuando el vértice contiene el tamaño de punto. Este valor está en unidades de espacio de pantalla si D3DRS POINTSCALEENABLE es FALSE; de lo contrario, este \_ valor está en unidades espaciales del mundo. El valor predeterminado es el valor que devuelve un controlador. Si un controlador devuelve 0 o 1, el valor predeterminado es 64, lo que permite emular el tamaño del punto de software. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ APUNTA A \_ MIN**
</dt> <dd>

Valor float que especifica el tamaño mínimo de los primitivos de punto. Las primitivas de punto se fijan a este tamaño durante la representación. Si se establece en valores menores que 1,0, los puntos se descartan cuando el punto no cubre un centro de píxeles y el suavizado de contorno se deshabilita o se representa con menor intensidad cuando se habilita el suavizado de contorno. El valor predeterminado es 1,0f. El intervalo de este valor es mayor o igual que 0,0f. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**PUNTOS \_ D3DRSPRITEENABLE**
</dt> <dd>

valor bool. Cuando **es TRUE,** las coordenadas de textura de las primitivas de punto se establecen para que las texturas completa se asignen a cada punto. Cuando **es FALSE,** las coordenadas de textura de vértice se usan para todo el punto. El valor predeterminado es **FALSE**. Puede lograr puntos de un solo píxel de estilo DirectX 7 estableciendo D3DRS \_ POINTSCALEENABLE en **FALSE** y D3DRS POINTSIZE en 1.0, que son los valores \_ predeterminados.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

valor bool que controla el cálculo del tamaño de las primitivas de punto. Cuando **es TRUE,** el tamaño del punto se interpreta como un valor de espacio de la cámara y se escala mediante la función distance y el frustum para la ventanilla y el escalado del eje Y para calcular el tamaño final del punto de espacio en pantalla. Cuando **es FALSE,** el tamaño del punto se interpreta como espacio de pantalla y se usa directamente. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto. Solo está activo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.** El valor predeterminado es 1,0f. El intervalo de este valor es mayor o igual que 0,0f. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto. Solo está activo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.** El valor predeterminado es 0,0f. El intervalo de este valor es mayor o igual que 0,0f. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto. Solo está activo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.** El valor predeterminado es 0,0f. El intervalo de este valor es mayor o igual que 0,0f. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

valor bool que determina cómo se calculan las muestras individuales al usar un búfer de destino de representación multimuestreo. Cuando se establece en **TRUE**, se calculan las múltiples muestras para que el suavizado de contorno de escena completa se realice mediante el muestreo en diferentes posiciones de muestra para cada muestra múltiple. Cuando se establece en **FALSE,** todas las muestras se escriben con el mismo valor de ejemplo, muestreados en el centro de píxeles, lo que permite la representación sin suavizado de contorno en un búfer de varios ejemplos. Este estado de representación no tiene ningún efecto al representar en un solo búfer de ejemplo. El valor predeterminado es **TRUE.**

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Cada bit de esta máscara, empezando por el bit menos significativo (LSB), controla la modificación de uno de los ejemplos en un destino de representación multimuestreo. Por lo tanto, para un destino de representación de 8 muestras, el byte bajo contiene las ocho escrituras que se habilitan para cada una de las ocho muestras. Este estado de representación no tiene ningún efecto al representar en un solo búfer de ejemplo. El valor predeterminado es 0xFFFFFFFF.

Este estado de representación permite el uso de un búfer de varios ejemplos como búfer de acumulación, realizando la representación multipass de geometry donde cada paso actualiza un subconjunto de ejemplos.

Si hay n muestras habilitadas para varios ejemplos y k, la intensidad resultante de la imagen representada debe ser k/n. Cada componente RGB de cada píxel se factorizó por k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Establece si los bordes de revisión usarán teselación de estilo float. El tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) define los valores posibles. El valor predeterminado es D3DPATCHEDGE \_ DISCRETE.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Establezca solo para depurar el monitor. El tipo enumerado [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) define los valores posibles. Tenga en cuenta que si D3DRS DEBUGMONITORTOKEN está establecido, la llamada se trata como pasar \_ un token al monitor de depuración. Por ejemplo, si después de pasar D3DDMT ENABLE o \_ D3DDMT DISABLE a \_ D3DRS DEBUGMONITORTOKEN, se pasan otros valores de token, el estado (habilitado o deshabilitado) del monitor de depuración se \_ conservará.

Este estado solo es útil para las compilaciones de depuración. El monitor de depuración tiene como valor predeterminado D3DDMT \_ ENABLE.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**
</dt> <dd>

Valor float que especifica el tamaño máximo al que se fijarán los sprites de punto. El valor debe ser menor o igual que el miembro MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) y mayor o igual que D3DRS \_ POINTSIZE \_ MIN. El valor predeterminado es 64,0. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

valor bool que habilita o deshabilita la combinación de vértices indexados. El valor predeterminado es **FALSE**. Cuando se establece en **TRUE,** se habilita la combinación de vértices indexados. Cuando se establece en **FALSE,** la combinación de vértices indexados está deshabilitada. Si este estado de representación está habilitado, el usuario debe pasar índices de matriz como DWORD empaquetadocon cada vértice. Cuando se deshabilita el estado de representación y la combinación de vértices se habilita a través del estado VERTEXBLEND de D3DRS, equivale a tener índices de \_ matriz 0, 1, 2, 3 en cada vértice.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

Valor UINT que permite una escritura por canal para el búfer de color de destino de representación. Un bit de conjunto da como resultado que el canal de color se actualice durante la representación en 3D. Un bit claro da como resultado que el canal de color no se vería afectado. Esta funcionalidad está disponible si el bit de funcionalidades COLORWRITEENABLE de D3DPMISCCAPS está establecido en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo. Este estado de representación no afecta a la operación de borrar. El valor predeterminado es 0x0000000F.

Los valores válidos para este estado de representación pueden ser cualquier combinación de las marcas RED D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN o \_ D3DCOLORWRITEENABLE \_ RED.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Valor float que controla el factor de interpolación. El valor predeterminado es 0,0f. Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**BLENDOP de D3DRS \_**
</dt> <dd>

Valor utilizado para seleccionar la operación aritmética aplicada cuando el estado de representación de combinación alfa, D3DRS \_ ALPHABLENDENABLE, se establece en **TRUE.** El tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) define los valores válidos. El valor predeterminado es D3DBLENDOP \_ ADD.

Si no se admite la funcionalidad del dispositivo BLENDOP D3DPMISCCAPS, se realiza \_ D3DBLENDOP \_ ADD.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

Grado de interpolación de la posición de N revisiones. Los valores pueden ser D3DDEGREE \_ CUBIC (valor predeterminado) o D3DDEGREE \_ LINEAR. Para obtener más información, [**vea D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

Grado de interpolación normal de N revisiones. Los valores pueden ser D3DDEGREE \_ LINEAR (valor predeterminado) o D3DDEGREE \_ QUADRATIC. Para obtener más información, [**vea D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS- \_ LAPRUEBATESTENABLE**
</dt> <dd>

**TRUE** para habilitar las pruebas de mossos **y FALSE** para deshabilitarla. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ PENDIENTECALEDEPTHBIAS**
</dt> <dd>

Se usa para determinar la cantidad de sesgo que se puede aplicar a las primitivas planas para reducir el z-fighting. El valor predeterminado es 0.

bias = (max \* D3DRS \_ CTRLCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

donde max es la pendiente de profundidad máxima del triángulo que se representa.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**TRUE** para habilitar el suavizado de contorno de línea, **FALSE para** deshabilitar el suavizado de contorno de línea. El valor predeterminado es **FALSE**.

Al representar en un destino de representación multimuestreo, D3DRS ANTIALIASEDLINEENABLE se omite y todas las líneas se representan \_ con alias. Use [**ID3DXLine para la**](id3dxline.md) representación de líneas suavizadas en un destino de representación multimuestreo.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Nivel mínimo de teselación. El valor predeterminado es 1,0f. Vea [Teselación (Direct3D 9).](tessellation.md)

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Nivel de teselación máximo. El valor predeterminado es 1,0f. Vea [Teselación (Direct3D 9).](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Cantidad que se puede tesentar de forma adaptable, en la dirección x. El valor predeterminado es 0,0f. Consulte [Tessellation adaptable.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Cantidad que se puede tesentar de forma adaptable, en la dirección y. El valor predeterminado es 0,0f. Consulte [ \_ Tessellation adaptable.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Cantidad que se puede tesentar de forma adaptable, en la dirección z. El valor predeterminado es 1,0f. Consulte [ \_ Tessellation adaptable.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Cantidad que se puede tesentar de forma adaptable, en la dirección w. El valor predeterminado es 0,0f. Consulte [ \_ Tessellation adaptable.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**TRUE** para habilitar la teselación adaptable, **FALSE** para deshabilitarla. El valor predeterminado es **FALSE**. Consulte [ \_ Tessellation adaptable.](tessellation.md)

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**TRUE** habilita la galería de símbolos de dos lados y **FALSE** la deshabilita. El valor predeterminado es **FALSE**. La aplicación debe establecer D3DRS \_ CULLMODE en D3DCULL NONE para habilitar el modo de \_ galería de símbolos de dos lados. Si el orden de enrollado del triángulo es en el sentido de las agujas del reloj, se usarán las operaciones D3DRS \_ STENCIL. \* Si el orden de cierre es en sentido contrario a las agujas del reloj, se usarán las operaciones \_ STENCIL de CCW de D3DRS. \_ \*

Para ver si se admite la galería de símbolos de dos lados, compruebe el miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED. Vea también [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCINCINCIIL**
</dt> <dd>

Operación de galería de símbolos que se realizará si se produce un error en la prueba de galería de símbolos CCW. Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Operación de galería de símbolos que se realizará si se supera la prueba de galería de símbolos CCW y se produce un error en la prueba z. Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Operación de galería de símbolos que se realizará si se supera la galería de símbolos CCW y las pruebas z. Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md) El valor predeterminado es D3DSTENCI \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Función de comparación. La prueba de galería de símbolos CCW se supera si la función de galería de símbolos ((ref & mask) (stencil & mask)) es **TRUE.** Los valores son del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md) El valor predeterminado es D3DCMP \_ ALWAYS.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Valores adicionales de ColorWriteEnable para los dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Valores adicionales de ColorWriteEnable para los dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Valores adicionales de ColorWriteEnable para los dispositivos. Consulte D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR se**](d3dcolor.md) usa para un factor de mezcla constante durante la mezcla alfa. Esta funcionalidad está disponible si el bit de funcionalidades DE BLENDFACTOR D3DPBLENDCAPS se establece en el miembro \_ SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o en el miembro DestBlendCaps de **D3DCAPS9.** Vea [**D3DRENDERSTATETYPE.**]() El valor predeterminado es 0xffffffff.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Habilite la corrección gamma de las escrituras de destino de representación en sRGB. El formato debe exponer D3DUSAGE \_ SRGBWRITE. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Valor de punto flotante que se usa para la comparación de valores de profundidad. Consulte [Sesgo de profundidad (Direct3D 9).](depth-bias.md) El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Consulte D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**TRUE** habilita el modo de combinación independiente para el canal alfa. El valor predeterminado es **FALSE**.

Cuando se establece en **FALSE,** los factores de combinación de destino de representación y las operaciones aplicadas a alfa se ven obligados a ser los mismos que los definidos para el color. Este modo se establece de forma eficaz en **FALSE** en implementaciones que no establecen el límite D3DPMISCCAPS \_ SEPARATEALPHABLEND. Vea [D3DPMISCCAPS](d3dpmisccaps.md).

El tipo de mezcla alfa independiente viene determinado por los estados de representación D3DRS \_ SRCBLEPHA y D3DRS \_ DESTBLEPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLEPHA**
</dt> <dd>

Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md) Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **TRUE.** El valor predeterminado es D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLEPHA**
</dt> <dd>

Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md) Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **TRUE.** El valor predeterminado es D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Valor utilizado para seleccionar la operación aritmética aplicada a la combinación alfa independiente cuando el estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE, se establece en **TRUE.**

El tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) define valores válidos. El valor predeterminado es D3DBLENDOP \_ ADD.

Si no se admite la funcionalidad del dispositivo BLENDOP D3DPMISCCAPS, \_ se realiza D3DBLENDOP \_ ADD. Vea [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios



| Estados de representación        |   Muestreador de textura                 |
|----------------------|--------------------|
| ps \_ 1 \_ 1 to ps \_ 1 \_ 3 | 4 muestreadores de textura |



 

Direct3D define la constante D3DRENDERSTATE WRAPBIAS como una comodidad para que las aplicaciones habiliten o deshabiliten el ajuste de textura, en función del entero de base cero de un conjunto de coordenadas de textura (en lugar de usar explícitamente uno de los valores de estado \_ D3DRS \_ WRAP n). Agregue el valor D3DRENDERSTATE WRAPBIAS al índice de base cero de un conjunto de coordenadas de textura para calcular el valor D3DRS WRAP n que corresponde a ese índice, como se muestra en el \_ \_ ejemplo siguiente.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 

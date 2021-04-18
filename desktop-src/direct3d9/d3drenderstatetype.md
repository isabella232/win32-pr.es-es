---
description: Los Estados de representación definen los Estados de configuración para todos los tipos de procesamiento de vértices y píxeles.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeración D3DRENDERSTATETYPE (D3D9Types. h)
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
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707779"
---
# <a name="d3drenderstatetype-enumeration"></a>Enumeración D3DRENDERSTATETYPE

Los Estados de representación definen los Estados de configuración para todos los tipos de procesamiento de vértices y píxeles. Algunos Estados de representación establecen el procesamiento de vértices y algunos conjuntos de procesamiento de píxeles (consulte [Estados de representación (Direct3D 9)](render-states.md)). Los Estados de representación se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxis


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

Estado de almacenamiento en búfer de profundidad como un miembro del tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) . Establezca este estado en D3DZB \_ true para habilitar el almacenamiento en búfer z, D3DZB \_ USEW para habilitar el almacenamiento en búfer de w o D3DZB \_ false para deshabilitar el almacenamiento en búfer de profundidad.

El valor predeterminado para este estado de representación es D3DZB \_ true si se ha creado una galería de símbolos de profundidad junto con la cadena de intercambio estableciendo el miembro EnableAutoDepthStencil de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) en **true** y D3DZB \_ false en caso contrario.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

Uno o más miembros del tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) . El valor predeterminado es D3DFILL \_ Solid.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Uno o más miembros del tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) . El valor predeterminado es D3DSHADE \_ GOURAUD.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**True** para permitir que la aplicación escriba en el búfer de profundidad. El valor predeterminado es **true**. Este miembro permite a una aplicación impedir que el sistema actualice el búfer de profundidad con nuevos valores de profundidad. Si es **false**, las comparaciones de profundidad se siguen realizando según el estado de representación D3DRS \_ ZFUNC, suponiendo que se está llevando a cabo el almacenamiento en búfer de profundidad, pero los valores de profundidad no se escriben en el búfer.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**True** para habilitar las pruebas alfa por píxel. Si se supera la prueba, el búfer de fotogramas procesa el píxel. De lo contrario, se omite todo el procesamiento del búfer de fotogramas para el píxel.

La prueba se realiza comparando el valor alfa entrante con el valor alfa de referencia, usando la función de comparación proporcionada por el estado de representación de D3DRS \_ ALPHAFUNC. El valor alfa de referencia viene determinado por el valor establecido para D3DRS \_ ALPHAREF. Para obtener más información, vea estado de la [prueba alfa (Direct3D 9)](alpha-testing-state.md).

El valor predeterminado de este parámetro es **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

El valor predeterminado es **true**, que permite dibujar el último píxel en una línea. Para evitar el dibujo del último píxel, establezca este valor en **false**. Para obtener más información, vea [resumir y rellenar el estado (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) . El valor predeterminado es D3DBLEND \_ uno.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) . El valor predeterminado es D3DBLEND \_ cero.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

Especifica cómo se seleccionan los triángulos de conexión hacia delante, en caso de que se produzcan. Se puede establecer en un miembro del tipo enumerado [**D3DCULL**](./d3dcull.md) . El valor predeterminado es D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**
</dt> <dd>

Un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) . El valor predeterminado es D3DCMP \_ LESSEQUAL. Este miembro permite a una aplicación aceptar o rechazar un píxel, en función de su distancia de la cámara.

El valor de profundidad del píxel se compara con el valor del búfer de profundidad. Si el valor de profundidad del píxel pasa la función de comparación, se escribe el píxel.

El valor de profundidad se escribe en el búfer de profundidad solo si el estado de representación es **true**.

Los rasterizadores de software y muchos aceleradores de hardware funcionan más rápido si se produce un error en la prueba de profundidad, ya que no hay necesidad de filtrar y modular la textura si el píxel no se va a representar.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

Valor que especifica un valor alfa de referencia con el que se prueban los píxeles cuando está habilitada la prueba alfa. Se trata de un valor de 8 bits colocado en los 8 bits inferiores del valor DWORD de representación de estado. Los valores pueden oscilar entre 0x00000000 y 0x000000FF. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

Un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) . El valor predeterminado es D3DCMP \_ siempre. Este miembro permite a una aplicación aceptar o rechazar un píxel, en función de su valor alfa.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**True** para habilitar el tramado. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**True** para habilitar la transparencia combinada alfa. El valor predeterminado es **FALSE**.

El tipo de combinación alfa viene determinado por los Estados de \_ representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**
</dt> <dd>

**True** para habilitar la combinación de niebla. El valor predeterminado es **FALSE**. Para obtener más información sobre el uso de la combinación de niebla, consulte [niebla](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**True** para habilitar los reflejos especulares. El valor predeterminado es **FALSE**.

Los reflejos especulares se calculan como si todos los vértices del objeto que se iluminan se encuentran en el origen del objeto. Esto proporciona los resultados esperados siempre que el objeto se modela en torno al origen y la distancia desde la luz al objeto es relativamente grande. En otros casos, los resultados son indefinidos.

Cuando este miembro está establecido en **true**, el color especular se agrega al color base después de la textura Cascade, pero antes de la combinación alfa.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**
</dt> <dd>

Valor cuyo tipo es [**D3DCOLOR**](d3dcolor.md). El valor predeterminado es 0. Para obtener más información sobre el color de la niebla, vea [niebla color (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**
</dt> <dd>

La fórmula de niebla que se va a utilizar para la niebla de píxeles. Establezca en uno de los miembros del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . El valor predeterminado es D3DFOG \_ None. Para obtener más información sobre la niebla de píxeles, vea [niebla de píxeles (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**
</dt> <dd>

Profundidad a la que se inician los efectos de niebla de píxeles o vértices para el modo de niebla lineal. El valor predeterminado es 0.0 f. La profundidad se especifica en el espacio universal para la niebla de vértices y el espacio \[ de dispositivo 0,0, 1,0 \] o el espacio universal para la niebla de píxeles. En el caso de la niebla de píxeles, estos valores se encuentran en el espacio de dispositivo cuando el sistema utiliza z para los cálculos de niebla y el espacio mundial cuando el sistema utiliza la niebla relativa a la vista (niebla). Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md) y [profundidad en relación con la profundidad basada en Z](pixel-fog.md).

Los valores de este estado de representación son valores de punto flotante. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**
</dt> <dd>

Profundidad en la que los efectos de niebla de píxeles o vértices terminan en el modo de niebla lineal. El valor predeterminado es 1.0 f. La profundidad se especifica en el espacio universal para la niebla de vértices y el espacio \[ de dispositivo 0,0, 1,0 \] o el espacio universal para la niebla de píxeles. En el caso de la niebla de píxeles, estos valores se encuentran en el espacio de dispositivo cuando el sistema utiliza z para los cálculos de niebla y en el espacio universal cuando el sistema utiliza niebla relativa a la vista (niebla). Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md) y [profundidad en relación con la profundidad basada en Z](pixel-fog.md).

Los valores de este estado de representación son valores de punto flotante. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**
</dt> <dd>

Densidad de niebla para la niebla de píxeles o vértices usada en los modos de niebla exponencial (D3DFOG \_ EXP y D3DFOG \_ EXP2). Los valores de densidad válidos van de 0,0 a 1,0. El valor predeterminado es 1,0. Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).

Los valores de este estado de representación son valores de punto flotante. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**True** para habilitar la niebla de vértices basada en intervalo. El valor predeterminado es **false**, en cuyo caso el sistema utiliza la niebla basada en la profundidad. En la niebla basada en intervalo, la distancia de un objeto desde el visor se usa para calcular los efectos de niebla, no la profundidad del objeto (es decir, la coordenada z) de la escena. En la niebla basada en intervalo, todos los métodos de niebla funcionan como de costumbre, salvo que usan el intervalo en lugar de la profundidad en los cálculos.

El intervalo es el factor correcto que se debe usar para los cálculos de niebla, pero la profundidad se usa normalmente en su lugar porque el intervalo lleva mucho tiempo en proceso y la profundidad ya está disponible. El uso de Depth para calcular la niebla tiene el efecto no deseado de que la luneta térmica de los objetos periféricos cambie a medida que se mueve el ojo del visor; en este caso, la profundidad cambia y el intervalo permanece constante.

Dado que ningún hardware admite actualmente la niebla basada en intervalos por píxel, la corrección del intervalo solo se ofrece para la niebla de vértice.

Para obtener más información, vea [niebla de vértices (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**True** para habilitar el estarcido o **false** para deshabilitar el estarcido. El valor predeterminado es **FALSE**. Para obtener más información, vea [técnicas de búfer de estarcido (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

Operación de estarcido que se va a realizar si se produce un error en la prueba de estarcido. Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Operación de estarcido que se va a realizar si se supera la prueba de estarcido y se produce un error en la prueba de profundidad (prueba z). Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Operación de estarcido que se va a realizar si se superan las pruebas de la galería de símbolos y la profundidad (z). Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Función de comparación para la prueba de estarcido. Los valores son del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) . El valor predeterminado es D3DCMP \_ siempre.

La función de comparación se usa para comparar el valor de referencia con una entrada de búfer de estarcido. Esta comparación se aplica solo a los bits del valor de referencia y la entrada del búfer de estarcido que se establecen en la máscara de la galería de símbolos (establecida por el estado de representación de D3DRS \_ STENCILMASK). Si **es true**, la prueba de estarcido se supera.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Valor de referencia int para la prueba de estarcido. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Máscara aplicada al valor de referencia y a cada entrada de búfer de estarcido para determinar los bits significativos para la prueba de estarcido. La máscara predeterminada es 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

Máscara de escritura aplicada a los valores escritos en el búfer de estarcido. La máscara predeterminada es 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

Color que se usa para la combinación de varias texturas con el \_ argumento D3DTA TFACTOR Texture-blending o la \_ operación D3DTOP BLENDFACTORALPHA Texture-blending. El valor asociado es una variable [**D3DCOLOR**](d3dcolor.md) . El valor predeterminado es blanco opaco (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Comportamiento de ajuste de textura para varios conjuntos de coordenadas de textura. Los valores válidos para este estado de representación pueden ser cualquier combinación de las \_ marcas D3DWRAPCOORD 0 (o D3DWRAP \_ u), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP \_ W) y D3DWRAPCOORD \_ 3. Esto hace que el sistema se ajuste en la dirección de las dimensiones primera, segunda, tercera y cuarta, que a veces se denominan direcciones s, t, r y q, para una textura determinada. El valor predeterminado para este estado de representación es 0 (ajuste deshabilitado en todas las direcciones).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**Recorte de D3DRS \_**
</dt> <dd>

**True** para habilitar el recorte primitivo por Direct3D o **false** para deshabilitarlo. El valor predeterminado es **true**.

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Iluminación D3DRS**
</dt> <dd>

**True** para habilitar la iluminación de Direct3D o **false** para deshabilitarlo. El valor predeterminado es **true**. Solo los vértices que incluyen el vértice normal están correctamente iluminados; los vértices que no contienen una normal emplean un producto de punto de 0 en todos los cálculos de iluminación.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**\_Ambiente D3DRS**
</dt> <dd>

Color claro ambiente. Este valor es de tipo [**D3DCOLOR**](d3dcolor.md). El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**
</dt> <dd>

Fórmula de niebla que se va a usar para la niebla de vértice. Se establece en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . El valor predeterminado es D3DFOG \_ None.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**True** para habilitar el color por vértice o **false** para deshabilitarlo. El valor predeterminado es **true**. La habilitación del color por vértice permite que el sistema incluya el color definido para los vértices individuales en los cálculos de iluminación.

Para obtener más información, vea los siguientes Estados de representación:

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**True** para habilitar los reflejos especulares relativos a la cámara, o **false** para usar los reflejos especulares ortogonales. El valor predeterminado es **true**. Las aplicaciones que usan la proyección ortogonal deben especificar **false**.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**True** para habilitar la normalización automática de las normales de vértice o **false** para deshabilitarla. El valor predeterminado es **FALSE**. Al habilitar esta característica, el sistema normaliza las normales de vértice para los vértices después de transformarlos en el espacio de la cámara, lo que puede consumir mucho tiempo.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

Origen de color difuso para los cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . El valor predeterminado es D3DMCS \_ COLOR1. El valor de este estado de representación se usa solo si el \_ Estado de representación de D3DRS COLORVERTEX está establecido en **true**.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Origen de color especular para los cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . El valor predeterminado es D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Origen de color ambiente para los cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . El valor predeterminado es \_ material D3DMCS.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Origen de color emisor para los cálculos de iluminación. Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . El valor predeterminado es \_ material D3DMCS.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

Número de matrices que se van a usar para realizar la combinación de geometría, si existe. Los valores válidos son miembros del tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . El valor predeterminado es D3DVBF \_ Disable.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

Habilita o deshabilita los planos de recorte definidos por el usuario. Los valores válidos son cualquier valor DWORD en el que el estado de cada bit (establecido o no establecido) alterna el estado de activación de un plano de recorte definido por el usuario correspondiente. El bit menos significativo (bit 0) controla el primer plano de recorte en el índice 0 y los bits subsiguientes controlan la activación de los planos de recorte en los índices más altos. Si se establece un bit, el sistema aplica el plano de recorte adecuado durante la representación de la escena. El valor predeterminado es 0.

Las macros [**D3DCLIPPLANEn**](d3dclipplanen.md) se definen para proporcionar una manera cómoda de habilitar los planos de recorte.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ puntuación**
</dt> <dd>

Valor flotante que especifica el tamaño que se va a usar para el cálculo del tamaño de punto en los casos en los que no se especifica el tamaño de punto para cada vértice. Este valor no se usa cuando el vértice contiene un tamaño de punto. Este valor se encuentra en unidades de espacio de pantalla si D3DRS \_ POINTSCALEENABLE es **false**; de lo contrario, este valor está en unidades de espacio universal. El valor predeterminado es el valor que devuelve un controlador. Si un controlador devuelve 0 o 1, el valor predeterminado es 64, que permite la emulación de tamaño de punto de software. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS de \_ puntuación \_ mín.**
</dt> <dd>

Valor flotante que especifica el tamaño mínimo de primitivas de punto. Los primitivos de punto se fijan a este tamaño durante la representación. Si se establece en valores inferiores a 1,0, los puntos se descartan cuando el punto no cubre un centro de píxeles y el suavizado de contorno está deshabilitado o se representa con menor intensidad cuando se habilita el suavizado de contorno. El valor predeterminado es 1.0 f. El intervalo para este valor es mayor o igual que 0,0 f. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**
</dt> <dd>

valor booleano. Cuando **es true**, las coordenadas de textura de los primitivos de punto se establecen para que las texturas completas se asignen en cada punto. Cuando **es false**, las coordenadas de textura de los vértices se utilizan para todo el punto. El valor predeterminado es **FALSE**. Puede obtener los puntos de un solo píxel con estilo de DirectX 7 Si establece D3DRS \_ POINTSCALEENABLE en **false** y D3DRS \_ en 1,0, que son los valores predeterminados.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

valor booleano que controla el cálculo del tamaño de los primitivos de punto. Si es **true**, el tamaño del punto se interpreta como un valor de espacio de la cámara y se escala mediante la función Distance y el frustum para viewport de la escala del eje y para calcular el tamaño final del punto de espacio de la pantalla. Cuando es **false**, el tamaño del punto se interpreta como espacio de la pantalla y se usa directamente. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_**
</dt> <dd>

Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto. Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**. El valor predeterminado es 1.0 f. El intervalo para este valor es mayor o igual que 0,0 f. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto. Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**. El valor predeterminado es 0.0 f. El intervalo para este valor es mayor o igual que 0,0 f. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto. Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**. El valor predeterminado es 0.0 f. El intervalo para este valor es mayor o igual que 0,0 f. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

valor booleano que determina cómo se calculan los ejemplos individuales cuando se usa un búfer de representación y destino de ejemplo múltiple. Cuando se establece en **true**, se calculan varios ejemplos para que el suavizado de contorno completo de la escena se realice mediante el muestreo en posiciones de ejemplo diferentes para cada ejemplo múltiple. Cuando se establece en **false**, todos los ejemplos se escriben con el mismo valor de ejemplo, muestreado en el centro de píxeles, lo que permite la representación sin suavizado de contorno en un búfer de muestreo múltiple. Este estado de representación no tiene ningún efecto cuando se representa en un búfer de ejemplo único. El valor predeterminado es **true**.

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Cada bit de esta máscara, que comienza en el bit menos significativo (LSB), controla la modificación de uno de los ejemplos en un destino de representación Multimuestra. Por lo tanto, para un destino de representación de 8 muestras, el byte bajo contiene las ocho escrituras habilitadas para cada una de las ocho muestras. Este estado de representación no tiene ningún efecto cuando se representa en un búfer de ejemplo único. El valor predeterminado es 0xFFFFFFFF.

Este estado de representación permite el uso de un búfer de ejemplo múltiples como búfer de acumulación, con una representación de la geometría en la que cada paso actualiza un subconjunto de muestras.

Si hay n muestras de varios ejemplos y de k habilitadas, la intensidad resultante de la imagen representada debe ser k/n. Cada componente RGB de cada píxel se factoriza por k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Establece si los bordes de la revisión utilizarán la teselación de estilo flotante. Los valores posibles se definen mediante el tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) . El valor predeterminado es D3DPATCHEDGE \_ discreto.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Solo se establece para depurar el monitor. Los valores posibles se definen mediante el tipo enumerado [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) . Tenga en cuenta que si \_ se establece D3DRS DEBUGMONITORTOKEN, la llamada se trata como si pasara un token al monitor de depuración. Por ejemplo, si-después de pasar D3DDMT \_ enable o D3DDMT \_ Disable a D3DRS \_ DEBUGMONITORTOKEN-se pasan otros valores de token, el estado (habilitado o deshabilitado) del monitor de depuración seguirá siendo persistente.

Este estado solo es útil para las compilaciones de depuración. El monitor de depuración tiene como valor predeterminado D3DDMT \_ enable.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ \_ Max**
</dt> <dd>

Valor flotante que especifica el tamaño máximo al que se van a fijar los sprites de punto. El valor debe ser menor o igual que el miembro MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) y mayor o igual que D3DRS separar \_ \_ min. El valor predeterminado es 64,0. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

valor booleano que habilita o deshabilita la combinación de vértices indizados. El valor predeterminado es **FALSE**. Cuando se establece en **true**, se habilita la combinación de vértices indizada. Cuando se establece en **false**, se deshabilita la mezcla de vértices indizados. Si este estado de representación está habilitado, el usuario debe pasar los índices de matriz como un DWORDwith empaquetado cada vértice. Cuando el estado de representación es deshabilitado y la combinación de vértices se habilita a través del \_ Estado D3DRS VERTEXBLEND, equivale a tener índices de matriz 0, 1, 2, 3 en cada vértice.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

Valor UINT que habilita una escritura por canal para el búfer de color de destino de representación. Un bit establecido hace que el canal de color se actualice durante la representación 3D. Un bit claro da lugar a que el canal de color no se vea afectado. Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ COLORWRITEENABLE se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo. Este estado de representación no afecta a la operación de borrado. El valor predeterminado es 0x0000000F.

Los valores válidos para este estado de representación pueden ser cualquier combinación de las \_ marcas D3DCOLORWRITEENABLE alfa, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ Green o D3DCOLORWRITEENABLE \_ roja.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Un valor de tipo float que controla el factor de intercalación. El valor predeterminado es 0.0 f. Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

Valor que se usa para seleccionar la operación aritmética aplicada cuando el estado de representación de la mezcla alfa, D3DRS \_ ALPHABLENDENABLE, se establece en **true**. Los valores válidos se definen mediante el tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) . El valor predeterminado es D3DBLENDOP \_ Add.

Si \_ no se admite la funcionalidad del dispositivo D3DPMISCCAPS BLENDOP, \_ se realiza D3DBLENDOP agregar.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

N: grado de interpolación de la posición de la revisión. Los valores pueden ser D3DDEGREE \_ cúbicos (valor predeterminado) o D3DDEGREE \_ linear. Para obtener más información, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

N: revisión del grado de interpolación normal. Los valores pueden ser D3DDEGREE \_ linear (default) o D3DDEGREE \_ cuadrático. Para obtener más información, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**True** para habilitar la prueba de tijera y **false** para deshabilitarla. El valor predeterminado es **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**
</dt> <dd>

Se usa para determinar la cantidad de sesgo que se puede aplicar a las primitivas coplanas para reducir la lucha de la z. El valor predeterminado es 0.

Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

donde Max es la pendiente de profundidad máxima del triángulo que se va a representar.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**True** para habilitar el suavizado de contorno de línea, **false** para deshabilitar el suavizado de línea. El valor predeterminado es **FALSE**.

Al representar un destino de representación Multimuestra, D3DRS \_ ANTIALIASEDLINEENABLE se omite y se representan los alias de todas las líneas. Use [**ID3DXLine**](id3dxline.md) para la representación de líneas alisadas en un destino de representación Multimuestra.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Nivel de teselación mínimo. El valor predeterminado es 1.0 f. Vea [teselación (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Nivel máximo de teselación. El valor predeterminado es 1.0 f. Vea [teselación (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Cantidad para dividirlas adaptable, en la dirección x. El valor predeterminado es 0.0 f. Vea [teselación adaptable](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Importe para dividirlas de modo adaptable, en la dirección y. El valor predeterminado es 0.0 f. Vea [ \_ teselación adaptable](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Importe para dividirlas adaptable, en la dirección z. El valor predeterminado es 1.0 f. Vea [ \_ teselación adaptable](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Cantidad para dividirlas adaptable, en la dirección w. El valor predeterminado es 0.0 f. Vea [ \_ teselación adaptable](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**True** para habilitar la teselación adaptable y **false** para deshabilitarla. El valor predeterminado es **FALSE**. Vea [ \_ teselación adaptable](tessellation.md).

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**True** habilita el estarcido de dos caras, **false** lo deshabilita. El valor predeterminado es **FALSE**. La aplicación debe establecer D3DRS \_ CULLMODE en D3DCULL \_ None para habilitar el modo de galería de símbolos de dos caras. Si el orden de la espiral del triángulo es el de las agujas del reloj, se \_ usarán las operaciones de la galería de símbolos D3DRS \* . Si el orden de bobinado es en sentido contrario a las agujas del reloj, se \_ usarán las operaciones de estarcido de D3DRS CCW \_ \* .

Para ver si se admite la galería de símbolos de dos caras, compruebe el miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED. Vea también [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

Operación de estarcido que se debe realizar si se produce un error en la prueba de estarcido CCW. Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Operación de estarcido que se va a realizar si se supera la prueba de estarcido CCW y la prueba z. Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Operación de estarcido que se realizará si se superan las pruebas de la galería de símbolos CCW y z. Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) . El valor predeterminado es D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Función de comparación. La prueba de estarcido CCW se supera si la función de estarcido (((Ref & Mask) (Galería de símbolos & máscara)) es **true**. Los valores son del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) . El valor predeterminado es D3DCMP \_ siempre.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Valores de ColorWriteEnable adicionales para los dispositivos. Vea D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Valores de ColorWriteEnable adicionales para los dispositivos. Vea D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Valores de ColorWriteEnable adicionales para los dispositivos. Vea D3DRS \_ COLORWRITEENABLE. Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo. El valor predeterminado es 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) usado para un factor de mezcla constante durante la combinación alfa. Esta funcionalidad está disponible si el bit de funcionalidad de D3DPBLENDCAPS \_ BLENDFACTOR se establece en el miembro SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o en el miembro DestBlendCaps de **D3DCAPS9**. Vea [**D3DRENDERSTATETYPE**](). El valor predeterminado es 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Habilite la escritura de representación-destino para que sea gamma corregida a sRGB. El formato debe exponer D3DUSAGE \_ SRGBWRITE. El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Un valor de punto flotante que se usa para la comparación de valores de profundidad. Vea [sesgo de profundidad (Direct3D 9)](depth-bias.md). El valor predeterminado es 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Vea D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**True** habilita el modo de mezcla independiente para el canal alfa. El valor predeterminado es **FALSE**.

Cuando se establece en **false**, los factores de mezcla y las operaciones de destino de representación que se aplican a alfa se fuerzan a ser iguales que los definidos para el color. Este modo está realmente cableado a **false** en las implementaciones que no establecen el Cap D3DPMISCCAPS \_ SEPARATEALPHABLEND. Vea [D3DPMISCCAPS](d3dpmisccaps.md).

El tipo de combinación alfa independiente viene determinado por los Estados de \_ representación D3DRS SRCBLENDALPHA y D3DRS \_ DESTBLENDALPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) . Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **true**. El valor predeterminado es D3DBLEND \_ uno.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) . Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **true**. El valor predeterminado es D3DBLEND \_ cero.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Valor que se usa para seleccionar la operación aritmética que se aplica a la combinación alfa independiente cuando el estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE, se establece en **true**.

Los valores válidos se definen mediante el tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) . El valor predeterminado es D3DBLENDOP \_ Add.

Si \_ no se admite la funcionalidad del dispositivo D3DPMISCCAPS BLENDOP, \_ se realiza D3DBLENDOP agregar. Vea [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones



| Estados de representación        |                    |
|----------------------|--------------------|
| PS \_ 1 \_ 1 a PS \_ 1 \_ 3 | 4 muestras de texturas |



 

Direct3D define la \_ constante D3DRENDERSTATE WRAPBIAS para que las aplicaciones puedan habilitar o deshabilitar el ajuste de textura, en función del entero de base cero de un conjunto de coordenadas de textura (en lugar de usar explícitamente uno de los valores de estado de ajuste de D3DRS \_ n). Agregue el \_ valor de WRAPBIAS D3DRENDERSTATE al índice de base cero de un conjunto de coordenadas de textura para calcular el valor del ajuste de D3DRS \_ n que corresponde a ese índice, como se muestra en el ejemplo siguiente.


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
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 

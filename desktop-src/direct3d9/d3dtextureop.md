---
description: Define las operaciones de combinación de texturas por fase.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumeración D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362502"
---
# <a name="d3dtextureop-enumeration"></a>Enumeración D3DTEXTUREOP

Define las operaciones de combinación de texturas por fase.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**Deshabilitación de D3DTOP \_**
</dt> <dd>

Deshabilita la salida de esta fase de textura y todas las fases con un índice superior. Para deshabilitar la asignación de texturas, establezca este valor como la operación de color para la primera fase de textura (fase 0). Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color. La configuración de la operación Alpha en D3DTOP \_ se deshabilita cuando la combinación de colores está habilitada provoca un comportamiento indefinido.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Use el primer argumento de color o alfa de esta fase de textura, sin modificar, como salida. Esta operación afecta al argumento de color cuando se usa con el \_ Estado D3DTSS COLOROP Texture-Stage y el argumento alfa cuando se usa con D3DTSS \_ ALPHAOP.

![ecuación de este argumento (1) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Use el segundo argumento de color o alfa de esta fase de textura, sin modificar, como salida. Esta operación afecta al argumento de color cuando se usa con el estado de fase de textura de D3DTSS \_ COLOROP y el argumento alfa cuando se usa con D3DTSS \_ ALPHAOP.

![ecuación de este argumento (1) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ modular**
</dt> <dd>

Multiplique los componentes de los argumentos.

![ecuación de las operaciones modulares (RGBA) = arg1 x Arg 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

Multiplique los componentes de los argumentos y desplace los productos a la izquierda de 1 bit (de forma eficaz, multiplíquelo por 2) para aclararlos.

![ecuación de las operaciones modulate2x (RGBA) = (arg1 x Arg 2) then Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

Multiplique los componentes de los argumentos y desplace los productos a los 2 bits de la izquierda (de forma eficaz, multiplíquelo por 4) para aclararlos.

![ecuación de las operaciones modulate4x (RGBA) = (arg1 x Arg 2) then Shift Left 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Agregar**
</dt> <dd>

Agregue los componentes de los argumentos.

![ecuación de las operaciones de adición (RGBA) = arg1 + Arg 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**
</dt> <dd>

Agregue los componentes de los argumentos con una diferencia de-0,5, lo que convierte el intervalo efectivo de valores entre-0,5 y 0,5.

![ecuación de la operación agregar firma (es decir, RGBA) = arg1 + Arg 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Agregue los componentes de los argumentos con una diferencia de-0,5 y desplace los productos a la izquierda 1 bit.

![ecuación de la operación agregar 2x con signo ((s (RGBA) = arg1 + Arg 2-0,5) then Shift Left 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**Resta de D3DTOP \_**
</dt> <dd>

Reste los componentes del segundo argumento de los del primer argumento.

![ecuación de la operación de resta (s (RGBA) = arg1-Arg 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**
</dt> <dd>

Agregue el primer y el segundo argumento; a continuación, reste su producto a la suma.

![ecuación de la operación agregar Smooth (es decir, RGBA) = arg1 + Arg 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**
</dt> <dd>

Mezcle linealmente esta fase de textura con el alfa interpolado de cada vértice.

![ecuación de las operaciones alfa difusas de Blend (RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**
</dt> <dd>

Mezcle linealmente esta fase de textura con el alfa de la textura de esta fase.

![ecuación de la operación alfa de textura de mezcla (es decir, RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**
</dt> <dd>

Mezcle linealmente esta fase de textura mediante un conjunto de alfa escalar con el estado de representación de TEXTUREFACTOR de D3DRS \_ .

![ecuación de la operación alfa del factor de mezcla ((RGBA) = arg1 x alfa + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**
</dt> <dd>

Mezcle linealmente una fase de textura que utiliza un alfa premultiplicado.

![ecuación de la operación de mezcla Alpha PM Operation (s (RGBA) = arg1 + Arg 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**
</dt> <dd>

Mezcle linealmente esta fase de textura con el alfa tomado de la fase de textura anterior.

![ecuación de la operación alfa actual de Blend (es decir, RGBA) = arg1 x alfa + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREmodulado**
</dt> <dd>

D3DTOP \_ PREmodulado está establecido en la fase n. La salida de la fase n es arg1. Además, si hay una textura en la fase n + 1, cualquier D3DTA \_ actual de la fase n + 1 se multiplica por la textura en la fase n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**
</dt> <dd>

Modula el color del segundo argumento, utilizando el alfa del primer argumento; a continuación, agregue el resultado al argumento uno. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

![ecuación de las operaciones alfa de la modular de colores de agregar (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**
</dt> <dd>

Modula los argumentos; a continuación, agregue el alfa del primer argumento. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

![ecuación de la operación de adición de color alfa modular (es decir, RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**
</dt> <dd>

Similar a D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, pero use el inverso del alfa del primer argumento. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

![ecuación de la operación de alfa inversa del modulador de color (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**
</dt> <dd>

Similar a D3DTOP \_ MODULATECOLOR \_ ADDALPHA, pero usa el inverso del color del primer argumento. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

![ecuación de la operación agregar color inverso alfa modular (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**
</dt> <dd>

Realice la asignación de rugosidad por píxel mediante el mapa de entorno en la siguiente fase de textura, sin luminancia. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**
</dt> <dd>

Realice la asignación de rugosidad por píxel mediante el mapa de entorno en la siguiente fase de textura, con luminancia. Esta operación solo se admite para operaciones de color (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Modula los componentes de cada argumento como componentes firmados, agrega sus productos; a continuación, replique la suma en todos los canales de color, incluido alfa. Esta operación se admite para las operaciones de color y alfa.

![ecuación de las operaciones de producto de punto 3 (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

En DirectX 6 y DirectX 7, las operaciones de múltiples texturas las entradas anteriores se desplazan hacia abajo a la mitad (y = x-0,5) antes de usarlas para simular los datos firmados, y el resultado escalar se fija automáticamente en valores positivos y se replica en los tres canales de salida. Además, tenga en cuenta que, como operación de color, no se actualiza el Alpha; simplemente, se actualizan los componentes RGB.

Sin embargo, en los sombreadores de DirectX 8,1 puede especificar que la salida se enrute a los componentes. RGB o. a, o a ambos (el valor predeterminado). También puede especificar una operación escalar independiente en el canal alfa.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**
</dt> <dd>

Realiza una operación de multiplicación acumulada. Toma los dos últimos argumentos, los multiplica juntos y los agrega al argumento de entrada/origen restante y lo coloca en el resultado.

S<sub>RGBA</sub> = arg1 + arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ lerp**
</dt> <dd>

Interpola linealmente entre el segundo y tercer argumento de origen mediante una proporción especificada en el primer argumento de origen.

S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* Arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los miembros de este tipo se usan al establecer operaciones de color o alfa mediante los valores de D3DTSS \_ COLOROP o D3DTSS \_ ALPHAOP con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .

En las fórmulas anteriores, S<sub>RGBA</sub> es el color RGBA generado por una operación de textura, y arg1, arg2 y Arg3 representan el color RGBA completo de los argumentos de textura. Los componentes individuales de un argumento se muestran con subíndices. Por ejemplo, el componente alfa para el argumento 1 se mostraría como arg1<sub>A</sub>.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 

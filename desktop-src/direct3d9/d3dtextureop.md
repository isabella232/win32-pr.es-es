---
description: Define las operaciones de mezcla de texturas por fase.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumeración D3DTEXTUREOP (D3D9Types.h)
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
ms.openlocfilehash: c8d3108c59ddf810a815cbfa5f05a6fe66704325ffcee3f5dc2436b83c2c605d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987415"
---
# <a name="d3dtextureop-enumeration"></a>D3DTEXTUREOP (enumeración)

Define las operaciones de mezcla de texturas por fase.

## <a name="syntax"></a>Syntax


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

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ DISABLE**
</dt> <dd>

Deshabilita la salida de esta fase de textura y todas las fases con un índice superior. Para deshabilitar la asignación de textura, establezca esta opción como la operación de color para la primera fase de textura (fase 0). Las operaciones alfa no se pueden deshabilitar cuando se habilitan las operaciones de color. Establecer la operación alfa en D3DTOP DISABLE cuando la combinación de colores está habilitada \_ provoca un comportamiento indefinido.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Use el primer argumento alfa o color de esta fase de textura, sin modificar, como salida. Esta operación afecta al argumento de color cuando se usa con el estado de fase de textura COLOROP de D3DTSS y el argumento alfa cuando se usa con \_ D3DTSS \_ ALPHAOP.

![ecuación de este argumento (s(rgba) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Use el segundo color o argumento alfa de esta fase de textura, sin modificar, como salida. Esta operación afecta al argumento de color cuando se usa con el estado de fase de textura COLOROP de D3DTSS y al argumento alfa cuando se usa con \_ D3DTSS \_ ALPHAOP.

![ecuación de este argumento (s(rgba) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ MODULARTE**
</dt> <dd>

Multiplique los componentes de los argumentos.

![ecuación de la operación de modular (s(rgba) = arg1 x arg 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**\_D3DTOPMODULTE2X**
</dt> <dd>

Multiplique los componentes de los argumentos y cambie los productos a la izquierda de 1 bit (multiplicándolos eficazmente por 2) para el brillo.

![ecuación de la operación de modularte2x (s(rgba) = (arg1 x arg 2) y desplazamiento a la izquierda 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**\_D3DTOPMODULTE4X**
</dt> <dd>

Multiplique los componentes de los argumentos y cambie los productos a los 2 bits izquierdos (multiplicándolos eficazmente por 4) para el brillo.

![ecuación de la operación de modularte4x (s(rgba) = (arg1 x arg 2) y desplazamiento a la izquierda 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ ADD**
</dt> <dd>

Agregue los componentes de los argumentos.

![ecuación de la operación de adición (s(rgba) = arg1 + arg 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**
</dt> <dd>

Agregue los componentes de los argumentos con un sesgo de - 0,5, lo que hace que el intervalo efectivo de valores de - 0,5 a 0,5.

![ecuación de la operación add signed (s(rgba) = arg1 + arg 2 – 0.5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Agregue los componentes de los argumentos con un sesgo de - 0,5 y cambie los productos a la izquierda de 1 bit.

![ecuación de la operación add signed 2x ((s(rgba) = arg1 + arg 2 - 0.5) y, a continuación, desplazar a la izquierda 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ SUBTRACT**
</dt> <dd>

Resta los componentes del segundo argumento de los del primer argumento.

![ecuación de la operación de resta (s(rgba) = arg1 - arg 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**
</dt> <dd>

Agregue los argumentos primero y segundo; a continuación, resta su producto de la suma.

![ecuación de la operación de adición de suavizado (s(rgba) = arg1 + arg 2 x (1 - arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**
</dt> <dd>

Combine linealmente esta fase de textura mediante el alfa interpolado de cada vértice.

![ecuación de la operación alfa difusa de mezcla (s(rgba) = arg1 x alpha + arg 2 x (1 - alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**
</dt> <dd>

Combine linealmente esta fase de textura mediante el alfa de la textura de esta fase.

![ecuación de la operación alfa de textura de mezcla (s(rgba) = arg1 x alpha + arg 2 x (1 - alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**
</dt> <dd>

Combine linealmente esta fase de textura mediante un conjunto alfa escalar con el estado de representación \_ TEXTUREFACTOR de D3DRS.

![ecuación de la operación alfa del factor de mezcla (s(rgba) = arg1 x alpha + arg 2 x (1 - alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**
</dt> <dd>

Mezcla lineal de una fase de textura que usa un alfa premultiplicado.

![ecuación de la operación blend texture alpha pm (s(rgba) = arg1 + arg 2 x (1 - alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**
</dt> <dd>

Combine linealmente esta fase de textura con el alfa tomado de la fase de textura anterior.

![ecuación de la operación alfa actual de mezcla (s(rgba) = arg1 x alpha + arg2 x (1 - alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PREMODULATE**
</dt> <dd>

D3DTOP \_ PREMODULATE se establece en la fase n. La salida de la fase n es arg1. Además, si hay una textura en la fase n + 1, cualquier D3DTA CURRENT en la fase n + 1 se multiplica previamente por textura en la fase \_ n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**\_D3DTOPMODULTEALPHA \_ ADDCOLOR**
</dt> <dd>

Modular el color del segundo argumento, usando el alfa del primer argumento; a continuación, agregue el resultado al argumento uno. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

![ecuación de la operación alfa add colormodulte (s(rgba) = arg1(rgb) + arg1(a) x arg2(rgb))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**\_D3DTOPMODULTECOLOR \_ ADDALPHA**
</dt> <dd>

Modular los argumentos; a continuación, agregue el valor alfa del primer argumento. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

![ecuación de la operación de color add alphamodulte (s(rgba) = arg1(rgb) x arg2(rgb) + arg1(a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**\_D3DTOPMODULTEINVALPHA \_ ADDCOLOR**
</dt> <dd>

Es similar a \_ D3DTOPMODULTEALPHA ADDCOLOR, pero usa el inverso del \_ alfa del primer argumento. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

![ecuación de la operación alfa inversa add colormodulte (s(rgba) = (1 - arg1(a)) x arg2(rgb) + arg1(rgb))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**\_D3DTOPMODULTEINVCOLOR \_ ADDALPHA**
</dt> <dd>

Es similar a \_ D3DTOPMODULTECOLOR ADDALPHA, pero usa el inverso del \_ color del primer argumento. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

![ecuación de la operación de color inverso add alphamodulte (s(rgba) = (1 - arg1(rgb)) x arg2(rgb) + arg1(a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**
</dt> <dd>

Realice la asignación de protuberancias por píxel, mediante el mapa de entorno en la siguiente fase de textura, sin luminosidad. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**
</dt> <dd>

Realice la asignación de protuberancias por píxel, mediante el mapa de entorno en la siguiente fase de textura, con luminosidad. Esta operación solo se admite para las operaciones de color (COLOROP de D3DTSS). \_

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Modular los componentes de cada argumento como componentes firmados, agregue sus productos; a continuación, replique la suma en todos los canales de color, incluido alfa. Esta operación se admite para las operaciones de color y alfa.

![ecuación de la operación dot product 3 (s(rgba) = arg1(r) x arg2(r) + arg1(g) x arg2(g) + arg1(b) x arg2(b))](images/topfrm17.png)

En DirectX 6 y DirectX 7, las operaciones de varios texto las entradas anteriores se desplazan a la mitad (y = x - 0,5) antes de usarse para simular datos firmados, y el resultado escalar se fija automáticamente a valores positivos y se replica en los tres canales de salida. Además, tenga en cuenta que, como operación de color, esta operación no actualiza el alfa, sino que solo actualiza los componentes RGB.

Sin embargo, en los sombreadores de DirectX 8.1 puede especificar que la salida se enruta a los componentes .rgb, .a o ambos (valor predeterminado). También puede especificar una operación escalar independiente en el canal alfa.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**
</dt> <dd>

Realiza una operación de multiplicación y acumulación. Toma los dos últimos argumentos, los multiplica y los agrega al argumento input/source restante y los coloca en el resultado.

S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**
</dt> <dd>

Interpola linealmente entre el segundo y el tercer argumento de origen por una proporción especificada en el primer argumento de origen.

S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los miembros de este tipo se usan al establecer operaciones de color o alfa mediante los valores ALPHAOP D3DTSS COLOROP o \_ D3DTSS con el método \_ [**IDirect3DDevice9::SetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)

En las fórmulas anteriores, S RGBA es el color<sub>RGBA</sub> generado por una operación de textura, y Arg1, Arg2 y Arg3 representan el color RGBA completo de los argumentos de textura. Los componentes individuales de un argumento se muestran con subíndices. Por ejemplo, el componente alfa del argumento 1 se mostraría como Arg1<sub>A</sub>.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 

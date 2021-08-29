---
title: texcoord - ps
description: Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 476f618634ee42e1363a091f79c97410b3e3b765138696c5c12e8d3c3fcb5bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043113"
---
# <a name="texcoord---ps"></a>texcoord - ps

Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).

## <a name="syntax"></a>Syntax



| texcoord dst |
|--------------|



 

where

-   dst es el registro de destino.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción interpreta el conjunto de coordenadas de textura (UVW1) correspondiente al número de registro de destino como datos de color (RGBA). Si el conjunto de coordenadas de textura contiene menos de tres componentes, los componentes que faltan se establecen en 0. El cuarto componente siempre se establece en 1. Todos los valores se fijan entre 0 y 1.

La ventaja de texcoord es que proporciona una manera de pasar datos de vértice interpolados con alta precisión directamente al sombreador de píxeles. Sin embargo, cuando los datos se escriben en el registro de destino, se perderá cierta precisión, en función del número de bits usados por el hardware para los registros.

Esta instrucción muestrea ninguna textura. Solo las coordenadas de textura establecidas en esta fase de textura son relevantes.

Cualquier dato de textura (como la posición, la dirección normal y la dirección del origen de luz) se puede asignar mediante un sombreador de vértices a una coordenada de textura. Esto se hace asociando una textura a un registro de textura mediante [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) y especificando cómo se realiza el muestreo de textura mediante [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Si se usa la canalización de función fija, asegúrese de proporcionar la marca \_ TSS TEXCOORDINDEX.

Esta instrucción se usa de la siguiente manera:


```
texcoord tn
```



Un [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contiene cuatro valores de color (RGBA). Los datos también se pueden pensar como datos vectoriales (xyzw). texcoord recuperará tres de estos valores (xyz) del conjunto de coordenadas de textura x y el cuarto componente (w) se establece en 1. La dirección de textura se copia del conjunto de coordenadas de textura n. El resultado se fija entre 0 y 1.

Este ejemplo solo tiene propósitos ilustrativos. El código de C que acompaña al sombreador no se ha optimizado para el rendimiento.

Este es un sombreador de ejemplo que usa texcoord.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



La salida representada del sombreador de píxeles se muestra en la ilustración siguiente. Los valores de coordenadas (u,v,w,1) se asignan a los canales (rgb). El canal alfa se establece en 1. En las esquinas de la ilustración, la coordenada (0,0,0,1) se interpreta como negra; (1,0,0,1) está rojo; (0,1,0,1) es verde; y (1,1,0,1) contienen verde y rojo, lo que genera amarillo.

![ilustración de la salida representada del sombreador de píxeles de ejemplo](images/pstexcoord.jpg)

Se requiere código adicional para usar este sombreador y a continuación se muestra un escenario de ejemplo.


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
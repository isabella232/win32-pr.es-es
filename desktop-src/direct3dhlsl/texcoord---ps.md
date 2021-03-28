---
title: texcoord-PS
description: Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792195"
---
# <a name="texcoord---ps"></a>texcoord-PS

Interpreta los datos de coordenadas de textura (UVW1) como datos de color (RGBA).

## <a name="syntax"></a>Sintaxis



| texcoord DST |
|--------------|



 

, donde

-   DST es el registro de destino.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcoord              | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción interpreta el conjunto de coordenadas de textura (UVW1) correspondiente al número de registro de destino como datos de color (RGBA). Si el conjunto de coordenadas de textura contiene menos de tres componentes, los componentes que faltan se establecen en 0. El cuarto componente siempre se establece en 1. Todos los valores se fijan entre 0 y 1.

La ventaja de texcoord es que proporciona una manera de pasar datos de vértice interpolados a alta precisión directamente en el sombreador de píxeles. Sin embargo, cuando los datos se escriben en el registro de destino, se perderá cierta precisión, dependiendo del número de bits que use el hardware para los registros.

Esta instrucción no muestrea ninguna textura. Solo se aplican las coordenadas de textura establecidas en esta fase de textura.

Los datos de textura (como la posición, la normal y la dirección de origen de la luz) pueden ser asignados por un sombreador de vértices en una coordenada de textura. Esto se hace asociando una textura con un registro de textura mediante [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) y especificando cómo se realiza el muestreo de textura con [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Si se usa la canalización de función fija, asegúrese de proporcionar la \_ marca TSS TEXCOORDINDEX.

Esta instrucción se utiliza como sigue:


```
texcoord tn
```



Un [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) contiene cuatro valores de color (RGBA). Los datos también se pueden considerar como datos vectoriales (xyzw). texcoord recuperará tres de estos valores (XYZ) del conjunto de coordenadas de textura x y el cuarto componente (w) se establece en 1. La dirección de la textura se copia desde el conjunto de coordenadas de textura n. El resultado se fija entre 0 y 1.

Este ejemplo solo tiene propósitos ilustrativos. El código de C que acompaña al sombreador no se ha optimizado para el rendimiento.

A continuación se muestra un sombreador de ejemplo que usa texcoord.


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



En la ilustración siguiente se muestra la salida representada del sombreador de píxeles. Los valores de coordenadas (u, v, w, 1) se asignan a los canales (RGB). El canal alfa está establecido en 1. En las esquinas de la ilustración, la coordenada (0, 0, 0, 1) se interpreta como negro; (1, 0, 0, 1) es rojo; (0, 1, 0, 1) es verde; y (1, 1, 0, 1) contiene verde y rojo, lo que produce amarillo.

![Ilustración de la salida representada del sombreador de píxeles de ejemplo](images/pstexcoord.jpg)

Se requiere código adicional para usar este sombreador y se muestra un escenario de ejemplo a continuación.


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

 

 
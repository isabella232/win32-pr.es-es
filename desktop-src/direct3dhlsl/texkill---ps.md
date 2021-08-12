---
title: texkill - ps
description: Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 462549a9caba9b4b49ca5b5ac088e41320b3d6f731a78a0251d5191cc601a2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284033"
---
# <a name="texkill---ps"></a>texkill - ps

Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.

## <a name="syntax"></a>Syntax



| texkill dst |
|-------------|



 

where

-   dst es un registro de destino

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción corresponde a la función de [**recorte**](dx-graphics-hlsl-clip.md) de HLSL.

no muestrea ninguna textura. Funciona en los tres primeros componentes de las coordenadas de textura que ofrece el número de registro de destino. Para ps \_ 1 \_ 4, texkill opera en los datos de los tres primeros componentes del registro de destino.

Puede usar esta instrucción para implementar planos de recorte arbitrarios en el rasterizador.

Al usar sombreadores de vértices, la aplicación es responsable de aplicar la transformación de perspectiva. Esto puede causar problemas para los planos de recorte arbitrarios porque si contiene factores de escala anisomórficos, los planos de recorte también deben transformarse. Por lo tanto, es mejor proporcionar una posición de vértice sin proyecto que se usará en el recortador arbitrario, que es el conjunto de coordenadas de textura identificado por el operador de textura.

Esta instrucción se usa de la siguiente manera:

<dl> texaskill tn  
El enmascaramiento de píxeles se realiza de la siguiente manera:  
if ( los componentes x,y,z de TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )  
cancelar representación de píxeles
</dl>

Para el sombreador de píxeles \_ 1 1, 1 2 y \_ 1 3, texaskill funciona en el conjunto de coordenadas de textura especificado por el número \_ de registro de destino. Sin embargo, en la versión 1 4, texaskill opera en los datos contenidos en el registro de coordenadas de textura (tn) o en el registro temporal (rn) que se ha especificado como \_ destino. [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)

Cuando se habilita el multimuestreo, no se logrará ningún efecto de suavizado de contorno en los bordes del polígono debido a la multimuestreo a lo largo de ningún borde generado por la habilidad. El sombreador de píxeles se ejecuta una vez por píxel.

Este ejemplo solo tiene propósitos ilustrativos.

En este ejemplo se enmascaran los píxeles que tienen coordenadas de textura negativas. Los colores de píxel se interpolan a partir de los colores de vértice proporcionados en los datos del vértice.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Las coordenadas de textura van de -0,5 a 0,5 en u y de 0,0 a 1,0 en v. Esta instrucción hace que los valores u negativos se enmascaran. En la primera ilustración siguiente se muestra el color del vértice aplicado al cuádculo sin la instrucción de habilidad aplicada. En la segunda ilustración siguiente se muestra el resultado de la instrucción texkill. Los colores de píxel de las coordenadas de textura inferiores a 0 (donde x va de -0,5 a 0,0) se enmascaran. El color de fondo (blanco) se usa donde se enmascara el color de píxel.

![ilustración de la salida con el color del vértice aplicado al cuadrándular sin la instrucción de habilidad](images/pstexkill-in.jpg)![ilustración de la salida con la instrucción texaskill aplicada](images/pstexkill-out.jpg)

Los datos de coordenadas de textura se declaran en la declaración de datos de vértice en este ejemplo.


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 





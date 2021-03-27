---
title: texkill-PS
description: Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358465"
---
# <a name="texkill---ps"></a>texkill-PS

Cancela la representación del píxel actual si alguno de los tres primeros componentes (UVW) de las coordenadas de textura es menor que cero.

## <a name="syntax"></a>Sintaxis



| texkill DST |
|-------------|



 

, donde

-   DST es un registro de destino

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Esta instrucción corresponde a la función de [**recorte**](dx-graphics-hlsl-clip.md) de HLSL.

texkill no muestra ninguna textura. Opera en los tres primeros componentes de las coordenadas de textura especificadas por el número de registro de destino. En el caso de PS \_ 1 \_ 4, texkill funciona en los datos de los tres primeros componentes del registro de destino.

Puede usar esta instrucción para implementar planos de clips arbitrarios en el rasterizador.

Al usar sombreadores de vértices, la aplicación es responsable de aplicar la transformación de perspectiva. Esto puede causar problemas en los planos de recorte arbitrarios porque, si contiene factores de escala de anisomorphic, también es necesario transformar los planos de clips. Por lo tanto, es mejor proporcionar una posición de vértice sin proyecto para usarla en el Clipper arbitrario, que es el conjunto de coordenadas de textura identificado por el operador texkill.

Esta instrucción se utiliza como sigue:

<dl> texkill TN  
El enmascaramiento de píxeles se realiza de la siguiente manera:  
if (los componentes x, y, z de TextureCoordinates (Stage n)<sub>UVWQ</sub>< 0)  
cancelar representación de píxeles
</dl>

Para el sombreador de píxeles 1 \_ 1, 1 \_ 2 y 1 \_ 3, texkill funciona en el conjunto de coordenadas de textura proporcionado por el número de registro de destino. En la versión 1 \_ 4, sin embargo, texkill funciona en los datos contenidos en el [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) o en el registro temporal (RN) que se ha especificado como destino.

Cuando se habilita el muestreo múltiple, el efecto de suavizado de contorno que se consigue en los bordes de polígono debido al muestreo múltiple no se logrará en los bordes generados por texkill. El sombreador de píxeles se ejecuta una vez por píxel.

Este ejemplo solo tiene propósitos ilustrativos.

Este ejemplo enmascara los píxeles que tienen coordenadas de textura negativas. Los colores de píxeles se interpolan a partir de los colores de los vértices proporcionados en los datos de vértices.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Las coordenadas de textura van de-0,5 a 0,5 en u y 0,0 a 1,0 en v. Esta instrucción hace que los valores de u negativos queden enmascarados. En la primera ilustración siguiente se muestra el color de vértice aplicado a la cuádruple sin aplicar la instrucción texkill. En la segunda ilustración siguiente se muestra el resultado de la instrucción texkill. Los colores de píxeles de las coordenadas de textura inferiores a 0 (donde x va de-0,5 a 0,0) se enmascaran. El color de fondo (blanco) se usa cuando se enmascara el color de píxel.

![Ilustración de la salida con el color de vértice aplicado a la cuádruple sin la instrucción texkill](images/pstexkill-in.jpg)![Ilustración de la salida con la instrucción texkill aplicada](images/pstexkill-out.jpg)

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

 

 





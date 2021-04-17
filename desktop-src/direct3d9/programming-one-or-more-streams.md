---
description: En esta sección se describen los sombreadores que se pueden usar para el modelo de secuencia programable.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programar una o más secuencias (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714720"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programar una o más secuencias (Direct3D 9)

En esta sección se describen los sombreadores que se pueden usar para el modelo de secuencia programable.

## <a name="using-streams"></a>Usar secuencias

DirectX 8 presentó la noción de una secuencia para enlazar datos a registros de entrada para su uso por parte de los sombreadores. Una secuencia es una matriz uniforme de datos de componentes, donde cada componente consta de uno o varios elementos que representan una sola entidad, como posición, normal, color, etc. Los flujos permiten que los chips gráficos realicen un acceso directo a la memoria desde varios búferes de vértices en paralelo y también proporcionan una asignación más natural de los datos de la aplicación. También habilitan tritexture triviales frente a Multipass. Piense en lo siguiente:

-   Un vértice se compone de n flujos.
-   Un flujo se compone de elementos m.
-   Un elemento es \[ posición, color, normal, coordenada de textura \] .

El método [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) enlaza un búfer de vértice a un flujo de datos de dispositivo, creando una asociación entre los datos de vértice y uno de varios puertos de flujo de datos que alimentan las funciones de procesamiento primitiva. Las referencias reales a los datos de la secuencia no se producen hasta que se llama a un método de dibujo, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

La asignación de los elementos de vértice de entrada a los registros de entrada de vértices para los sombreadores de vértices programables se define en la declaración del sombreador, pero los elementos del vértice de entrada no tienen una semántica específica sobre su uso. La interpretación de los elementos de vértice de entrada se programa mediante las instrucciones del sombreador. La función de sombreador de vértices se define mediante una matriz de instrucciones que se aplican a cada vértice. Los registros de salida de vértices se escriben explícitamente en, mediante instrucciones en la función de sombreador.

En este debate, sin embargo, debe preocuparse de la asignación semántica de elementos a los registros y más preocupado por el motivo del uso de las secuencias y del problema que se resuelve mediante el uso de secuencias. La principal ventaja de las secuencias es que quitan los costos de datos de vértices previamente asociados con la multitexturización. Antes de las secuencias, un usuario tenía que duplicar conjuntos de datos de vértices para controlar el caso de una sola y multitextura sin elementos de datos no usados, o bien transportar elementos de datos que no se utilizarían excepto en el caso de múltiples texturas.

Este es un ejemplo del uso de dos conjuntos de datos de vértices, uno para la textura única y otro para la multitexturización.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



La alternativa era tener un elemento de vértice único que contenía ambos conjuntos de coordenadas de textura.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Con estos datos de vértices, solo una copia de la posición y los datos de color se transfieren en memoria, a costa de llevar ambos conjuntos de coordenadas de textura para la representación, incluso en el caso de una sola textura.

Ahora que la contrapartida es clara, las secuencias proporcionan una solución elegante para este dilema. Este es un conjunto de definiciones de vértices para admitir tres flujos: uno con posición y color, uno con el primer conjunto de coordenadas de textura y otro con el segundo conjunto de coordenadas de textura.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



La declaración de vértice sería la siguiente:


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



Ahora cree el objeto de declaración de vértices y establézcalo como se muestra:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Ejemplos de combinaciones

### <a name="one-stream-diffuse-color"></a>Color difuso de una secuencia

La declaración de vértices y la configuración de secuencia para la representación de color difusa tendrían el siguiente aspecto:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>Dos flujos con color y textura

La declaración de vértices y la configuración de flujo para la representación de textura única tendrían el siguiente aspecto:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>Dos flujos con color y dos texturas

La declaración de vértices y la configuración de flujo para la representación de varias texturas de dos texturas tendrían el siguiente aspecto:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



En cada caso, basta con la invocación de [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Esto muestra la flexibilidad de las secuencias para resolver el problema de la duplicación de datos o la transmisión de datos redundante a través del bus (es decir, de desperdiciar ancho de banda).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 

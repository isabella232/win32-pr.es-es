---
description: Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Códigos FVF de función fija (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705191"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Códigos FVF de función fija (Direct3D 9)

Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos. Normalmente, especifica los datos que va a procesar la canalización de procesamiento de vértices de función fija. Se trata de una declaración de vértice de estilo anterior; para ver el estilo de declaración de vértices actual, vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Las aplicaciones Direct3D pueden definir vértices del modelo de varias maneras diferentes. La compatibilidad con definiciones de vértices flexibles, también conocidas como formatos de vértices flexibles o códigos de formato de vértices flexibles, permite que la aplicación use solo los componentes de vértice que necesita, lo que elimina los componentes que no se usan. Al usar solo los componentes de vértice necesarios, la aplicación puede conservar memoria y minimizar el ancho de banda de procesamiento necesario para representar los modelos. Describe cómo se da formato a los vértices mediante una combinación de códigos [D3DFVF](d3dfvf.md) .

La especificación FVF incluye formatos para el tamaño de punto, especificado por D3DFVF \_ PSIZE. Este tamaño se expresa en unidades de espacio de la cámara para los vértices no transformados y encendidos (TL) y en unidades de espacio de dispositivo para los vértices de TL.

Los métodos de representación de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) proporcionan a las aplicaciones de C++ métodos que aceptan una combinación de estas marcas y las usan para determinar cómo representar primitivas. Básicamente, estas marcas indican al sistema qué componentes de vértices-posición, pesos de fusión de vértices, normal, colores y el número y el formato de las coordenadas de textura (la aplicación usa y, indirectamente, qué partes de la canalización de representación desea que se apliquen a Direct3D). Además, la presencia o ausencia de una marca de formato de vértice determinado se comunica con el sistema en el que los campos de componente de vértice están presentes en la memoria y que se han omitido.

Para determinar las limitaciones de los dispositivos, puede consultar en un dispositivo los valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS y D3DFVFCAPS \_ TEXCOORDCOUNTMASK en el miembro FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

Las coordenadas de textura se pueden declarar en formatos diferentes, lo que permite direccionar las texturas usando tan solo una coordenada o hasta cuatro coordenadas de textura (para las coordenadas de textura proyectadas en 2D). Para obtener más información, vea [formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md). Utilice el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para crear patrones de bits que identifiquen los formatos de coordenadas de textura que usa el formato de vértice.

Ninguna aplicación usará todos los componentes. Los campos de vectores de vértices y homogéneos recíprocos (RHW) son mutuamente excluyentes. Además, la mayoría de las aplicaciones intentan usar los ocho conjuntos de coordenadas de textura, pero Direct3D tiene esta capacidad. Existen varias restricciones en cuanto a las marcas que puede usar con otras marcas. Por ejemplo, no puede usar los \_ marcadores D3DFVF XYZ y D3DFVF \_ XYZRHW juntos, ya que esto indicaría que la aplicación está describiendo la posición de un vértice con vértices sin transformar y transformados.

Para usar la combinación de vértices indizada, la \_ marca D3DFVF LASTBETA \_ UBYTE4 debe aparecer al final de la declaración FVF. La presencia de esta marca indica que el quinto peso de la mezcla se tratará como DWORD en lugar de como float. Para obtener más información, vea [fusión de vértices indizados (Direct3D 9)](indexed-vertex-blending.md).

En los siguientes ejemplos de código se muestra la diferencia entre un código FVF que usa la \_ marca D3DFVF LASTBETA \_ UBYTE4 y otro que no lo es. La marca D3DFVF \_ XYZB3 está presente cuando se usan cuatro índices de mezcla porque siempre resta la suma de los tres primeros del número uno para obtener el cuarto (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



El FVF que se define a continuación usa la \_ marca D3DFVF Last \_ UBYTE4.


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declaración de vértice](vertex-declaration.md)
</dt> </dl>

 

 

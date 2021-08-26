---
description: Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Códigos FVF de función fija (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4fb691192fcc4dbd7dc42c4d6c00829c209f87f68ec32ea42f6c26ff4663c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069204"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Códigos FVF de función fija (Direct3D 9)

Un código FVF describe el contenido de los vértices almacenados intercalados en un único flujo de datos. Por lo general, especifica los datos que va a procesar la canalización de procesamiento de vértices de función fija. Se trata de una declaración de vértice de estilo anterior; Para ver el estilo de declaración de vértice actual, vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Las aplicaciones de Direct3D pueden definir los vértices del modelo de varias maneras diferentes. La compatibilidad con definiciones de vértice flexibles, también conocidas como formatos de vértice flexibles o códigos de formato de vértice flexible, permite que la aplicación use solo los componentes de vértice que necesita, lo que elimina los componentes que no se usan. Al usar solo los componentes de vértice necesarios, la aplicación puede conservar memoria y minimizar el ancho de banda de procesamiento necesario para representar los modelos. Describe cómo se formatearán los vértices mediante una combinación de [códigos D3DFVF.](d3dfvf.md)

La especificación FVF incluye formatos para el tamaño de punto, especificados por D3DFVF \_ PSIZE. Este tamaño se expresa en unidades de espacio de la cámara para los vértices no transformados y encendidos (TL) y en unidades de espacio del dispositivo para los vértices TL.

Los métodos de representación de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) proporcionan a las aplicaciones de C++ métodos que aceptan una combinación de estas marcas y los usan para determinar cómo representar primitivas. Básicamente, estas marcas le dicen al sistema qué componentes de vértice (posición, pesos de combinación de vértices, normal, colores y el número y formato de coordenadas de textura) la aplicación usa y, indirectamente, qué partes de la canalización de representación quiere que Se les aplique Direct3D. Además, la presencia o ausencia de una marca de formato de vértice determinada comunica al sistema qué campos de componentes de vértice están presentes en la memoria y cuáles ha omitido.

Para determinar las limitaciones del dispositivo, puede consultar a un dispositivo los valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS y D3DFVFCAPS \_ TEXCOORDCOUNTMASK en el miembro FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

Las coordenadas de textura se pueden declarar en formatos diferentes, lo que permite que las texturas se aborde con tan solo una coordenada o hasta cuatro coordenadas de textura (para coordenadas de textura proyectadas en 2D). Para obtener más información, vea [Formatos de coordenadas de textura (Direct3D 9).](texture-coordinate-formats.md) Use el conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para crear patrones de bits que identifiquen los formatos de coordenadas de textura que usa el formato de vértice.

Ninguna aplicación usará todos los componentes. Los campos homogéneos recíprocos W (RHW) y normal de vértices son mutuamente excluyentes. La mayoría de las aplicaciones tampoco intentarán usar los ocho conjuntos de coordenadas de textura, pero Direct3D tiene esta capacidad. Hay varias restricciones en las que las marcas se pueden usar con otras marcas. Por ejemplo, no puede usar las marcas D3DFVF XYZ y \_ D3DFVF XYZRHW juntos, ya que esto indicaría que la aplicación está describiendo la posición de un vértice con vértices sin transformar y \_ transformados.

Para usar la combinación de vértices indexada, la marca D3DFVF \_ LASTBETA UBYTE4 debe aparecer \_ al final de la declaración FVF. La presencia de esta marca indica que el quinto peso de mezcla se tratará como DWORD en lugar de float. Para obtener más información, [vea Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).

En los ejemplos de código siguientes se muestra la diferencia entre un código FVF que usa la marca D3DFVF \_ LASTBETA UBYTE4 y otro \_ que no. La marca D3DFVF XYZB3 está presente cuando se usan cuatro índices de mezcla porque siempre se resta la suma de los tres primeros del número uno para obtener el cuarto \_ (blend₄ = 1 - (blend₁ + blend3 + blend₃)).


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



La FVF definida a continuación usa la marca D3DFVF \_ LAST \_ UBYTE4.


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

 

 

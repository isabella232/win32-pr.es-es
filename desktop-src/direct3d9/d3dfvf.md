---
description: Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56136b57aa0af7e8a7d4050f9feb6e1e3e92f3b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629744"
---
# <a name="d3dfvf"></a>D3DFVF

Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.

## <a name="vertex-data-flags"></a>Marcas de datos de vértices

Las marcas siguientes describen un formato de vértice. Para obtener información sobre los formatos de vértice, [vea Códigos FVF de función fija (Direct3D 9).](fixed-function-fvf-codes.md)



| \#Definir                            | Descripción                                                                                                                                                                                                                                                                                                                                                             | Orden y tipo de datos                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D3DFVF \_ DIFUSO                     | El formato de vértice incluye un componente de color difuso.                                                                                                                                                                                                                                                                                                                       | DWORD en orden ARGB. Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ NORMAL                      | El formato de vértice incluye un vector normal de vértice. Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ PSIZE                       | Formato de vértice especificado en tamaño de punto. Este tamaño se expresa en unidades de espacio de la cámara para vértices que no se transforman ni se encienden, y en unidades de espacio del dispositivo para vértices transformados y encendidos.                                                                                                                                                                          | FLOAT                                                                                                     |
| ESPECULAR D3DFVF \_                    | El formato de vértice incluye un componente de color especular.                                                                                                                                                                                                                                                                                                                      | DWORD en orden ARGB. Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | El formato de vértice incluye la posición de un vértice sin convertir. Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ XYZRHW                      | El formato de vértice incluye la posición de un vértice transformado. Esta marca no se puede usar con las marcas D3DFVF \_ XYZ o D3DFVF \_ NORMAL.                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5 | El formato de vértice contiene datos de posición y un número correspondiente de valores de ponderación (beta) que se usarán para las operaciones de combinación de vértices multimatrix. Actualmente, Direct3D puede combinarse con hasta tres valores de ponderación y cuatro matrices de mezcla. Para obtener más información sobre el uso de matrices de mezcla, vea [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 o 3 flotantes. Cuando se usa D3DFVF \_ LASTBETA UBYTE4, el último peso de mezcla \_ se trata como DWORD. |
| D3DFVF \_ XYZW                        | El formato de vértice contiene datos transformados y recortados (x, y, z, w). ProcessVertices no invoca el recortador, sino que genera datos en coordenadas de recorte. Esta constante está diseñada para y solo se puede usar con la canalización de vértices programable.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Marcas de textura

Las marcas siguientes describen las marcas de textura usadas por la canalización de función fija.



| \#Definir                          | Descripción                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0 - D3DFVF \_ TEX8       | Número de conjuntos de coordenadas de textura para este vértice. Los valores reales de estas marcas no son secuenciales.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN(coordIndex) | Defina un conjunto de datos de coordenadas de textura. n indica la dimensión de las coordenadas de textura. coordIndex indica el número de índice de coordenadas de textura. Vea [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) y [Coordenadas de textura y Fases de textura.](texture-coordinates.md) |



 

## <a name="mask-flags"></a>Marcas de máscara

Las marcas siguientes describen las marcas de máscara usadas por la canalización de función fija.



| \#Definir                             | Descripción                                           |
|--------------------------------------|-------------------------------------------------------|
| MÁSCARA DE POSICIÓN D3DFVF \_ \_               | Máscara para los bits de posición.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Enmascara los valores de los bits reservados en FVF. No debe usarse. |
| D3DFVF \_ TEXCOUNT \_ MASK               | Valor de máscara para los bits de la marca de textura.                     |



 

## <a name="miscellaneous-flags"></a>Marcas misceláneas

Las marcas siguientes describen una variedad de marcas usadas por la canalización de función fija.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>El último campo beta de los datos de posición del vértice será del tipo D3DCOLOR. Los datos de los campos beta se usan con el desnasado de la paleta de matrices para especificar índices de matriz.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>El último campo beta de los datos de posición del vértice será del tipo UBYTE4. Los datos de los campos beta se usan con el desnasado de la paleta de matrices para especificar índices de matriz. <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Dado que la FVF se declara como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight y MatrixIndices se incluyen en beta[5], donde D3DFVF_LASTBETA_UBYTE4 indica que interprete el último DWORD en beta[5] como tipo UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Número de bits por los que se desplaza un valor entero que identifica el número de coordenadas de textura de un vértice. Este valor puede usarse como se muestra a continuación.
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestran otras combinaciones de marcas comunes.


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a>Información constante



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3d9types.h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Combinación de geometría (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 




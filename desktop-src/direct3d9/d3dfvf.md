---
description: Las constantes de formato de vértice flexible, o los códigos FVF, se usan para describir el contenido de los vértices intercalados en un flujo de datos único que se procesará mediante la canalización de función fija.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4bfc1dcabdb6991b49af967bb596fd4c1e3bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686454"
---
# <a name="d3dfvf"></a>D3DFVF

Las constantes de formato de vértice flexible, o los códigos FVF, se usan para describir el contenido de los vértices intercalados en un flujo de datos único que se procesará mediante la canalización de función fija.

## <a name="vertex-data-flags"></a>Marcadores de datos de vértices

Las marcas siguientes describen un formato de vértice. Para obtener información sobre los formatos de vértices, vea [códigos FVF de funciones fijas (Direct3D 9)](fixed-function-fvf-codes.md).



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| \#define                            | Descripción                                                                                                                                                                                                                                                                                                                                                             | Orden de datos y tipo                                                                                       |
| \_Difusión D3DFVF                     | El formato de vértice incluye un componente de color difuso.                                                                                                                                                                                                                                                                                                                       | DWORD en orden ARGB. Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ normal                      | El formato de vértice incluye un vector normal de vértice. Esta marca no se puede usar con la \_ marca XYZRHW de D3DFVF.                                                                                                                                                                                                                                                                   | Float, Float, Float                                                                                       |
| D3DFVF \_ PSIZE                       | Formato de vértice especificado en el tamaño de punto. Este tamaño se expresa en unidades de espacio de la cámara para los vértices que no se transforman y iluminan, y en unidades de espacio de dispositivo para los vértices transformados y iluminados.                                                                                                                                                                          | FLOAT                                                                                                     |
| \_Reflejo D3DFVF                    | El formato de vértice incluye un componente de color especular.                                                                                                                                                                                                                                                                                                                      | DWORD en orden ARGB. Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | El formato de vértice incluye la posición de un vértice no transformado. Esta marca no se puede usar con la \_ marca XYZRHW de D3DFVF.                                                                                                                                                                                                                                                  | Float, Float, Float.                                                                                      |
| D3DFVF \_ XYZRHW                      | El formato de vértice incluye la posición de un vértice transformado. Esta marca no se puede usar con las \_ marcas normales D3DFVF XYZ ni D3DFVF \_ .                                                                                                                                                                                                                                     | Float, Float, Float, Float.                                                                               |
| D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5 | El formato de vértice contiene datos de posición y un número correspondiente de valores de ponderación (beta) que se usarán para las operaciones de combinación de vértices multimatrix. Actualmente, Direct3D puede fusionar con hasta tres valores de ponderación y cuatro matrices de mezcla. Para obtener más información sobre el uso de matrices de mezcla, vea [fusión de vértices indizados (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 o 3 flotantes. Cuando \_ \_ se usa D3DFVF LASTBETA UBYTE4, el último peso de la mezcla se trata como un valor DWORD. |
| D3DFVF \_ XYZW                        | El formato de vértice contiene datos transformados y recortados (x, y, z, w). ProcessVertices no invoca Clipper, sino que genera datos en coordenadas de recorte. Esta constante está diseñada para y solo se puede usar con, la canalización de vértices programable.                                                                                                                 | Float, Float, Float, Float                                                                                |



 

## <a name="texture-flags"></a>Marcas de textura

Las marcas siguientes describen las marcas de textura utilizadas por la canalización de funciones fijas.



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#define                          | Descripción                                                                                                                                                                                                                                                                        |
| D3DFVF \_ TEX0-D3DFVF \_ TEX8       | Número de conjuntos de coordenadas de textura para este vértice. Los valores reales de estas marcas no son secuenciales.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN (coordIndex) | Defina un conjunto de datos de coordenadas de textura. n indica la dimensión de las coordenadas de textura. coordIndex indica el número de índice de coordenadas de textura. Consulte [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) y las [coordenadas de textura y las fases de textura](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Marcas de máscara

En los siguientes marcadores se describen las marcas de máscara utilizadas por la canalización de funciones fijas.



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| \#define                             | Descripción                                           |
| \_Máscara de posición de D3DFVF \_               | Máscara para bits de posición.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Enmascara valores para bits reservados en el FVF. No debe usarse. |
| D3DFVF \_ máscara de TEXCOUNT \_               | Valor de máscara para los bits de la marca de textura.                     |



 

## <a name="miscellaneous-flags"></a>Marcas misceláneas

Las marcas siguientes describen una variedad de marcas usadas por la canalización de funciones fijas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#define</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>El último campo de la versión beta en los datos de posición del vértice será de tipo D3DCOLOR. Los datos de los campos beta se usan con la presentación de la paleta de la matriz para especificar índices de matriz.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>El último campo de la versión beta en los datos de posición del vértice será de tipo UBYTE4. Los datos de los campos beta se usan con la presentación de la paleta de la matriz para especificar índices de matriz. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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

<p>Dado que FVF se declara como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight y MatrixIndices se incluyen en la versión beta [5], donde D3DFVF_LASTBETA_UBYTE4 dice interpretar el último valor DWORD de beta [5] como tipo UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Número de bits por el que se va a desplazar un valor entero que identifica el número de coordenadas de textura de un vértice. Este valor se puede usar como se muestra a continuación.
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Combinación de geometría (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 




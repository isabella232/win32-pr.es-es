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
# <a name="d3dfvf"></a><span data-ttu-id="d91dc-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="d91dc-103">D3DFVF</span></span>

<span data-ttu-id="d91dc-104">Las constantes de formato de vértice flexible, o los códigos FVF, se usan para describir el contenido de los vértices intercalados en un flujo de datos único que se procesará mediante la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="d91dc-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="d91dc-105">Marcadores de datos de vértices</span><span class="sxs-lookup"><span data-stu-id="d91dc-105">Vertex Data Flags</span></span>

<span data-ttu-id="d91dc-106">Las marcas siguientes describen un formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="d91dc-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="d91dc-107">Para obtener información sobre los formatos de vértices, vea [códigos FVF de funciones fijas (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d91dc-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91dc-108">\#define</span><span class="sxs-lookup"><span data-stu-id="d91dc-108">\#define</span></span>                            | <span data-ttu-id="d91dc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d91dc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="d91dc-110">Orden de datos y tipo</span><span class="sxs-lookup"><span data-stu-id="d91dc-110">Data order and type</span></span>                                                                                       |
| <span data-ttu-id="d91dc-111">\_Difusión D3DFVF</span><span class="sxs-lookup"><span data-stu-id="d91dc-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="d91dc-112">El formato de vértice incluye un componente de color difuso.</span><span class="sxs-lookup"><span data-stu-id="d91dc-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="d91dc-113">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="d91dc-113">DWORD in ARGB order.</span></span> <span data-ttu-id="d91dc-114">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="d91dc-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="d91dc-115">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="d91dc-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="d91dc-116">El formato de vértice incluye un vector normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="d91dc-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="d91dc-117">Esta marca no se puede usar con la \_ marca XYZRHW de D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="d91dc-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d91dc-118">Float, Float, Float</span><span class="sxs-lookup"><span data-stu-id="d91dc-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="d91dc-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="d91dc-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="d91dc-120">Formato de vértice especificado en el tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="d91dc-120">Vertex format specified in point size.</span></span> <span data-ttu-id="d91dc-121">Este tamaño se expresa en unidades de espacio de la cámara para los vértices que no se transforman y iluminan, y en unidades de espacio de dispositivo para los vértices transformados y iluminados.</span><span class="sxs-lookup"><span data-stu-id="d91dc-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="d91dc-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d91dc-122">float</span></span>                                                                                                     |
| <span data-ttu-id="d91dc-123">\_Reflejo D3DFVF</span><span class="sxs-lookup"><span data-stu-id="d91dc-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="d91dc-124">El formato de vértice incluye un componente de color especular.</span><span class="sxs-lookup"><span data-stu-id="d91dc-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="d91dc-125">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="d91dc-125">DWORD in ARGB order.</span></span> <span data-ttu-id="d91dc-126">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="d91dc-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="d91dc-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="d91dc-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="d91dc-128">El formato de vértice incluye la posición de un vértice no transformado.</span><span class="sxs-lookup"><span data-stu-id="d91dc-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="d91dc-129">Esta marca no se puede usar con la \_ marca XYZRHW de D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="d91dc-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="d91dc-130">Float, Float, Float.</span><span class="sxs-lookup"><span data-stu-id="d91dc-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="d91dc-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="d91dc-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="d91dc-132">El formato de vértice incluye la posición de un vértice transformado.</span><span class="sxs-lookup"><span data-stu-id="d91dc-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="d91dc-133">Esta marca no se puede usar con las \_ marcas normales D3DFVF XYZ ni D3DFVF \_ .</span><span class="sxs-lookup"><span data-stu-id="d91dc-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="d91dc-134">Float, Float, Float, Float.</span><span class="sxs-lookup"><span data-stu-id="d91dc-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="d91dc-135">D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="d91dc-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="d91dc-136">El formato de vértice contiene datos de posición y un número correspondiente de valores de ponderación (beta) que se usarán para las operaciones de combinación de vértices multimatrix.</span><span class="sxs-lookup"><span data-stu-id="d91dc-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="d91dc-137">Actualmente, Direct3D puede fusionar con hasta tres valores de ponderación y cuatro matrices de mezcla.</span><span class="sxs-lookup"><span data-stu-id="d91dc-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="d91dc-138">Para obtener más información sobre el uso de matrices de mezcla, vea [fusión de vértices indizados (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="d91dc-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="d91dc-139">1, 2 o 3 flotantes.</span><span class="sxs-lookup"><span data-stu-id="d91dc-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="d91dc-140">Cuando \_ \_ se usa D3DFVF LASTBETA UBYTE4, el último peso de la mezcla se trata como un valor DWORD.</span><span class="sxs-lookup"><span data-stu-id="d91dc-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="d91dc-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="d91dc-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="d91dc-142">El formato de vértice contiene datos transformados y recortados (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="d91dc-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="d91dc-143">ProcessVertices no invoca Clipper, sino que genera datos en coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="d91dc-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="d91dc-144">Esta constante está diseñada para y solo se puede usar con, la canalización de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="d91dc-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="d91dc-145">Float, Float, Float, Float</span><span class="sxs-lookup"><span data-stu-id="d91dc-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="d91dc-146">Marcas de textura</span><span class="sxs-lookup"><span data-stu-id="d91dc-146">Texture Flags</span></span>

<span data-ttu-id="d91dc-147">Las marcas siguientes describen las marcas de textura utilizadas por la canalización de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="d91dc-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91dc-148">\#define</span><span class="sxs-lookup"><span data-stu-id="d91dc-148">\#define</span></span>                          | <span data-ttu-id="d91dc-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="d91dc-149">Description</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d91dc-150">D3DFVF \_ TEX0-D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="d91dc-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="d91dc-151">Número de conjuntos de coordenadas de textura para este vértice.</span><span class="sxs-lookup"><span data-stu-id="d91dc-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="d91dc-152">Los valores reales de estas marcas no son secuenciales.</span><span class="sxs-lookup"><span data-stu-id="d91dc-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="d91dc-153">D3DFVF \_ TEXCOORDSIZEN (coordIndex)</span><span class="sxs-lookup"><span data-stu-id="d91dc-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="d91dc-154">Defina un conjunto de datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d91dc-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="d91dc-155">n indica la dimensión de las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d91dc-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="d91dc-156">coordIndex indica el número de índice de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="d91dc-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="d91dc-157">Consulte [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) y las [coordenadas de textura y las fases de textura](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="d91dc-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="d91dc-158">Marcas de máscara</span><span class="sxs-lookup"><span data-stu-id="d91dc-158">Mask Flags</span></span>

<span data-ttu-id="d91dc-159">En los siguientes marcadores se describen las marcas de máscara utilizadas por la canalización de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="d91dc-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="d91dc-160">\#define</span><span class="sxs-lookup"><span data-stu-id="d91dc-160">\#define</span></span>                             | <span data-ttu-id="d91dc-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="d91dc-161">Description</span></span>                                           |
| <span data-ttu-id="d91dc-162">\_Máscara de posición de D3DFVF \_</span><span class="sxs-lookup"><span data-stu-id="d91dc-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="d91dc-163">Máscara para bits de posición.</span><span class="sxs-lookup"><span data-stu-id="d91dc-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="d91dc-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="d91dc-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="d91dc-165">Enmascara valores para bits reservados en el FVF.</span><span class="sxs-lookup"><span data-stu-id="d91dc-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="d91dc-166">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="d91dc-166">Do not use.</span></span> |
| <span data-ttu-id="d91dc-167">D3DFVF \_ máscara de TEXCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="d91dc-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="d91dc-168">Valor de máscara para los bits de la marca de textura.</span><span class="sxs-lookup"><span data-stu-id="d91dc-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="d91dc-169">Marcas misceláneas</span><span class="sxs-lookup"><span data-stu-id="d91dc-169">Miscellaneous Flags</span></span>

<span data-ttu-id="d91dc-170">Las marcas siguientes describen una variedad de marcas usadas por la canalización de funciones fijas.</span><span class="sxs-lookup"><span data-stu-id="d91dc-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d91dc-171">#define</span><span class="sxs-lookup"><span data-stu-id="d91dc-171">#define</span></span></td>
<td><span data-ttu-id="d91dc-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="d91dc-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d91dc-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d91dc-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="d91dc-174">El último campo de la versión beta en los datos de posición del vértice será de tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="d91dc-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="d91dc-175">Los datos de los campos beta se usan con la presentación de la paleta de la matriz para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="d91dc-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d91dc-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d91dc-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="d91dc-177">El último campo de la versión beta en los datos de posición del vértice será de tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d91dc-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="d91dc-178">Los datos de los campos beta se usan con la presentación de la paleta de la matriz para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="d91dc-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
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

<p><span data-ttu-id="d91dc-179">Dado que FVF se declara como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d91dc-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="d91dc-180">Weight y MatrixIndices se incluyen en la versión beta [5], donde D3DFVF_LASTBETA_UBYTE4 dice interpretar el último valor DWORD de beta [5] como tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d91dc-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d91dc-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="d91dc-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="d91dc-182">Número de bits por el que se va a desplazar un valor entero que identifica el número de coordenadas de textura de un vértice.</span><span class="sxs-lookup"><span data-stu-id="d91dc-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="d91dc-183">Este valor se puede usar como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d91dc-183">This value might be used as shown below.</span></span>
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



 

### <a name="examples"></a><span data-ttu-id="d91dc-184">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d91dc-184">Examples</span></span>

<span data-ttu-id="d91dc-185">En los ejemplos siguientes se muestran otras combinaciones de marcas comunes.</span><span class="sxs-lookup"><span data-stu-id="d91dc-185">The following examples show other common flag combinations.</span></span>


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



## <a name="constant-information"></a><span data-ttu-id="d91dc-186">Información constante</span><span class="sxs-lookup"><span data-stu-id="d91dc-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="d91dc-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d91dc-187">Header</span></span>                   | <span data-ttu-id="d91dc-188">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="d91dc-188">d3d9types.h</span></span> |
| <span data-ttu-id="d91dc-189">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="d91dc-189">Minimum operating system</span></span> | <span data-ttu-id="d91dc-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="d91dc-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="d91dc-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d91dc-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d91dc-192">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d91dc-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="d91dc-193">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d91dc-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="d91dc-194">Combinación de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d91dc-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 




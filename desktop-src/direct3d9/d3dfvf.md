---
description: Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343270"
---
# <a name="d3dfvf"></a><span data-ttu-id="0fae3-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="0fae3-103">D3DFVF</span></span>

<span data-ttu-id="0fae3-104">Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.</span><span class="sxs-lookup"><span data-stu-id="0fae3-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="0fae3-105">Marcas de datos de vértices</span><span class="sxs-lookup"><span data-stu-id="0fae3-105">Vertex Data Flags</span></span>

<span data-ttu-id="0fae3-106">Las marcas siguientes describen un formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="0fae3-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="0fae3-107">Para obtener información sobre los formatos de vértice, [vea Códigos FVF de función fija (Direct3D 9).](fixed-function-fvf-codes.md)</span><span class="sxs-lookup"><span data-stu-id="0fae3-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="0fae3-108">\#Definir</span><span class="sxs-lookup"><span data-stu-id="0fae3-108">\#define</span></span>                            | <span data-ttu-id="0fae3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fae3-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="0fae3-110">Orden y tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0fae3-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fae3-111">D3DFVF \_ DIFUSO</span><span class="sxs-lookup"><span data-stu-id="0fae3-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="0fae3-112">El formato de vértice incluye un componente de color difuso.</span><span class="sxs-lookup"><span data-stu-id="0fae3-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="0fae3-113">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="0fae3-113">DWORD in ARGB order.</span></span> <span data-ttu-id="0fae3-114">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="0fae3-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="0fae3-115">D3DFVF \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="0fae3-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="0fae3-116">El formato de vértice incluye un vector normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="0fae3-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="0fae3-117">Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="0fae3-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0fae3-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="0fae3-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="0fae3-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="0fae3-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="0fae3-120">Formato de vértice especificado en tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="0fae3-120">Vertex format specified in point size.</span></span> <span data-ttu-id="0fae3-121">Este tamaño se expresa en unidades de espacio de la cámara para los vértices que no se transforman ni se encienden, y en unidades de espacio del dispositivo para vértices transformados y encendidos.</span><span class="sxs-lookup"><span data-stu-id="0fae3-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="0fae3-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0fae3-122">float</span></span>                                                                                                     |
| <span data-ttu-id="0fae3-123">ESPECULAR D3DFVF \_</span><span class="sxs-lookup"><span data-stu-id="0fae3-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="0fae3-124">El formato de vértice incluye un componente de color especular.</span><span class="sxs-lookup"><span data-stu-id="0fae3-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="0fae3-125">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="0fae3-125">DWORD in ARGB order.</span></span> <span data-ttu-id="0fae3-126">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="0fae3-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="0fae3-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="0fae3-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="0fae3-128">El formato de vértice incluye la posición de un vértice sin convertir.</span><span class="sxs-lookup"><span data-stu-id="0fae3-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="0fae3-129">Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="0fae3-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="0fae3-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="0fae3-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="0fae3-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="0fae3-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="0fae3-132">El formato de vértice incluye la posición de un vértice transformado.</span><span class="sxs-lookup"><span data-stu-id="0fae3-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="0fae3-133">Esta marca no se puede usar con las marcas D3DFVF \_ XYZ o D3DFVF \_ NORMAL.</span><span class="sxs-lookup"><span data-stu-id="0fae3-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="0fae3-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="0fae3-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="0fae3-135">D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="0fae3-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="0fae3-136">El formato de vértice contiene datos de posición y un número correspondiente de valores de ponderación (beta) que se usarán para las operaciones de combinación de vértices multimatrix.</span><span class="sxs-lookup"><span data-stu-id="0fae3-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="0fae3-137">Actualmente, Direct3D puede combinarse con hasta tres valores de ponderación y cuatro matrices de mezcla.</span><span class="sxs-lookup"><span data-stu-id="0fae3-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="0fae3-138">Para obtener más información sobre el uso de matrices de mezcla, vea [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="0fae3-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="0fae3-139">1, 2 o 3 flotantes.</span><span class="sxs-lookup"><span data-stu-id="0fae3-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="0fae3-140">Cuando se usa D3DFVF \_ LASTBETA UBYTE4, el último peso de mezcla \_ se trata como DWORD.</span><span class="sxs-lookup"><span data-stu-id="0fae3-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="0fae3-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="0fae3-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="0fae3-142">El formato de vértice contiene datos transformados y recortados (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="0fae3-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="0fae3-143">ProcessVertices no invoca el clipper, sino que genera datos en coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="0fae3-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="0fae3-144">Esta constante está diseñada para la canalización programable de vértices y solo se puede usar con esta.</span><span class="sxs-lookup"><span data-stu-id="0fae3-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="0fae3-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="0fae3-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="0fae3-146">Marcas de textura</span><span class="sxs-lookup"><span data-stu-id="0fae3-146">Texture Flags</span></span>

<span data-ttu-id="0fae3-147">Las marcas siguientes describen las marcas de textura usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="0fae3-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="0fae3-148">\#Definir</span><span class="sxs-lookup"><span data-stu-id="0fae3-148">\#define</span></span>                          | <span data-ttu-id="0fae3-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fae3-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fae3-150">D3DFVF \_ TEX0 - D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="0fae3-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="0fae3-151">Número de conjuntos de coordenadas de textura para este vértice.</span><span class="sxs-lookup"><span data-stu-id="0fae3-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="0fae3-152">Los valores reales de estas marcas no son secuenciales.</span><span class="sxs-lookup"><span data-stu-id="0fae3-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="0fae3-153">D3DFVF \_ TEXCOORDSIZEN(coordIndex)</span><span class="sxs-lookup"><span data-stu-id="0fae3-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="0fae3-154">Defina un conjunto de datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0fae3-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="0fae3-155">n indica la dimensión de las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0fae3-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="0fae3-156">coordIndex indica el número de índice de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="0fae3-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="0fae3-157">Vea [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) y Las coordenadas [de textura y las fases de textura.](texture-coordinates.md)</span><span class="sxs-lookup"><span data-stu-id="0fae3-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="0fae3-158">Marcas de máscara</span><span class="sxs-lookup"><span data-stu-id="0fae3-158">Mask Flags</span></span>

<span data-ttu-id="0fae3-159">Las marcas siguientes describen las marcas de máscara usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="0fae3-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="0fae3-160">\#Definir</span><span class="sxs-lookup"><span data-stu-id="0fae3-160">\#define</span></span>                             | <span data-ttu-id="0fae3-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fae3-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0fae3-162">MÁSCARA DE POSICIÓN D3DFVF \_ \_</span><span class="sxs-lookup"><span data-stu-id="0fae3-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="0fae3-163">Máscara para los bits de posición.</span><span class="sxs-lookup"><span data-stu-id="0fae3-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="0fae3-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="0fae3-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="0fae3-165">Enmascara los valores de los bits reservados en FVF.</span><span class="sxs-lookup"><span data-stu-id="0fae3-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="0fae3-166">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="0fae3-166">Do not use.</span></span> |
| <span data-ttu-id="0fae3-167">D3DFVF \_ TEXCOUNT \_ MASK</span><span class="sxs-lookup"><span data-stu-id="0fae3-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="0fae3-168">Valor de máscara para los bits de la marca de textura.</span><span class="sxs-lookup"><span data-stu-id="0fae3-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="0fae3-169">Marcas misceláneas</span><span class="sxs-lookup"><span data-stu-id="0fae3-169">Miscellaneous Flags</span></span>

<span data-ttu-id="0fae3-170">Las marcas siguientes describen una variedad de marcas usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="0fae3-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0fae3-171">#Definir</span><span class="sxs-lookup"><span data-stu-id="0fae3-171">#define</span></span></td>
<td><span data-ttu-id="0fae3-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fae3-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fae3-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="0fae3-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="0fae3-174">El último campo beta de los datos de posición del vértice será del tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="0fae3-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="0fae3-175">Los datos de los campos beta se usan con el desnasado de la paleta de matrices para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="0fae3-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0fae3-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="0fae3-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="0fae3-177">El último campo beta de los datos de posición del vértice será del tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0fae3-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="0fae3-178">Los datos de los campos beta se usan con el desnasado de la paleta de matrices para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="0fae3-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
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

<p><span data-ttu-id="0fae3-179">Dado que la FVF se declara como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0fae3-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="0fae3-180">Weight y MatrixIndices se incluyen en beta[5], donde D3DFVF_LASTBETA_UBYTE4 indica que interprete el último DWORD en beta[5] como tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0fae3-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0fae3-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="0fae3-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="0fae3-182">Número de bits por los que se desplaza un valor entero que identifica el número de coordenadas de textura para un vértice.</span><span class="sxs-lookup"><span data-stu-id="0fae3-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="0fae3-183">Este valor puede usarse como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="0fae3-183">This value might be used as shown below.</span></span>
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



 

### <a name="examples"></a><span data-ttu-id="0fae3-184">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0fae3-184">Examples</span></span>

<span data-ttu-id="0fae3-185">En los ejemplos siguientes se muestran otras combinaciones de marcas comunes.</span><span class="sxs-lookup"><span data-stu-id="0fae3-185">The following examples show other common flag combinations.</span></span>


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



## <a name="constant-information"></a><span data-ttu-id="0fae3-186">Información constante</span><span class="sxs-lookup"><span data-stu-id="0fae3-186">Constant Information</span></span>



| <span data-ttu-id="0fae3-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fae3-187">Requirement</span></span>                         | <span data-ttu-id="0fae3-188">Value</span><span class="sxs-lookup"><span data-stu-id="0fae3-188">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="0fae3-189">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fae3-189">Header</span></span>                   | <span data-ttu-id="0fae3-190">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="0fae3-190">d3d9types.h</span></span> |
| <span data-ttu-id="0fae3-191">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="0fae3-191">Minimum operating system</span></span> | <span data-ttu-id="0fae3-192">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0fae3-192">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="0fae3-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0fae3-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fae3-194">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0fae3-194">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="0fae3-195">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fae3-195">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="0fae3-196">Mezcla de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0fae3-196">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 




---
description: Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a12b4f6008023a388bd204440a0b544db85c19
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999442"
---
# <a name="d3dfvf"></a><span data-ttu-id="aec0a-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="aec0a-103">D3DFVF</span></span>

<span data-ttu-id="aec0a-104">Las constantes de formato de vértice flexible, o códigos FVF, se usan para describir el contenido de los vértices intercalados en un único flujo de datos que la canalización de función fija procesará.</span><span class="sxs-lookup"><span data-stu-id="aec0a-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="aec0a-105">Marcas de datos de vértices</span><span class="sxs-lookup"><span data-stu-id="aec0a-105">Vertex Data Flags</span></span>

<span data-ttu-id="aec0a-106">Las marcas siguientes describen un formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="aec0a-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="aec0a-107">Para obtener información sobre los formatos de vértice, [vea Códigos FVF de función fija (Direct3D 9).](fixed-function-fvf-codes.md)</span><span class="sxs-lookup"><span data-stu-id="aec0a-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="aec0a-108">\#Definir</span><span class="sxs-lookup"><span data-stu-id="aec0a-108">\#define</span></span>                            | <span data-ttu-id="aec0a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="aec0a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="aec0a-110">Orden y tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aec0a-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec0a-111">D3DFVF \_ DIFUSO</span><span class="sxs-lookup"><span data-stu-id="aec0a-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="aec0a-112">El formato de vértice incluye un componente de color difuso.</span><span class="sxs-lookup"><span data-stu-id="aec0a-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="aec0a-113">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="aec0a-113">DWORD in ARGB order.</span></span> <span data-ttu-id="aec0a-114">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="aec0a-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="aec0a-115">D3DFVF \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="aec0a-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="aec0a-116">El formato de vértice incluye un vector normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="aec0a-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="aec0a-117">Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="aec0a-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="aec0a-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="aec0a-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="aec0a-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="aec0a-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="aec0a-120">Formato de vértice especificado en tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="aec0a-120">Vertex format specified in point size.</span></span> <span data-ttu-id="aec0a-121">Este tamaño se expresa en unidades de espacio de la cámara para vértices que no se transforman ni se encienden, y en unidades de espacio del dispositivo para vértices transformados y encendidos.</span><span class="sxs-lookup"><span data-stu-id="aec0a-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="aec0a-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="aec0a-122">float</span></span>                                                                                                     |
| <span data-ttu-id="aec0a-123">D3DFVF \_ SPECULAR</span><span class="sxs-lookup"><span data-stu-id="aec0a-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="aec0a-124">El formato de vértice incluye un componente de color especular.</span><span class="sxs-lookup"><span data-stu-id="aec0a-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="aec0a-125">DWORD en orden ARGB.</span><span class="sxs-lookup"><span data-stu-id="aec0a-125">DWORD in ARGB order.</span></span> <span data-ttu-id="aec0a-126">Vea [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="aec0a-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="aec0a-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="aec0a-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="aec0a-128">El formato de vértice incluye la posición de un vértice sin formato.</span><span class="sxs-lookup"><span data-stu-id="aec0a-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="aec0a-129">Esta marca no se puede usar con la marca D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="aec0a-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="aec0a-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="aec0a-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="aec0a-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="aec0a-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="aec0a-132">El formato de vértice incluye la posición de un vértice transformado.</span><span class="sxs-lookup"><span data-stu-id="aec0a-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="aec0a-133">Esta marca no se puede usar con las marcas D3DFVF \_ XYZ o D3DFVF \_ NORMAL.</span><span class="sxs-lookup"><span data-stu-id="aec0a-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="aec0a-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="aec0a-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="aec0a-135">D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="aec0a-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="aec0a-136">El formato de vértice contiene datos de posición y un número correspondiente de valores de ponderación (beta) que se usarán para las operaciones de combinación de vértices multimatrix.</span><span class="sxs-lookup"><span data-stu-id="aec0a-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="aec0a-137">Actualmente, Direct3D puede combinarse con hasta tres valores de ponderación y cuatro matrices de mezcla.</span><span class="sxs-lookup"><span data-stu-id="aec0a-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="aec0a-138">Para obtener más información sobre el uso de matrices de mezcla, vea [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md)(Mezcla de vértices indexados [Direct3D 9]).</span><span class="sxs-lookup"><span data-stu-id="aec0a-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="aec0a-139">1, 2 o 3 flotantes.</span><span class="sxs-lookup"><span data-stu-id="aec0a-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="aec0a-140">Cuando se usa D3DFVF \_ LASTBETA UBYTE4, el último peso de mezcla se \_ trata como DWORD.</span><span class="sxs-lookup"><span data-stu-id="aec0a-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="aec0a-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="aec0a-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="aec0a-142">El formato de vértice contiene datos transformados y recortados (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="aec0a-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="aec0a-143">ProcessVertices no invoca el recortador, sino que genera datos en coordenadas de recorte.</span><span class="sxs-lookup"><span data-stu-id="aec0a-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="aec0a-144">Esta constante está diseñada para y solo se puede usar con la canalización de vértices programable.</span><span class="sxs-lookup"><span data-stu-id="aec0a-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="aec0a-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="aec0a-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="aec0a-146">Marcas de textura</span><span class="sxs-lookup"><span data-stu-id="aec0a-146">Texture Flags</span></span>

<span data-ttu-id="aec0a-147">Las marcas siguientes describen las marcas de textura usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="aec0a-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="aec0a-148">\#Definir</span><span class="sxs-lookup"><span data-stu-id="aec0a-148">\#define</span></span>                          | <span data-ttu-id="aec0a-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="aec0a-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec0a-150">D3DFVF \_ TEX0 - D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="aec0a-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="aec0a-151">Número de conjuntos de coordenadas de textura para este vértice.</span><span class="sxs-lookup"><span data-stu-id="aec0a-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="aec0a-152">Los valores reales de estas marcas no son secuenciales.</span><span class="sxs-lookup"><span data-stu-id="aec0a-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="aec0a-153">D3DFVF \_ TEXCOORDSIZEN(coordIndex)</span><span class="sxs-lookup"><span data-stu-id="aec0a-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="aec0a-154">Defina un conjunto de datos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="aec0a-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="aec0a-155">n indica la dimensión de las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="aec0a-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="aec0a-156">coordIndex indica el número de índice de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="aec0a-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="aec0a-157">Vea [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) y [Coordenadas de textura y Fases de textura.](texture-coordinates.md)</span><span class="sxs-lookup"><span data-stu-id="aec0a-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="aec0a-158">Marcas de máscara</span><span class="sxs-lookup"><span data-stu-id="aec0a-158">Mask Flags</span></span>

<span data-ttu-id="aec0a-159">Las marcas siguientes describen las marcas de máscara usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="aec0a-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="aec0a-160">\#Definir</span><span class="sxs-lookup"><span data-stu-id="aec0a-160">\#define</span></span>                             | <span data-ttu-id="aec0a-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="aec0a-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="aec0a-162">MÁSCARA DE POSICIÓN D3DFVF \_ \_</span><span class="sxs-lookup"><span data-stu-id="aec0a-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="aec0a-163">Máscara para los bits de posición.</span><span class="sxs-lookup"><span data-stu-id="aec0a-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="aec0a-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="aec0a-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="aec0a-165">Enmascara los valores de los bits reservados en FVF.</span><span class="sxs-lookup"><span data-stu-id="aec0a-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="aec0a-166">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="aec0a-166">Do not use.</span></span> |
| <span data-ttu-id="aec0a-167">D3DFVF \_ TEXCOUNT \_ MASK</span><span class="sxs-lookup"><span data-stu-id="aec0a-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="aec0a-168">Valor de máscara para los bits de marca de textura.</span><span class="sxs-lookup"><span data-stu-id="aec0a-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="aec0a-169">Marcas misceláneas</span><span class="sxs-lookup"><span data-stu-id="aec0a-169">Miscellaneous Flags</span></span>

<span data-ttu-id="aec0a-170">Las marcas siguientes describen una variedad de marcas usadas por la canalización de función fija.</span><span class="sxs-lookup"><span data-stu-id="aec0a-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aec0a-171">#Definir</span><span class="sxs-lookup"><span data-stu-id="aec0a-171">#define</span></span></td>
<td><span data-ttu-id="aec0a-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="aec0a-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aec0a-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="aec0a-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="aec0a-174">El último campo beta en los datos de posición del vértice será de tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="aec0a-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="aec0a-175">Los datos de los campos beta se usan con el movimiento de la paleta de matrices para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="aec0a-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aec0a-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="aec0a-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="aec0a-177">El último campo beta de los datos de posición del vértice será de tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="aec0a-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="aec0a-178">Los datos de los campos beta se usan con el movimiento de la paleta de matrices para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="aec0a-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
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

<p><span data-ttu-id="aec0a-179">Dado que la FVF se declara como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="aec0a-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="aec0a-180">Weight y MatrixIndices se incluyen en beta[5], donde D3DFVF_LASTBETA_UBYTE4 indica que interprete el último DWORD en beta[5] como tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="aec0a-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aec0a-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="aec0a-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="aec0a-182">Número de bits por el que se desplaza un valor entero que identifica el número de coordenadas de textura de un vértice.</span><span class="sxs-lookup"><span data-stu-id="aec0a-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="aec0a-183">Este valor se puede usar como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="aec0a-183">This value might be used as shown below.</span></span>
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



 

### <a name="examples"></a><span data-ttu-id="aec0a-184">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aec0a-184">Examples</span></span>

<span data-ttu-id="aec0a-185">En los ejemplos siguientes se muestran otras combinaciones de marcas comunes.</span><span class="sxs-lookup"><span data-stu-id="aec0a-185">The following examples show other common flag combinations.</span></span>


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



## <a name="constant-information"></a><span data-ttu-id="aec0a-186">Información constante</span><span class="sxs-lookup"><span data-stu-id="aec0a-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="aec0a-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aec0a-187">Header</span></span>                   | <span data-ttu-id="aec0a-188">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="aec0a-188">d3d9types.h</span></span> |
| <span data-ttu-id="aec0a-189">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="aec0a-189">Minimum operating system</span></span> | <span data-ttu-id="aec0a-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="aec0a-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="aec0a-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aec0a-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec0a-192">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="aec0a-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="aec0a-193">Códigos FVF de función fija (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aec0a-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="aec0a-194">Combinación de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="aec0a-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 




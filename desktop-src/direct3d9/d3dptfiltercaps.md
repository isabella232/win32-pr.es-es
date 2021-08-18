---
description: Constantes de filtrado de textura.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86645ca1d0f8c1904307b80c27c2b8ce8d635229d3bb15b0f8178d6a9d70dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804673"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Constantes de filtrado de textura.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>El dispositivo admite el filtrado de convolución monocromática. Este filtro se representa mediante el D3DTEXF_CONVOLUTIONMONO del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a> 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>El dispositivo admite el filtrado de muestras de punto por fase para las texturas de aumento. El filtro de ampliación de ejemplo de punto se representa D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>El dispositivo admite el filtrado de interpolación bilineal por fase para la lupa de mapas MIP. El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>El dispositivo admite el filtrado anisotropico por fase para las texturas de aumento. El filtro de ampliación anisotrófica se representa mediante D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>El dispositivo admite el filtrado de muestras piramidales por fase para las texturas de aumento. El filtro de lupa piramidal se representa mediante D3DTEXF_PYRAMIDALQUAD miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>El dispositivo admite el filtrado de quads gaussiano por fase para las texturas de aumento.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>El dispositivo admite el filtrado de muestras de punto por fase para la compresión de texturas. El filtro de minificación de ejemplo de punto se representa D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>El dispositivo admite el filtrado lineal por fase para la compresión de texturas. El filtro de minificación lineal se representa mediante D3DTEXF_LINEAR miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>El dispositivo admite el filtrado anisotropico por fase para la compresión de texturas. El filtro de minificación anisotrófica se representa D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>El dispositivo admite el filtrado de muestras piramidales por fase para la compresión de texturas.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>El dispositivo admite el filtrado de quads gaussiano por fase para la compresión de texturas.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>El dispositivo admite el filtrado de ejemplo de punto por fase para mapas MIP. El filtro mipmapping de ejemplo de punto se representa mediante D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>El dispositivo admite el filtrado de interpolación bilineal por fase para mapas MIP. El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
</tbody>
</table>



 

Estas constantes las usan los miembros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps y VertexTextureFilterCaps de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

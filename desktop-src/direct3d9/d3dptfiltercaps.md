---
description: Constantes de filtrado de texturas.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080284"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Constantes de filtrado de texturas.



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
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>El dispositivo admite el filtrado de circunvolución monocromática. Este filtro se representa mediante el miembro D3DTEXF_CONVOLUTIONMONO del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> . 
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
<td>El dispositivo admite el filtrado de muestra de punto por fase para aumentar las texturas. El filtro de aumento de punto-muestra se representa mediante el D3DTEXF_POINT miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>El dispositivo admite el filtrado de interpolación bilineal por fase para la lupa. El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>El dispositivo admite el filtrado anisotrópico por fase para aumentar las texturas. El filtro de ampliación anisotrópico se representa mediante el D3DTEXF_ANISOTROPIC miembro del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>El dispositivo admite el filtrado de ejemplo pyramidal por fases para aumentar las texturas. El filtro de lupa pyramidal se representa mediante el miembro D3DTEXF_PYRAMIDALQUAD del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>El dispositivo admite el filtrado cuádruple gaussiano de cada fase para aumentar las texturas.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>El dispositivo admite el filtrado de muestra de punto por fase para las texturas de minificar. El filtro minificación de punto-muestra se representa mediante el miembro D3DTEXF_POINT del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>El dispositivo admite el filtrado lineal por fase para las texturas de minificar. El filtro minificación lineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>El dispositivo admite el filtrado anisotrópico por fase para las texturas de minificar. El filtro minificación anisotrópico se representa mediante el miembro D3DTEXF_ANISOTROPIC del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>El dispositivo admite el filtrado de ejemplo pyramidal por fases para las texturas de minificar.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>El dispositivo admite el filtrado cuádruple gaussiano por fase para las texturas de minificar.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>El dispositivo admite el filtrado de muestra de punto por fase para los mapas de bits. El filtro mipmapping de punto-muestra se representa mediante el miembro D3DTEXF_POINT del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>El dispositivo admite el filtrado de interpolación bilineal por fase para los mapas de bits. El filtro mipmapping de interpolación bilineal se representa mediante el miembro D3DTEXF_LINEAR del tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
</tbody>
</table>



 

Estas constantes se utilizan en los miembros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps y VertexTextureFilterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

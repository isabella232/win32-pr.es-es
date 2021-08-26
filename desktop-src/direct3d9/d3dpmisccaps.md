---
description: Marcas de funcionalidad primitiva de controladores varios.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee88ba03b3c0a6d51c0100b20768df4cbf632d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624541"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Marcas de funcionalidad primitiva de controladores varios.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Value</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>El dispositivo puede habilitar y deshabilitar la modificación del búfer de profundidad en las operaciones de píxeles.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>El controlador no realiza la selección de triángulos. Esto corresponde al miembro D3DCULL_NONE del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerado D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>El controlador admite la selección de triángulos en el sentido de las agujas del reloj a través D3DRS_CULLMODE estado. (Esto solo se aplica a las primitivas de triángulo). Esta marca corresponde al miembro D3DCULL_CW del tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>El controlador admite la selección en sentido contrario a las agujas del reloj a través D3DRS_CULLMODE estado. (Esto solo se aplica a las primitivas de triángulo). Esta marca corresponde al miembro D3DCULL_CCW del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerado D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>El dispositivo admite escrituras por canal para el búfer de color de destino de representación a través D3DRS_COLORWRITEENABLE estado.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>El dispositivo recorta correctamente puntos de tamaño mayores que 1,0 a planos de recorte definidos por el usuario.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Clips de dispositivos primitivos de vértices transformados posteriormente. Especifique D3DUSAGE_DONOTCLIP cuando la canalización no debe realizar ningún recorte. En este caso, puede que sea necesario realizar un recorte de software adicional en tiempo de dibujo, lo que requiere que el búfer de vértices esté en la memoria del sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>El dispositivo admite <a href="d3dta.md">D3DTA para</a> el registro temporal.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>El dispositivo admite operaciones de mezcla alfa que no son D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Un dispositivo de referencia que no se representa.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>El dispositivo admite máscaras de escritura independientes para varias texturas de elementos o varios destinos de representación.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>El dispositivo admite constantes por fase. Vea D3DTSS_CONSTANT en <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>El dispositivo admite la conversión a sRGB después de la mezcla. 
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
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>El dispositivo admite caracteres alfa especulares y independientes. Muchos dispositivos usan el canal alfa especular para almacenar el factor de crecimiento.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>El dispositivo admite la configuración de mezcla independiente para el canal alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>El dispositivo admite diferentes profundidades de bits para varios destinos de representación.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>El dispositivo admite operaciones de sombreador posterior a píxeles para varios destinos de representación.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>El dispositivo fija el factor de fusión por vértice.</td>
</tr>
</tbody>
</table>



 

El miembro PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



| Requisito                         |  Value          |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

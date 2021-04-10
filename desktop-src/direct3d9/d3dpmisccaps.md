---
description: Marcas de capacidad primitiva del controlador varias.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275044"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Marcas de capacidad primitiva del controlador varias.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#define</td>
<td>Value</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>El dispositivo puede habilitar y deshabilitar la modificación del búfer de profundidad en operaciones de píxeles.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>El controlador no realiza la selección de triángulos. Esto corresponde al miembro D3DCULL_NONE del tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>El controlador admite la selección del triángulo en el sentido de las agujas del reloj a través del estado D3DRS_CULLMODE. (Esto solo se aplica a los primitivos triangulares). Esta marca corresponde al miembro D3DCULL_CW del tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>El controlador admite la selección en sentido contrario a las agujas del reloj a través del estado D3DRS_CULLMODE. (Esto solo se aplica a los primitivos triangulares). Esta marca corresponde al miembro D3DCULL_CCW del tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>El dispositivo admite las escrituras por canal para el búfer de color de destino de representación a través del estado de D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>El dispositivo recorta correctamente los puntos de tamaño de escala superior a 1,0 a los planos de recorte definidos por el usuario.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Clips del dispositivo elementos primitivos de vértices posteriores transformados. Especifique D3DUSAGE_DONOTCLIP cuando la canalización no debe realizar ningún recorte. En este caso, es posible que sea necesario realizar un recorte de software adicional en el momento de la operación de dibujo, lo que requiere que el búfer de vértices esté en la memoria del sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>El dispositivo admite <a href="d3dta.md">D3DTA</a> para el registro temporal.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>El dispositivo admite operaciones de combinación alfa distintas de D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Un dispositivo de referencia que no se representa.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>El dispositivo admite máscaras de escritura independientes para varias texturas de elemento o varios destinos de representación.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>El dispositivo admite constantes por fase. Consulte D3DTSS_CONSTANT en <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>El dispositivo admite la conversión a sRGB después de la fusión. 
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
<td>El dispositivo admite la niebla independiente y el alfa especular. Muchos dispositivos usan el canal alfa especular para almacenar el factor de niebla.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>El dispositivo es compatible con la configuración de Blend independiente para el canal alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>El dispositivo admite diferentes profundidades de bits para varios destinos de representación.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>El dispositivo admite operaciones de sombreador de postpíxel para varios destinos de representación.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Factor de mezcla de niebla de abrazadera de dispositivo por vértice.</td>
</tr>
</tbody>
</table>



 

El miembro PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

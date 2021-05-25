---
description: Marcas de funcionalidad del controlador.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda81aa7f77dcaf03eb06b357ebfb91b4956f6d4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343370"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Marcas de funcionalidad del controlador.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Valor</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Indica que el dispositivo puede respetar el estado D3DRS_ALPHABLENDENABLE representación en modo de pantalla completa mientras se usa el efecto de intercambio FLIP o DISCARD. Esto solo se aplica cuando los estados D3DRS_SRCBLEND o D3DRS_DESTBLEND están establecidos en uno de los siguientes:
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>El dispositivo puede acelerar una copia de memoria de la memoria del sistema a la memoria de vídeo local. Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas UpdateSurface</strong></a> <a href="/windows/desktop/api"><strong>y UpdateTexture</strong></a> se acelerarán por hardware. Si este límite no está presente, estas llamadas se realizarán correctamente, pero serán más lentas.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>El dispositivo puede acelerar una copia de memoria de la memoria de vídeo local a la memoria del sistema. Este límite garantiza que las <a href="/windows/desktop/api"><strong>llamadas a GetRenderTargetData</strong></a> se acelerarán por hardware. Si este límite no está presente, esta llamada se realizará correctamente, pero será más lenta.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>El controlador de pantalla admite el DDI DXVA-HD. Para obtener más información sobre DXVA-HD DDI, vea <a href="https://msdn.microsoft.com/library/dd835176.aspx">Processing High-Definition Video</a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>Indica que el dispositivo puede realizar la corrección gamma desde un búfer de reserva con ventanas (que contiene contenido lineal) a un escritorio sRGB.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Reservado; no se usa.</td>
</tr>
</tbody>
</table>



 

El miembro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 





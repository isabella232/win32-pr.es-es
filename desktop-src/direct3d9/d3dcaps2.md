---
description: Consulte una lista de marcas de funcionalidad del controlador D3DCAPS2. Incluye las definiciones, los valores y las descripciones con vínculos a las API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adada1f5e38247482af38cd335c6fd719cf9a603
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627711"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Marcas de funcionalidad del controlador.



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
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>El controlador es capaz de generar automáticamente mapas MIP. Para obtener más información, vea Generación automática de <a href="automatic-generation-of-mipmaps.md">mapas Mip (Direct3D 9).</a></td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>El sistema tiene instalado un calibrador que puede ajustar automáticamente la rampa gamma para que el resultado sea idéntico en todos los sistemas que tienen un calibrador. Para invocar el calibrador al establecer nuevos niveles gamma, use la D3DSGR_CALIBRATE al llamar a <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>. La calibración de las rampas gamma incurre en cierta sobrecarga de procesamiento y no se debe usar con frecuencia.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>El dispositivo puede crear recursos que se pueden compartir. Los métodos que crean recursos pueden establecer valores que no son NULL para sus <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>parámetros pSharedHandle.</strong></a> 
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
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>El controlador es capaz de administrar recursos. En estos controladores, D3DPOOL_MANAGED recursos administrados por el controlador. Para que Direct3D invalide el controlador para que Direct3D administre los recursos, use la marca D3DCREATE_DISABLE_DRIVER_MANAGEMENT al llamar <a href="/windows/desktop/api"><strong>a CreateDevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>El controlador admite texturas dinámicas.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>El controlador admite el ajuste dinámico de la rampa gamma en modo de pantalla completa.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Reservado; no se usa.</td>
</tr>
</tbody>
</table>



 

El miembro D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|  Requisito                        | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

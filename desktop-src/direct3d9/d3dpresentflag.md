---
description: Constantes usadas por \_ los parámetros D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705287"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Constantes usadas por [**\_ los parámetros D3DPRESENT**](d3dpresent-parameters.md).



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
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Recortar un blit de <a href="/windows/desktop/api"><strong>presentación</strong></a> de ventana en el área de cliente de la ventana, dentro del área de pantalla monitor del adaptador de vídeo que creó el dispositivo Direct3D. D3DPRESENTFLAG_DEVICECLIP no es válido con D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Establezca esta marca cuando se cree el dispositivo o la cadena de intercambio para habilitar la descartación del búfer z. Si se establece esta marca, el contenido del búfer de estarcido de profundidad no será válido después de llamar a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente. Descartar los datos del búfer z puede aumentar el rendimiento y depende del controlador. El tiempo de ejecución de depuración exigirá el descarting al borrar el búfer z en algún valor constante después de llamar a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.<br/> Descartar los datos del búfer z no es válido para todos los formatos de bloqueos, D3DFMT_D16_LOCKABLE y D3DFMT_D32F_LOCKABLE. Cualquier uso de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> que especifique un formato de bloqueable y un descartado de búfer z producirá un error. Para obtener más información acerca de los formatos, vea <a href="d3dformat.md">D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Establezca esta marca si la aplicación requiere la capacidad de bloquear el búfer de reserva directamente. Tenga en cuenta que los búferes de reserva no se pueden bloquear a menos que la aplicación especifique D3DPRESENTFLAG_LOCKABLE_BACKBUFFER al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>RESET</strong></a>. Los búferes de reserva que se bloquean incurren en un costo de rendimiento en algunas configuraciones de hardware de gráficos. La realización de una operación de bloqueo (o el uso de <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> para escribir) en el búfer de reserva de bloqueos reduce el rendimiento en muchas tarjetas. En este caso, considere la posibilidad de usar triángulos con textura para trasladar datos al búfer de reserva.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> En Direct3D9Ex no se puede establecer esta marca si el valor de D3DSWAPEFFECT es D3DSWAPEFFECT_FLIPEX, ya que el modelo de volteo permite al Administrador de ventanas de escritorio tener acceso al búfer de reserva de una aplicación. Una superficie compartida entre procesos no debe estar bloqueada.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Los monitores girados se controlan automáticamente con una copia giratoria durante la presentación, lo que no es muy eficaz. Esta marca significa que la aplicación realizará su propia rotación de pantalla. 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Las aplicaciones pueden lograr su propia rotación posiblemente mediante una matriz de vistas girada. Los métodos <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> deben usarse para buscar el valor de rotación actual. Los parámetros de ancho y alto del búfer de reserva de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> deben usar la orientación horizontal, mientras que la estructura del modo de presentación de pantalla completa debe ser la misma que la devuelta desde <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (es decir, el ancho y el alto se intercambian cuando giran 90 y 270 grados).</p>
<p>Cuando se usa el bloqueo en destinos de representación girados, las suposiciones de la esquina superior izquierda ya no tienen el valor true, el destino de representación SURFACE_DESC permanecerá horizontal (como lo implican los parámetros de creación) y la ventana de GDI, las coordenadas del mouse, y tal necesidad de traducirse correctamente cuando se usa con el destino de representación y la escena de Direct3D.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Use esta marca para especificar cualquier modo de presentación sin formato enumerado por el adaptador de pantalla, aunque Direct3D haya indicado que el modo no es válido. La aplicación debe implementar esto de forma sólida en caso de que el modo deseado realmente no sea válido. 
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
<td>D3DPRESENTFLAG_VIDEO</td>
<td>0x00000010</td>
<td>Esta es una sugerencia para el controlador que los búferes de reserva contendrán datos de vídeo.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Especifica si la superposición es RGB de intervalo completo o de intervalo limitado. Al establecer esta marca, se indica RGB de intervalo limitado. En el intervalo de RGB limitado, el intervalo RGB se comprime de forma que 16:16:16 sea negro y 235:235:235 sea blanco.
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</td>
<td>0x00000100</td>
<td>Especifica si la superposición es BT. 601 o BT. 709. La configuración de esta marca indica BT. 709, para TV de alta definición (HDTV).
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
<td>D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</td>
<td>0x00000200</td>
<td>Especifica si la superposición es el YCbCr convencional o la extensión YCbCr extendida (xvYCC). Al establecer esta marca, se indica el YCbCr extendido (xvYCC).
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
<td>D3DPRESENTFLAG_RESTRICTED_CONTENT</td>
<td>0x00000400</td>
<td>Al establecer esta marca, se indica que intercambio contiene contenido protegido y hace que el tiempo de ejecución restrinja automáticamente el acceso a intercambio para que solo el administrador de Windows de escritorio (DWM) pueda usar intercambio.
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
<td>D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</td>
<td>0x00000800</td>
<td>Al establecer esta marca, se indica que el controlador debe restringir el acceso a los recursos compartidos que se crean para la interacción de DWM. El autor de la llamada debe crear un canal autenticado con el controlador. A continuación, el controlador debe permitir el acceso a los procesos que intenten abrir esos recursos compartidos.
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

[**\_ Los parámetros D3DPRESENT**](d3dpresent-parameters.md)usan estas constantes.

## <a name="constant-information"></a>Información constante



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3d9types. h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 





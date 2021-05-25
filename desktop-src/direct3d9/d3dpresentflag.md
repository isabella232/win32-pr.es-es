---
description: Constantes usadas por D3DPRESENT \_ PARAMETERS.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578d41119980719e69b9eb0e502c025414018f73
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343100"
---
# <a name="d3dpresentflag"></a>D3DPRESENTFLAG

Constantes utilizadas por [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).



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
<td>D3DPRESENTFLAG_DEVICECLIP</td>
<td>0x00000004</td>
<td>Recorte una ventana <a href="/windows/desktop/api"><strong>Presente</strong></a> blit en el área de cliente de la ventana, dentro del área de pantalla del monitor del adaptador de vídeo que creó el dispositivo Direct3D. D3DPRESENTFLAG_DEVICECLIP no es válido con D3DSWAPEFFECT_FLIPEX.</td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</td>
<td>0x00000002</td>
<td>Establezca esta marca cuando se cree el dispositivo o la cadena de intercambio para habilitar el descarte de búfer z. Si se establece esta marca, el contenido del búfer de galería de símbolos de profundidad no será válido después de llamar a <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente. Descartar los datos del búfer z puede aumentar el rendimiento y depende del controlador. El tiempo de ejecución de depuración aplicará el descarte borrando el búfer z en algún valor constante después de llamar a <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.<br/> Descartar los datos del búfer z no es posible para todos los formatos que se pueden bloquear, D3DFMT_D16_LOCKABLE y D3DFMT_D32F_LOCKABLE. Se producirá un error en cualquier uso <a href="/windows/desktop/api"><strong>de CreateDevice</strong></a> que especifique un formato que se puede bloquear y el descarte del búfer z. Para obtener más información sobre los formatos, <a href="d3dformat.md">vea D3DFORMAT</a>.<br/></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</td>
<td>0x00000001</td>
<td>Establezca esta marca si la aplicación requiere la capacidad de bloquear el búfer de reserva directamente. Tenga en cuenta que los búferes de reserva no se pueden bloquear a menos que la aplicación D3DPRESENTFLAG_LOCKABLE_BACKBUFFER al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>Restablecer</strong></a>. Los búferes de reserva que se pueden bloquear incurren en un costo de rendimiento en algunas configuraciones de hardware gráfico. La realización de una operación de bloqueo (o el uso <a href="/windows/desktop/api"><strong>de UpdateSurface</strong></a> para escribir) en el búfer de reserva que se puede bloquear reduce el rendimiento en muchas tarjetas. En este caso, considere la posibilidad de usar triángulos con textura para mover datos al búfer de reserva.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> En Direct3D9Ex, esta marca no se puede establecer si D3DSWAPEFFECT es D3DSWAPEFFECT_FLIPEX, ya que el modelo de volteo permite que el Administrador de ventanas de escritorio acceda al búfer de reserva de una aplicación. No se debe bloquear una superficie compartida entre procesos.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPRESENTFLAG_NOAUTOROTATE</td>
<td>0x00000020</td>
<td>Los monitores girados se controlan automáticamente con una copia rotativa durante la presentación, lo que no es muy eficaz. Esta marca significa que la aplicación realizará su propia rotación de pantalla. 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p>Las aplicaciones pueden lograr su propia rotación posiblemente mediante una matriz de vista girada. Los <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>métodos GetDisplayModeEx</strong></a> <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>y GetAdapterDisplayModeEx</strong></a> deben usarse para buscar la configuración de rotación actual. Los parámetros Ancho y Alto del búfer de reserva de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> deben usar orientación horizontal, mientras que la estructura del modo de presentación de pantalla completa debe ser la misma que la que se devuelve de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (es decir, el ancho y el alto se intercambian cuando se giran 90 y 270 grados).</p>
<p>Cuando se usa Bloquear en destinos de representación girados, las suposiciones de la esquina superior izquierda ya no son verdaderas, el destino de representación SURFACE_DESC permanecerá horizontal (como implícito en los parámetros de creación) y la ventana GDI, las coordenadas del mouse y tales deben traducirse correctamente cuando se usen con el destino y la escena de representación de Direct3D.</p></td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_UNPRUNEDMODE</td>
<td>0x00000040</td>
<td>Use esta marca para especificar cualquier modo de presentación RAW enumerado por el adaptador de pantalla, aunque Direct3D pueda haber indicado que el modo no es válido. La aplicación debe implementar esto de una manera sólida en caso de que el modo deseado no sea realmente válido. 
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
<td>Se trata de una sugerencia para el controlador de que los búferes de reserva contendrán datos de vídeo.</td>
</tr>
<tr class="even">
<td>D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</td>
<td>0x00000080</td>
<td>Especifica si la superposición es RGB de intervalo completo o RGB de intervalo limitado. Establecer esta marca indica un intervalo rgb limitado. En el rango limitado RGB, el intervalo RGB se comprime de forma que 16:16:16 es negro y 235:235:235 es blanco.
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
<td>Especifica si la superposición es BT.601 o BT.709. Si se establece esta marca, se indica BT.709, para televisión de alta definición (BT).
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
<td>Especifica si la superposición es YCbCr convencional o YCbCr extendido (sipYCC). Si se establece esta marca, se indica el YCbCr extendido (sipYCC).
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
<td>Establecer esta marca indica que la cadena de intercambio contiene contenido protegido y hace que el tiempo de ejecución restrinja automáticamente el acceso a la cadena de intercambio para que solo el Administrador de Escritorio de Windows (DWM) pueda usar la cadena de intercambio.
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
<td>Establecer esta marca indica que el controlador debe restringir el acceso a los recursos compartidos que se crean para la interacción de DWM. El autor de la llamada debe crear un canal autenticado con el controlador. A continuación, el controlador debe permitir el acceso a los procesos que intentan abrir esos recursos compartidos.
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



 

D3DPRESENT PARAMETERS usa estas [**\_ constantes.**](d3dpresent-parameters.md)

## <a name="constant-information"></a>Información constante



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3d9types.h |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 





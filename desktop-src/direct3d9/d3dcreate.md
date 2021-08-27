---
description: Vea una combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo en la constante D3DCREATE.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09cfd220e3fae2af079ba4eceba8f820a9267b4d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630233"
---
# <a name="d3dcreate"></a>D3DCREATE

Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Descripción</td>
</tr>
<tr class="even">
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>La aplicación pide al dispositivo que controle todas las caras que posee este adaptador maestro. La marca no es posible en adaptadores no maestros. Si se establece esta marca, los parámetros de presentación pasados a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> deben apuntar a una matriz <a href="d3dpresent-parameters.md"><strong>de D3DPRESENT_PARAMETERS</strong></a>. El número de elementos <strong>D3DPRESENT_PARAMETERS</strong> debe ser igual al número de adaptadores definido por el miembro NumberOfAdaptersInGroup de la <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>estructura D3DCAPS9.</strong></a> El tiempo de ejecución de DirectX asignará cada elemento a cada cabeza en el orden numérico especificado por el miembro AdapterOrdinalInGroup <strong>de D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D administrará los recursos en lugar del controlador. Las llamadas de Direct3D no producirán errores en los recursos, como memoria de vídeo insuficiente.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Al D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D administrará los recursos en lugar del controlador. A D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX devolverá errores para condiciones como memoria de vídeo insuficiente.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Hace que el tiempo de ejecución no registre las teclas de acceso rápido para Printscreen, Ctrl-Printscreen y Alt-Printscreen capturar el contenido del escritorio o la ventana. 
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
<td>D3DCREATE_DISABLE_PSGP_THREADING</td>
<td>Restrinja el cálculo al subproceso de aplicación principal. Si no se establece la marca, el tiempo de ejecución puede realizar el procesamiento de vértices de software y otros cálculos en el subproceso de trabajo para mejorar el rendimiento en sistemas de varios procesadores. 
<table>
<tbody>
<tr class="odd">
<td>Diferencias entre Windows XP y Windows Vista:<br/> Esta marca está disponible en Windows Vista, Windows Server 2008 y Windows 7.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DCREATE_ENABLE_PRESENTSTATS</td>
<td>Habilita la recopilación de estadísticas actuales en el dispositivo. Las llamadas <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>a GetPresentStatistics</strong></a> devolverán datos válidos. 
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
<td>D3DCREATE_FPU_PRESERVE</td>
<td>Establezca la precisión de los cálculos de punto flotante de Direct3D en la precisión utilizada por el subproceso que realiza la llamada. Si no especifica esta marca, Direct3D tiene como valor predeterminado el modo round-to-nearest de precisión sencilla por dos motivos:
<ul>
<li>El modo de doble precisión reducirá el rendimiento de Direct3D.</li>
<li>Las partes de Direct3D suponen que las excepciones de unidad de punto flotante están enmascaradas; la desenmascaramiento de estas excepciones puede dar lugar a un comportamiento indefinido.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices de hardware.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices mixtos (tanto de software como de hardware). Por Windows 10, versión 1607 y posteriores, no se recomienda usar esta configuración. Consulte D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices de software. Por Windows 10, versión 1607 y posteriores, no se recomienda usar esta configuración. Use D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
A menos que el procesamiento de vértices de hardware no esté disponible, no se recomienda el uso del procesamiento de vértices de software en Windows 10, versión 1607 (y versiones posteriores) porque la eficacia del procesamiento de vértices de software se redujo significativamente al mejorar la seguridad de la implementación.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indica que la aplicación solicita que Direct3D sea seguro para multiproceso. Esto hace que un subproceso de Direct3D tome posesión de su sección <a href="/windows/desktop/Sync/critical-section-objects">crítica</a> global con más frecuencia, lo que puede degradar el rendimiento. Si una aplicación procesa mensajes de ventana en un subproceso mientras realiza llamadas API de Direct3D en otro, la aplicación debe usar esta marca al crear el dispositivo. Esta ventana también debe destruirse antes de descargar d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indica que Direct3D no debe modificar la ventana de foco de ninguna manera.
<div class="alert">
<blockquote>
[!Note]<br />
Si se establece esta marca, la aplicación debe admitir completamente todos los eventos de administración de foco, como ALT+TAB y eventos de clic del mouse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Especifica que Direct3D no admite llamadas Get* para todo lo que se puede almacenar en bloques de estado. También indica a Direct3D que no proporcione ningún servicio de emulación para el procesamiento de vértices. Esto significa que si el dispositivo no admite el procesamiento de vértices, la aplicación solo puede usar vértices posteriores a la transformación.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Permite protectores de pantalla durante una aplicación de pantalla completa. Sin esta marca, Direct3D deshabilitará los protectores de pantalla mientras la aplicación que realiza la llamada sea de pantalla completa. Si la aplicación que realiza la llamada ya es un protector de pantalla, esta marca no tiene ningún efecto. 
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



 

D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING, D3DCREATE \_ MIXED VERTEXPROCESSING y \_ D3DCREATE SOFTWARE VERTEXPROCESSING son marcas \_ \_ mutuamente excluyentes. Al menos una de estas marcas de procesamiento de vértices debe especificarse al llamar a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).

## <a name="constant-information"></a>Información constante



| Requisito                         |  Value          |
|--------------------------|------------|
| Encabezado                   | D3D9.h     |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

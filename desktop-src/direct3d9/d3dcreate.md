---
description: Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000701"
---
# <a name="d3dcreate"></a>D3DCREATE

Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.



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
<td>D3DCREATE_ADAPTERGROUP_DEVICE</td>
<td>La aplicación pide al dispositivo que controle todos los dispositivos que posee este adaptador maestro. La marca no es válida en los adaptadores no maestros. Si se establece esta marca, los parámetros de presentación que se pasan a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> deben apuntar a una matriz de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>. El número de elementos de <strong>D3DPRESENT_PARAMETERS</strong> debe ser igual al número de adaptadores definido por el miembro NumberOfAdaptersInGroup de la estructura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> . El tiempo de ejecución de DirectX asignará cada elemento a cada encabezado en el orden numérico especificado por el miembro AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT</td>
<td>Direct3D administrará los recursos en lugar del controlador. No se producirá un error en las llamadas de Direct3D para los errores de recursos, como la memoria de vídeo insuficiente.</td>
</tr>
<tr class="even">
<td>D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</td>
<td>Como D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D administrará los recursos en lugar del controlador. A diferencia de D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX devolverá errores para condiciones como la memoria de vídeo insuficiente.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_DISABLE_PRINTSCREEN</td>
<td>Hace que el tiempo de ejecución no registre las teclas de PrintScreen, Ctrl-Printscreen y Alt-Printscreen para capturar el escritorio o el contenido de la ventana. 
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
<td>Restrinja el cálculo al subproceso de la aplicación principal. Si no se establece la marca, el runtime puede realizar el procesamiento de vértices de software y otros cálculos en el subproceso de trabajo para mejorar el rendimiento en sistemas de varios procesadores. 
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
<td>Habilita la recopilación de estadísticas presentes en el dispositivo. Las llamadas a <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> devolverán datos válidos. 
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
<td>Establezca la precisión para los cálculos de punto flotante de Direct3D en la precisión utilizada por el subproceso que realiza la llamada. Si no se especifica esta marca, Direct3D toma como valor predeterminado el modo de redondeo de precisión sencilla por dos motivos:
<ul>
<li>El modo de doble precisión reducirá el rendimiento de Direct3D.</li>
<li>Algunas partes de Direct3D suponen que las excepciones de la unidad de punto flotante se enmascaran; al desenmascarar estas excepciones, se puede producir un comportamiento indefinido.</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCREATE_HARDWARE_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices de hardware.</td>
</tr>
<tr class="even">
<td>D3DCREATE_MIXED_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices mixtos (tanto de software como de hardware). En Windows 10, versión 1607 y versiones posteriores, no se recomienda el uso de esta configuración. Vea D3DCREATE_SOFTWARE_VERTEXPROCESSING.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SOFTWARE_VERTEXPROCESSING</td>
<td>Especifica el procesamiento de vértices de software. En Windows 10, versión 1607 y versiones posteriores, no se recomienda el uso de esta configuración. Use D3DCREATE_HARDWARE_VERTEXPROCESSING.
<div class="alert">
<blockquote>
[!Note]<br />
A menos que no esté disponible el procesamiento de vértices de hardware, no se recomienda el uso del procesamiento de vértices de software en Windows 10, versión 1607 (y versiones posteriores), ya que la eficacia del procesamiento de vértices de software se redujo considerablemente al mejorar la seguridad de la implementación.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_MULTITHREADED</td>
<td>Indica que la aplicación solicita a Direct3D que sea segura para subprocesos. Esto hace que un subproceso de Direct3D tome posesión de su <a href="/windows/desktop/Sync/critical-section-objects">sección crítica</a> global con mayor frecuencia, lo que puede reducir el rendimiento. Si una aplicación procesa los mensajes de ventana en un subproceso mientras realiza llamadas a la API de Direct3D en otro, la aplicación debe usar esta marca al crear el dispositivo. Esta ventana también se debe destruir antes de descargar d3d9.dll.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_NOWINDOWCHANGES</td>
<td>Indica que Direct3D no debe modificar la ventana de foco de ningún modo.
<div class="alert">
<blockquote>
[!Note]<br />
Si se establece esta marca, la aplicación debe admitir todos los eventos de administración de foco, como ALT + TAB y eventos de clic del mouse.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td>D3DCREATE_PUREDEVICE</td>
<td>Especifica que Direct3D no admite llamadas Get * para cualquier elemento que se pueda almacenar en bloques de estado. También indica a Direct3D que no proporcione ningún servicio de emulación para el procesamiento de vértices. Esto significa que si el dispositivo no admite el procesamiento de vértices, la aplicación solo puede usar vértices posteriores transformados.</td>
</tr>
<tr class="odd">
<td>D3DCREATE_SCREENSAVER</td>
<td>Permite protectores de pantalla durante una aplicación de pantalla completa. Sin esta marca, Direct3D deshabilitará los protectores de pantalla mientras la aplicación que realiza la llamada sea pantalla completa. Si la aplicación que realiza la llamada ya es un protector de la aplicación, esta marca no tiene ningún efecto. 
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



 

D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING y D3DCREATE \_ software \_ VERTEXPROCESSING son marcas mutuamente excluyentes. Se debe especificar al menos una de estas marcas de procesamiento de vértices al llamar a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | D3D9. h     |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 

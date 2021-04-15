---
description: Describe la relación entre la frecuencia de actualización del adaptador y la velocidad a la que se completan las operaciones presentes o presentes. Estos valores también sirven como valores de marca para el campo PresentationIntervals de D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b8bf496c8c8e10d50b23ad4f784634fb983d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707932"
---
# <a name="d3dpresent"></a>D3DPRESENT

Describe la relación entre la frecuencia de actualización del adaptador y la velocidad a la que se completan las operaciones [**presentes**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) o [**presentes**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) . Estos valores también sirven como valores de marca para el campo PresentationIntervals de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTFLIP"></span><span id="d3dpresent_donotflip"></span><dl> <dt><strong>D3DPRESENT_DONOTFLIP</strong></dt> </dl></td>
<td style="text-align: left;">Use el búfer frontal como la superficie de origen y de destino durante la representación. Se programa una sincronización de fotogramas, pero la superficie mostrada no cambia. Esta marca solo está disponible cuando la aplicación está en modo de pantalla completa y se ha especificado D3DSWAPEFFECT_FLIPEX. <br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Un dispositivo Hal no puede programar una presentación. Si esta marca se establece en una llamada a <a href="/windows/desktop/api"><strong>present</strong></a>y el hardware está ocupado procesando o esperando un intervalo de sincronización vertical, entonces present devolverá D3DERR_WASSTILLDRAWING para indicar que la operación de blit está incompleta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Reservado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE se aplica en esta llamada <a href="/windows/desktop/api"><strong>actual</strong></a> . Esta marca solo se puede especificar cuando se usa D3DSWAPEFFECT_FLIPEX. Los comportamientos de presentación con ventanas y de pantalla completa son los mismos. Esto es especialmente útil para las aplicaciones multimedia que desean descartar fotogramas detectados en tiempo de espera y presentan fotogramas posteriores en el momento de la composición. Si esta marca no se especifica correctamente, se devolverá un error de parámetro no válido. Cuando se ponen en cola varios marcos consecutivos con D3DPRESENT_FORCEIMMEDIATEs, solo se muestra el último fotograma, para la presentación en ventanas y en pantalla completa.<br/> Esta marca está disponible en Direct3D 9Ex en Windows 7 o sistemas operativos posteriores.<br/> Cuando se usa D3DSWAPEFFECT_FLIPEX, cada fotograma presentado mediante D3DPRESENT_INTERVAL_IMMEDIATE o D3DPRESENT_INTERVAL_FORCEIMMEDIATE invalidará el intervalo actual del fotograma anterior. Por ejemplo, si pone en cola los fotogramas siguientes con los siguientes efectos de intercambio: el marco A (D3DPRESENT_INTERVAL_ONE), el marco B (D3DPRESENT_INTERVAL_ONE), el marco C (D3DPRESENT_INTERVAL_ONE), el marco D (D3DPRESENT_INTERVAL_FORCEIMMEDIATE), el marco D invalidará el intervalo presente del marco C. Los fotogramas mostrados por intervalo actual son el marco A, el marco B, (marco C invalidado por) fotograma D.<br/> Vea la sección Comentarios.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Es casi equivalente a D3DPRESENT_INTERVAL_ONE. Vea Notas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">El controlador esperará el período de reseguimiento vertical (el tiempo de ejecución hará que se produzca el &quot; siguiente paso &quot; para evitar el desgarro). Las operaciones <a href="/windows/desktop/api"><strong>presentes</strong></a> no se verán afectadas con mayor frecuencia que la actualización de la pantalla. el tiempo de ejecución completará como máximo una operación de presentación por cada período de actualización del adaptador. Esto es equivalente a usar D3DSWAPEFFECT_COPYVSYNC en DirectX 8,1. Esta opción siempre está disponible para las cadenas de intercambio en ventanas y de pantalla completa. Vea Notas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">El controlador esperará el período de reseguimiento vertical. Las operaciones <a href="/windows/desktop/api"><strong>presentes</strong></a> no se verán afectadas con mayor frecuencia que cada segunda actualización de la pantalla. Compruebe el límite de PresentationIntervals (consulte <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver si el controlador admite D3DPRESENT_INTERVAL_TWO.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">El controlador esperará el período de reseguimiento vertical. Las operaciones <a href="/windows/desktop/api"><strong>presentes</strong></a> no se verán afectadas con mayor frecuencia que cada actualización de la tercera pantalla. Compruebe el límite de PresentationIntervals (consulte <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver si el controlador admite D3DPRESENT_INTERVAL_THREE.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">El controlador esperará el período de reseguimiento vertical. Las operaciones <a href="/windows/desktop/api"><strong>presentes</strong></a> no se verán afectadas con mayor frecuencia que cada cuarta actualización de pantalla. Compruebe el miembro PresentationIntervals (vea <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver si el controlador admite D3DPRESENT_INTERVAL_FOUR.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">El tiempo de ejecución actualiza el área cliente de la ventana inmediatamente y podría hacerlo más de una vez durante el período de actualización del adaptador. Esto es equivalente a usar D3DSWAPEFFECT_COPY en DirectX 8. Las operaciones de <a href="/windows/desktop/api"><strong>presentación</strong></a> pueden verse afectadas de inmediato. Esta opción siempre está disponible para las cadenas de intercambio en ventanas y de pantalla completa. Vea Notas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">El contenido del búfer de reserva que se va a presentar está en el espacio de colores lineal. <br/>
<ul>
<li>La presentación se convertirá implícitamente del espacio lineal al sRGB (gamma = 2,2). Esta es la única conversión que se admite.</li>
<li>Dado que esta marca representa una propiedad del contenido del búfer de reserva, la marca se puede especificar durante una llamada a <a href="/windows/desktop/api"><strong>present</strong></a> . En otras palabras, una aplicación puede presentar contenido lineal en un marco y, a continuación, cambiar al contenido corregido en el siguiente.</li>
<li>Esta marca se omite cuando la cadena de intercambio es de pantalla completa. (Tenga en cuenta que esta marca solo está disponible en la versión de la cadena de intercambio explícita de <a href="/windows/desktop/api"><strong>presente</strong></a>. El método <a href="/windows/desktop/api"><strong>present</strong></a> no toma un parámetro flags.)</li>
<li>Esta marca siempre se acepta, pero solo se aplica cuando el controlador expone >D3DCAPS3_LINEAR_TO_SRGB_PresentATION.</li>
<li>El único formato de búfer de reserva admitido es <a href="d3dformat.md">X8R8G8B8</a>.</li>
</ul>
Consulte <a href="gamma.md">cadenas de intercambio en ventanas</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Recorta el contenido representado al monitor o dispositivo al que se dirige el adaptador, muestra las miniaturas del contenido de la vista Flip3D y las miniaturas de la barra de tareas en otros monitores. <br/> Esta marca solo está disponible en Direct3D 9Ex.<br/> Consulte <a href="/windows/desktop/dwm/dwm-overview">Administrador de ventanas de escritorio</a> para obtener más detalles sobre esta característica de Windows Vista. Si no se está ejecutando en el modo de composición de escritorio, la marca proporciona el mismo comportamiento que <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>.<br/>
<blockquote>
[!Note]<br />
Esta marca solo se debe usar con el efecto de intercambio D3DSWAPEFFECT_FLIPEX. El uso de esta marca con <em>otros</em> efectos de intercambio está en desuso y es posible que no funcione en versiones futuras de Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Actualiza la posición de superposición o los datos de Colorkey sin producir un volteo real y sin cambiar la duración con la que se muestra la imagen.<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Desactiva el hardware de superposición.<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Vuelve a dibujar los datos de Colorkey.<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Observaciones

El modo de ventana admite el intervalo \_ \_ de D3DPRESENT predeterminado, D3DPRESENT \_ Interval \_ Immediate y D3DPRESENT \_ Interval \_ uno. D3DPRESENT \_ Interval \_ default y el \_ intervalo D3DPRESENT \_ son casi equivalentes (consulte la información relativa a la resolución del temporizador a continuación). Funcionan de forma similar para copiar \_ VSYNC en el que solo hay un presente por fotograma y evitan el desgaste con el cruce. Por el contrario, el \_ intervalo inmediato de D3DPRESENT \_ intentará proporcionar una velocidad de presentación ilimitada.

El modo de pantalla completa admite un uso similar como modo de ventana mediante \_ la compatibilidad con \_ el intervalo de D3DPRESENT inmediato, independientemente de la frecuencia de actualización o el efecto de intercambio. El \_ valor predeterminado del intervalo D3DPRESENT \_ usa la resolución predeterminada del temporizador del sistema, mientras que el \_ intervalo D3DPRESENT \_ llama a [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) para mejorar la resolución del temporizador del sistema. Esto mejora la calidad de la sincronización vertical, pero consume un tiempo de procesamiento ligeramente mayor. Ambos parámetros intentan sincronizarse verticalmente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9. h</dt> </dl> |

## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)

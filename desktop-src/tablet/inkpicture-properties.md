---
description: Esta sección contiene propiedades para el control InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propiedades de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817726"
---
# <a name="inkpicture-properties"></a>Propiedades de InkPicture

Esta sección contiene propiedades para el control InkPicture.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw (propiedad)</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> se vuelve a dibujar cuando se invalida la ventana (si el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> asociado actualmente al control InkPicture se vuelve a dibujar automáticamente cuando la ventana asociada a inkpicture recibe un mensaje WM_PAINT).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></td>
<td>Obtiene o establece el color de fondo del control <a href="inkpicture-control-reference.md">InkPicture</a> . El color de fondo predeterminado es el color de fondo de la ventana del sistema, que suele ser blanco.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Propiedad CollectingInk</strong></a></td>
<td>Obtiene el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> está recopilando la entrada de lápiz (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>Si CollectionMode es</strong></a></td>
<td>Obtiene o establece el modo de recopilación que determina si se reconocen la tinta, los gestos o la entrada de lápiz y los gestos a medida que el usuario escribe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursor (propiedad)</strong></a></td>
<td>Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponible para su uso en la región de entrada manuscrita del control <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></td>
<td>Obtiene la colección <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> que se va a conservar con la entrada de lápiz (solo en tiempo de diseño).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propiedad DefaultDrawingAttributes</strong></a></td>
<td>Obtiene o establece la colección <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predeterminada que se va a usar al dibujar y mostrar la entrada de lápiz (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propiedad DesiredPacketDescription</strong></a></td>
<td>Obtiene o establece la descripción del paquete del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propiedad DynamicRendering</strong></a></td>
<td>Obtiene o establece el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> representa dinámicamente la entrada de lápiz a medida que se recopila.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> está en modo de entrada de lápiz, modo de eliminación o modo de edición o selección.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>habilitado</strong></a></td>
<td>Obtiene o establece un valor que determina si el control <a href="inkpicture-control-reference.md">InkPicture</a> puede responder a los eventos generados por el usuario.<br/>
<blockquote>
[!Note]<br />
Esta propiedad es equivalente a la propiedad <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></td>
<td>Obtiene o establece el valor que especifica si la entrada de lápiz se borra por trazo o por punto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></td>
<td>Obtiene o establece el valor que especifica el ancho de la punta del lápiz de borrador.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Identificador</strong></a></td>
<td>Obtiene el identificador de ventana al que está enlazado el control <a href="inkpicture-control-reference.md">InkPicture</a> . (solo en tiempo de ejecución)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrada de lápiz</strong></a></td>
<td>Obtiene o establece el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> que está asociado al control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></td>
<td>Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> recopila entradas manuscritas (paquetes en el aire, cursor en eventos de intervalo, etc.).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propiedad MarginX</strong></a></td>
<td>Obtiene o establece el margen del eje x alrededor del rectángulo de la ventana en coordenadas de la pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propiedad marginy</strong></a></td>
<td>Obtiene o establece el margen del eje y alrededor del rectángulo de la ventana en coordenadas de la pantalla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propiedad MouseIcon</strong></a></td>
<td>Obtiene o establece el icono actual del mouse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer (propiedad)</strong></a></td>
<td>Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está encima de una parte determinada del control <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagen</strong></a></td>
<td>Obtiene el archivo de gráficos que se va a mostrar en el control <a href="inkpicture-control-reference.md">InkPicture</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propiedad)</strong></a></td>
<td>Obtiene o establece el objeto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> que se usa para dibujar la entrada de lápiz en el control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selección</strong></a></td>
<td>Obtiene la colección <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> actualmente seleccionada dentro del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></td>
<td>Obtiene o establece cómo controla el control la posición y el tamaño de la imagen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propiedad SupportHighContrastInk</strong></a></td>
<td>Obtiene un valor que especifica si la entrada de lápiz se representa como un solo color, color = COLOR_WINDOWTEXT (de la llamada a GetSystemMetrics) cuando el sistema está en modo de contraste alto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></td>
<td>Obtiene o establece un valor que especifica si todas las interfaces de usuario de selección (el cuadro de límite de selección y los controladores de selección) se dibujan en contraste alto cuando el sistema está en modo de contraste alto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propiedad de Tablet PC</strong></a></td>
<td>Obtiene el objeto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> que el control <a href="inkpicture-control-reference.md">InkPicture</a> está usando actualmente para recopilar la entrada.<br/></td>
</tr>
</tbody>
</table>



 


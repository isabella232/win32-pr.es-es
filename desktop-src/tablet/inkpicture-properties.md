---
description: Esta sección contiene propiedades para el control InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Propiedades de InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5419d6a72af365af7f663018e121563c263e6b3b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476811"
---
# <a name="inkpicture-properties"></a>Propiedades de InkPicture

Esta sección contiene propiedades para el control InkPicture.




| Propiedad | Descripción | 
|----------|-------------|
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Propiedad AutoRedraw</strong></a> | Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> se vuelve a dibujar cuando se invalida la ventana (si el objeto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> asociado actualmente al control InkPicture se vuelve a dibujar automáticamente cuando la ventana asociada a InkPicture recibe un mensaje WM_PAINT).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>Backcolor</strong></a> | Obtiene o establece el color de fondo del control <a href="inkpicture-control-reference.md">InkPicture.</a> El color de fondo predeterminado es el color de fondo de la ventana del sistema, que suele ser blanco.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk (propiedad)</strong></a> | Obtiene el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> recopila entrada de lápiz (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a> | Obtiene o establece el modo de colección que determina si la entrada de lápiz, los gestos o la entrada de lápiz y los gestos se reconocen a medida que el usuario escribe.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors (propiedad)</strong></a> | Obtiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>colección IInkCursors</strong></a> disponible para su uso en la región de entrada manuscrita del control <a href="inkpicture-control-reference.md">InkPicture.</a><br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a> | Obtiene la <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>colección IInkCustomStrokes</strong></a> que se va a conservar con la entrada de lápiz (solo en tiempo de diseño).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Propiedad DefaultDrawingAttributes</strong></a> | Obtiene o establece la colección <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predeterminada que se va a usar al dibujar y mostrar la entrada de lápiz (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Propiedad DesiredPacketDescription</strong></a> | Obtiene o establece la descripción del paquete del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Propiedad DynamicRendering</strong></a> | Obtiene o establece el valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> representa dinámicamente la entrada de lápiz a medida que se recopila.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a> | Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> está en modo de entrada de lápiz, en modo de eliminación o en modo de selección o edición.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Habilitado</strong></a> | Obtiene o establece un valor que determina si el control <a href="inkpicture-control-reference.md">InkPicture</a> puede responder a eventos generados por el usuario.<br /><blockquote>[!Note]<br />Esta propiedad es equivalente a la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>propiedad InkEnabled.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a> | Obtiene o establece el valor que especifica si la entrada manuscrita se borra por trazo o por punto.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a> | Obtiene o establece el valor que especifica el ancho de la punta del lápiz de borrador.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>Hwnd</strong></a> | Obtiene el identificador de ventana al que está enlazado el control <a href="inkpicture-control-reference.md">InkPicture.</a> (solo en tiempo de ejecución)<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Entrada de lápiz</strong></a> | Obtiene o establece el <a href="inkdisp-class.md"><strong>objeto InkDisp</strong></a> asociado al control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> | Obtiene o establece un valor que especifica si el control <a href="inkpicture-control-reference.md">InkPicture</a> recopila entradas de lápiz (paquetes en el aire, cursor en eventos de intervalo, y así sucesivamente).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Propiedad MarginX</strong></a> | Obtiene o establece el margen del eje X alrededor del rectángulo de la ventana en coordenadas de pantalla.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Propiedad MarginY</strong></a> | Obtiene o establece el margen del eje Y alrededor del rectángulo de la ventana en coordenadas de pantalla.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Propiedad MouseIcon</strong></a> | Obtiene o establece el icono del mouse personalizado actual.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Propiedad MousePointer</strong></a> | Obtiene o establece un valor que indica el tipo de puntero del mouse que aparece cuando el mouse está sobre una parte determinada del control <a href="inkpicture-control-reference.md">InkPicture.</a><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Imagen</strong></a> | Obtiene el archivo de gráficos que aparece en el control <a href="inkpicture-control-reference.md">InkPicture.</a><br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (propiedad)</strong></a> | Obtiene o establece el <a href="inkrenderer-class.md"><strong>objeto InkRenderer</strong></a> que se usa para dibujar entrada manuscrita en el control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Número de selección</strong></a> | Obtiene la <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">colección InkStrokes</a> seleccionada actualmente dentro del control <a href="inkpicture-control-reference.md">InkPicture</a> (solo en tiempo de ejecución).<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a> | Obtiene o establece cómo el control controla la ubicación y el tamaño de la imagen.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Propiedad SupportHighContrastInk</strong></a> | Obtiene un valor que especifica si la entrada de lápiz se representa como un solo color, Color = COLOR_WINDOWTEXT (de la llamada a GetSystemMetrics) cuando el sistema está en modo contraste alto automático.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a> | Obtiene o establece un valor que especifica si todas las interfaces de usuario de selección (rectángulo de selección y identificadores de selección) se dibujan en contraste alto cuando el sistema está en modo contraste alto selección.<br /> | 
| <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Propiedad de tableta</strong></a> | Obtiene el <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>objeto IInkTablet</strong></a> que el control <a href="inkpicture-control-reference.md">InkPicture</a> usa actualmente para recopilar la entrada.<br /> | 




 


---
title: Usar controles de ficha
description: Este tema contiene dos ejemplos que usan controles de ficha.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488418"
---
# <a name="using-tab-controls"></a>Usar controles de ficha

Este tema contiene dos ejemplos que usan controles de ficha. En el primer ejemplo se muestra cómo usar un control de pestaña para cambiar entre varias páginas de texto en la ventana principal de una aplicación. En el segundo ejemplo se muestra cómo utilizar un control de ficha para cambiar entre varias páginas de controles en un cuadro de diálogo.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-a-tab-control-in-the-main-window.md">Cómo crear un control de pestaña en la ventana principal</a><br/></td>
<td>En el ejemplo de esta sección se muestra cómo crear un control de pestaña y cómo mostrarlo en el área cliente de la ventana principal de la aplicación. La aplicación muestra una tercera ventana (un control estático) en el área de presentación del control de ficha. La ventana primaria coloca y ajusta el tamaño del control de pestaña y del control estático cuando procesa el mensaje de <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> . <br/> En este ejemplo hay siete pestañas, una para cada día de la semana. Cuando el usuario selecciona una pestaña, la aplicación muestra el nombre del día correspondiente en el control estático. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Cómo crear un cuadro de diálogo con pestañas</a><br/></td>
<td>En el ejemplo de esta sección se muestra cómo crear un cuadro de diálogo que usa pestañas para proporcionar varias páginas de controles. El cuadro de diálogo principal es un cuadro de diálogo modal. Cada página de controles se define mediante una plantilla de cuadro de diálogo que tiene el estilo <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> . Cuando se selecciona una ficha, se crea un cuadro de diálogo no modal para la página entrante y se destruye el cuadro de diálogo de la página saliente. <br/>
<blockquote>
[!Note]<br />
En muchos casos, puede implementar cuadros de diálogo de varias páginas más fácilmente mediante el uso de hojas de propiedades. Para obtener más información acerca de las hojas de propiedades, vea <a href="property-sheets.md">acerca de las hojas de propiedades</a>.
</blockquote>
<br/> La plantilla del cuadro de diálogo principal simplemente define dos controles de botón. Al procesar el mensaje de <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , el procedimiento de cuadro de diálogo crea un control de ficha y carga los recursos de plantilla de cuadro de diálogo para cada uno de los cuadros de diálogo secundarios. <br/></td>
</tr>
</tbody>
</table>



 


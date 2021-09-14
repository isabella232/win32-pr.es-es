---
title: Usar controles tab
description: Este tema contiene dos ejemplos que usan controles tab.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a373a1d7d1fc44da851480841aab04bf364b27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165294"
---
# <a name="using-tab-controls"></a>Usar controles tab

Este tema contiene dos ejemplos que usan controles tab. En el primer ejemplo se muestra cómo usar un control de pestaña para cambiar entre varias páginas de texto en la ventana principal de una aplicación. En el segundo ejemplo se muestra cómo usar un control de ficha para cambiar entre varias páginas de controles en un cuadro de diálogo.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="create-a-tab-control-in-the-main-window.md">Cómo crear un control de pestaña en la ventana principal</a><br /> | En el ejemplo de esta sección se muestra cómo crear un control de pestaña y mostrarlo en el área cliente de la ventana principal de la aplicación. La aplicación muestra una tercera ventana (un control estático) en el área de presentación del control de pestaña. La ventana primaria coloca y tamaño el control de tabulación y el control estático cuando procesa <a href="/windows/desktop/winmsg/wm-size"><strong>el WM_SIZE</strong></a> mensaje. <br /> Hay siete pestañas en este ejemplo, una para cada día de la semana. Cuando el usuario selecciona una pestaña, la aplicación muestra el nombre del día correspondiente en el control estático. <br /> | 
| <a href="create-a-tabbed-dialog-box.md">Cómo crear un cuadro de diálogo con pestañas</a><br /> | En el ejemplo de esta sección se muestra cómo crear un cuadro de diálogo que usa pestañas para proporcionar varias páginas de controles. El cuadro de diálogo principal es un cuadro de diálogo modal. Cada página de controles se define mediante una plantilla de cuadro de diálogo que tiene el <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> de diálogo. Cuando se selecciona una pestaña, se crea un cuadro de diálogo de modelado para la página entrante y se destruye el cuadro de diálogo de la página saliente. <br /><blockquote>[!Note]<br />En muchos casos, puede implementar cuadros de diálogo de varias páginas más fácilmente mediante hojas de propiedades. Para obtener más información sobre las hojas de propiedades, vea <a href="property-sheets.md">Acerca de las hojas de propiedades</a>.</blockquote><br /> La plantilla del cuadro de diálogo principal simplemente define dos controles de botón. Al procesar el mensaje <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG,</strong></a> el procedimiento del cuadro de diálogo crea un control de ficha y carga los recursos de plantilla de cuadro de diálogo para cada uno de los cuadros de diálogo secundarios. <br /> | 




 


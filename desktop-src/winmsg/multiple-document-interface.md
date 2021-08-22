---
description: En esta sección se describe la interfaz de múltiples documentos, que es una especificación que define una interfaz de usuario para las aplicaciones que permiten al usuario trabajar con más de un documento al mismo tiempo.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d579d1075f85fae7cd2d4ca6e63e1b8196c6d2118e33102cd511a1e468a18ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705364"
---
# <a name="multiple-document-interface"></a>Interfaz de varios documentos

\[A muchos usuarios nuevos e intermedios les resulta difícil aprender a usar aplicaciones MDI. Por lo tanto, debe tener en cuenta otros modelos para la interfaz de usuario. Sin embargo, puede usar MDI para aplicaciones que no se ajustan fácilmente a un modelo existente.\]

La interfaz de varios documentos (MDI) es una especificación que define una interfaz de usuario para las aplicaciones que permiten al usuario trabajar con más de un documento al mismo tiempo.

### <a name="in-this-section"></a>En esta sección



| Tema                                                                              | Descripción                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Acerca de la interfaz de varios documentos](about-the-multiple-document-interface.md) | Describe la interfaz de varios documentos.<br/>                                     |
| [Uso de la interfaz de varios documentos](using-the-multiple-document-interface.md) | Explica cómo realizar tareas asociadas a la interfaz de múltiples documentos.<br/> |
| [Referencia de MDI](multiple-document-interface-reference.md)                         | Contiene la referencia de API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funciones MDI



| Nombre                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Crea una ventana secundaria MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Proporciona el procesamiento predeterminado para los mensajes de ventana que el procedimiento de ventana de una ventana de marco MDI no procesa. Todos los mensajes de ventana que el procedimiento de ventana no procesa explícitamente deben pasarse a la función [**DefFrameProc,**](/windows/win32/api/winuser/nf-winuser-defframeproca) no a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Proporciona el procesamiento predeterminado para cualquier mensaje de ventana que no procese el procedimiento de ventana de una ventana secundaria MDI. Un mensaje de ventana no procesado por el procedimiento de ventana debe pasarse a la función [**DefMDIChildProc,**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) no a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Procesa las pulsaciones de tecla del acelerador para los comandos de menú de ventana de las ventanas secundarias MDI asociadas a la ventana de cliente MDI especificada. La función traduce los mensajes [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) y [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) en mensajes [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) de WM y los envía a las ventanas secundarias MDI adecuadas. <br/> |



 

### <a name="mdi-messages"></a>Mensajes MDI



| Nombre                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ MDIACTIVATE**](wm-mdiactivate.md)       | Se envía a una ventana de cliente MDI para indicar a la ventana de cliente que active otra ventana secundaria de MDI. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**WM \_ MDICASCADE**](wm-mdicascade.md)         | Se envía a una ventana de cliente MDI para organizar todas sus ventanas secundarias en un formato en cascada. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ MDICREATE**](wm-mdicreate.md)           | Se envía a una ventana de cliente MDI para crear una ventana secundaria de MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIDESTROY**](wm-mdidestroy.md)         | Se envía a una ventana de cliente MDI para cerrar una ventana secundaria de MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md)     | Se envía a una ventana de cliente MDI para recuperar el identificador en la ventana secundaria de MDI activa. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) | Se envía a una ventana de cliente MDI para organizar todas las ventanas secundarias de MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas. <br/>                                                                                                                                                                                                                                                                                                  |
| [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md)       | Se envía a una ventana de cliente MDI para maximizar una ventana secundaria de MDI. El sistema cambia el tamaño de la ventana secundaria para que su área de cliente rellene la ventana de cliente. El sistema coloca el icono de menú de ventana de la ventana secundaria en la posición más a la derecha de la barra de menús de la ventana de marco y coloca el icono de restauración de la ventana secundaria en la posición más a la izquierda. El sistema también anexa el texto de la barra de título de la ventana secundaria al de la ventana de marco. <br/> |
| [**WM \_ MDINEXT**](wm-mdinext.md)               | Se envía a una ventana de cliente MDI para activar la ventana secundaria siguiente o anterior. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md) | Se envía a una ventana de cliente MDI para actualizar el menú de ventana de la ventana marco MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**WM \_ MDIRESTORE**](wm-mdirestore.md)         | Se envía a una ventana de cliente MDI para restaurar una ventana secundaria MDI a partir de un tamaño maximizado o minimizado. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**WM \_ MDISETMENU**](wm-mdisetmenu.md)         | Se envía a una ventana de cliente MDI para reemplazar todo el menú de una ventana de marco MDI, para reemplazar el menú de ventana de la ventana marco, o ambos. <br/>                                                                                                                                                                                                                                                                                           |
| [**WM \_ MDITILE**](wm-mditile.md)               | Se envía a una ventana de cliente MDI para organizar todas sus ventanas secundarias MDI en un formato de icono. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Estructuras MDI



| Nombre                                       | Descripción                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contiene información sobre la clase, el título, el propietario, la ubicación y el tamaño de una ventana secundaria MDI. <br/> |



 

 


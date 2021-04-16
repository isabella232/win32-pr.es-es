---
description: En esta sección se describe la interfaz de varios documentos, que es una especificación que define una interfaz de usuario para las aplicaciones que permiten al usuario trabajar con más de un documento al mismo tiempo.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface.htm
title: Interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1898202aad6ec8d26f859bec2457124328c3a27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706332"
---
# <a name="multiple-document-interface"></a>Interfaz de varios documentos

\[Muchos usuarios nuevos e intermedios le resulta difícil aprender a usar aplicaciones MDI. Por lo tanto, debe tener en cuenta otros modelos para la interfaz de usuario. Sin embargo, puede usar MDI para las aplicaciones que no caben fácilmente en un modelo existente.\]

La interfaz de múltiples documentos (MDI) es una especificación que define una interfaz de usuario para las aplicaciones que permiten al usuario trabajar con más de un documento al mismo tiempo.

### <a name="in-this-section"></a>En esta sección



| Tema                                                                              | Descripción                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Acerca de la interfaz de varios documentos](about-the-multiple-document-interface.md) | Describe la interfaz de múltiples documentos.<br/>                                     |
| [Usar la interfaz de varios documentos](using-the-multiple-document-interface.md) | Explica cómo realizar tareas asociadas con la interfaz de múltiples documentos.<br/> |
| [Referencia de MDI](multiple-document-interface-reference.md)                         | Contiene la referencia de la API.<br/>                                                    |



 

### <a name="mdi-functions"></a>Funciones MDI



| Nombre                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)           | Crea una ventana secundaria MDI. <br/>                                                                                                                                                                                                                                                                                                                                    |
| [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca)                 | Proporciona el procesamiento predeterminado para los mensajes de ventana que el procedimiento de ventana de una ventana de marco MDI no procesa. Todos los mensajes de ventana que el procedimiento de ventana no procese explícitamente se deben pasar a la función [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) , no a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                              |
| [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca)           | Proporciona el procesamiento predeterminado para cualquier mensaje de ventana que el procedimiento de ventana de una ventana secundaria MDI no procese. Un mensaje de ventana no procesado por el procedimiento de ventana se debe pasar a la función [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) , no a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . <br/>                                             |
| [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) | Procesa las pulsaciones de teclas del acelerador para los comandos de menú ventana de las ventanas secundarias MDI asociadas a la ventana de cliente MDI especificada. La función traduce los mensajes de [**\_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) y [**\_ KeyDown**](/windows/desktop/inputdev/wm-keydown) [**de WM a \_**](/windows/desktop/inputdev/wm-keyup) mensajes de WM y los envía a las ventanas secundarias MDI adecuadas. <br/> |



 

### <a name="mdi-messages"></a>Mensajes MDI



| Nombre                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDIACTIVATE de WM \_**](wm-mdiactivate.md)       | Se envía a una ventana de cliente MDI para indicar a la ventana de cliente que active una ventana secundaria MDI diferente. <br/>                                                                                                                                                                                                                                                                                                                               |
| [**MDICASCADE de WM \_**](wm-mdicascade.md)         | Se envía a una ventana de cliente MDI para organizar todas sus ventanas secundarias en un formato en cascada. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MDICREATE de WM \_**](wm-mdicreate.md)           | Se envía a una ventana de cliente MDI para crear una ventana secundaria MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**MDIDESTROY de WM \_**](wm-mdidestroy.md)         | Se envía a una ventana de cliente MDI para cerrar una ventana secundaria MDI. <br/>                                                                                                                                                                                                                                                                                                                                                                         |
| [**MDIGETACTIVE de WM \_**](wm-mdigetactive.md)     | Se envía a una ventana de cliente MDI para recuperar el identificador de la ventana secundaria MDI activa. <br/>                                                                                                                                                                                                                                                                                                                                                |
| [**MDIICONARRANGE de WM \_**](wm-mdiiconarrange.md) | Se envía a una ventana de cliente MDI para organizar todas las ventanas secundarias MDI minimizadas. No afecta a las ventanas secundarias que no están minimizadas. <br/>                                                                                                                                                                                                                                                                                                  |
| [**MDIMAXIMIZE de WM \_**](wm-mdimaximize.md)       | Se envía a una ventana de cliente MDI para maximizar una ventana secundaria MDI. El sistema cambia el tamaño de la ventana secundaria para que su área cliente rellene la ventana del cliente. El sistema coloca el icono de menú ventana de la ventana secundaria en la posición más a la derecha de la barra de menús de la ventana de marco y coloca el icono de restauración de la ventana secundaria en la posición más a la izquierda. El sistema también anexa el texto de la barra de título de la ventana secundaria al de la ventana de marco. <br/> |
| [**MDINEXT de WM \_**](wm-mdinext.md)               | Se envía a una ventana de cliente MDI para activar la ventana secundaria siguiente o anterior. <br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**MDIREFRESHMENU de WM \_**](wm-mdirefreshmenu.md) | Se envía a una ventana de cliente MDI para actualizar el menú ventana de la ventana de marco MDI. <br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**MDIRESTORE de WM \_**](wm-mdirestore.md)         | Se envía a una ventana de cliente MDI para restaurar una ventana secundaria MDI de tamaño maximizado o minimizado. <br/>                                                                                                                                                                                                                                                                                                                                      |
| [**MDISETMENU de WM \_**](wm-mdisetmenu.md)         | Se envía a una ventana de cliente MDI para reemplazar el menú completo de una ventana de marco MDI, para reemplazar el menú ventana de la ventana marco o ambos. <br/>                                                                                                                                                                                                                                                                                           |
| [**MDITILE de WM \_**](wm-mditile.md)               | Se envía a una ventana de cliente MDI para organizar todas las ventanas secundarias MDI en formato de mosaico. <br/>                                                                                                                                                                                                                                                                                                                                             |



 

### <a name="mdi-structures"></a>Estructuras MDI



| Nombre                                       | Descripción                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) | Contiene información sobre la clase, el título, el propietario, la ubicación y el tamaño de una ventana secundaria MDI. <br/> |



 

 


---
description: En esta sección se de abordan los procedimientos de ventana. Cada ventana tiene un procedimiento de ventana asociado que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase .
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7892c1547d7f5ed1bf5d70a9242e3bb5bc6a3c8e93121470d27ecbd64fb912
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548465"
---
# <a name="window-procedures"></a>Procedimientos de ventana

Cada ventana tiene un procedimiento de ventana asociado, una función que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase . Todos los aspectos de la apariencia y el comportamiento de una ventana dependen de la respuesta del procedimiento de ventana a estos mensajes.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                         | Descripción                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los procedimientos de ventana](about-window-procedures.md)       | Describe los procedimientos de ventana. Cada ventana es miembro de una clase de ventana determinada. La clase window determina el procedimiento de ventana predeterminado que usa una ventana individual para procesar sus mensajes.<br/> |
| [Usar procedimientos de ventana](using-window-procedures.md)       | Describe cómo realizar las siguientes tareas asociadas a los procedimientos de ventana.<br/>                                                                                                                        |
| [Referencia de procedimiento de ventana](window-procedure-reference.md) | Contiene la referencia de API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Funciones



| Nombre                                     | Descripción                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Pasa información del mensaje al procedimiento de ventana especificado. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Llama al procedimiento de ventana predeterminado para proporcionar el procesamiento predeterminado de los mensajes de ventana que una aplicación no procesa. Esta función garantiza que se procese cada mensaje. [**Se llama a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) con los mismos parámetros recibidos por el procedimiento de ventana. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Función definida por la aplicación que procesa los mensajes enviados a una ventana. El **tipo WNDPROC** define un puntero a esta función de devolución de llamada. [*WindowProc es*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) un marcador de posición para el nombre de la función definida por la aplicación. <br/>                                                            |



 

 

 

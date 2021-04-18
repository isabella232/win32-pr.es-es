---
description: En esta sección se describen los procedimientos de ventana. Cada ventana tiene un procedimiento de ventana asociado que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Procedimientos de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707130"
---
# <a name="window-procedures"></a>Procedimientos de ventana

Cada ventana tiene un procedimiento de ventana asociado, una función que procesa todos los mensajes enviados o publicados en todas las ventanas de la clase. Todos los aspectos de la apariencia y el comportamiento de una ventana dependen de la respuesta del procedimiento de ventana a estos mensajes.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                         | Descripción                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los procedimientos de ventana](about-window-procedures.md)       | Describe los procedimientos de ventana. Cada ventana es miembro de una clase de ventana determinada. La clase Window determina el procedimiento de ventana predeterminado que usa una ventana individual para procesar sus mensajes.<br/> |
| [Usar procedimientos de ventana](using-window-procedures.md)       | Explica cómo realizar las siguientes tareas asociadas a los procedimientos de ventana.<br/>                                                                                                                        |
| [Referencia de procedimiento de ventana](window-procedure-reference.md) | Contiene la referencia de la API.<br/>                                                                                                                                                                         |



 

### <a name="functions"></a>Functions



| Nombre                                     | Descripción                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) | Pasa información del mensaje al procedimiento de ventana especificado. <br/>                                                                                                                                                                                                                                     |
| [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | Llama al procedimiento de ventana predeterminado para proporcionar el procesamiento predeterminado de los mensajes de ventana que una aplicación no procesa. Esta función garantiza que se procesan todos los mensajes. Se llama a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) con los mismos parámetros recibidos por el procedimiento de ventana. <br/> |
| [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))           | Función definida por la aplicación que procesa los mensajes enviados a una ventana. El tipo **WndProc** define un puntero a esta función de devolución de llamada. [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) es un marcador de posición para el nombre de la función definida por la aplicación. <br/>                                                            |



 

 

 

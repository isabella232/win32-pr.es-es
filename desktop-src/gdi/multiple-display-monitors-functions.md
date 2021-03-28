---
description: Las funciones siguientes proporcionan compatibilidad con varios monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Múltiples funciones de monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984927"
---
# <a name="multiple-display-monitors-functions"></a>Múltiples funciones de monitores de pantalla

Las funciones siguientes proporcionan compatibilidad con varios monitores.



| Función                                           | Descripción                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera los monitores de visualización que intersecan una región formada por la intersección de un rectángulo de recorte especificado y el área visible de un contexto de dispositivo. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera información acerca de un monitor de pantalla.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Función de devolución de llamada definida por la aplicación a la que llama la función [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera un identificador para el monitor de pantalla que contiene un punto especificado.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera un identificador para el monitor de pantalla que tiene el área más grande de intersección con un rectángulo especificado.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera un identificador para el monitor de pantalla que tiene el área más grande de intersección con el rectángulo delimitador de una ventana especificada.                       |



 

 

 




---
description: Las siguientes funciones proporcionan compatibilidad con varios monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funciones de varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779145"
---
# <a name="multiple-display-monitors-functions"></a>Funciones de varios monitores de pantalla

Las siguientes funciones proporcionan compatibilidad con varios monitores.



| Función                                           | Descripción                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera los monitores de presentación que forman una intersección con una región formada por la intersección de un rectángulo de recorte especificado y la región visible de un contexto de dispositivo. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera información sobre un monitor de visualización.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Función de devolución de llamada definida por la aplicación a la que llama [**la función EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera un identificador para el monitor de visualización que contiene un punto especificado.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera un identificador para el monitor de visualización que tiene el área de intersección más grande con un rectángulo especificado.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera un identificador para el monitor de visualización que tiene el área de intersección más grande con el rectángulo delimitador de una ventana especificada.                       |



 

 

 




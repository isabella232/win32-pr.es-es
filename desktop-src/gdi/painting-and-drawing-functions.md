---
description: Las siguientes funciones se usan con dibujo y dibujo.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Funciones de dibujo y dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51b8acb0ea187c17d220d80f105ad6ae49371688d4eb8671c2a8eb5949b6e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666625"
---
# <a name="painting-and-drawing-functions"></a>Funciones de dibujo y dibujo

Las siguientes funciones se usan con dibujo y dibujo.



| Función                                       | Descripción                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Prepara una ventana para pintar.                                                                             |
| [**DrawAnimatedRects**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Dibuja un rectángulo y lo anima para indicar la actividad de icono o ventana.                                      |
| [**DrawCaption**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Dibuja un título de ventana.                                                                                     |
| [**DrawEdge**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Dibuja uno o varios bordes del rectángulo.                                                                       |
| [**DrawFocusRect**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Dibuja un rectángulo en el estilo que indica que el rectángulo tiene el foco.                                  |
| [**DrawFrameControl**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Dibuja un control de marco.                                                                                      |
| [**DrawState**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Muestra una imagen y aplica un efecto visual para indicar un estado.                                          |
| [**DrawStateProc**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Función de devolución de llamada que representa una imagen compleja para [**DrawState.**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                        |
| [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Marca el final del dibujo en una ventana.                                                                      |
| [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Impide dibujar dentro de áreas no válidas de una ventana.                                                          |
| [**GdiFlush**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Vacía el lote actual del subproceso que realiza la llamada.                                                                 |
| [**GdiGetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Devuelve el número máximo de llamadas de función que se pueden acumular en el lote actual del subproceso de llamada. |
| [**GdiSetBatchLimit**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Establece el número máximo de llamadas de función que se pueden acumular en el lote actual del subproceso de llamada.    |
| [**GetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Devuelve el color de fondo de un contexto de dispositivo.                                                          |
| [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Devuelve el modo de combinación de fondo para un contexto de dispositivo.                                                       |
| [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Obtiene el rectángulo delimitador acumulado para un contexto de dispositivo.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Obtiene el modo de combinación de primer plano de un contexto de dispositivo.                                                           |
| [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Obtiene las coordenadas del rectángulo más pequeño que incluye la región de actualización de una ventana.                 |
| [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Obtiene la región de actualización de una ventana.                                                                         |
| [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Obtiene el contexto del dispositivo para una ventana, incluida la barra de título, los menús y las barras de desplazamiento.                          |
| [**GetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Obtiene una copia de la región de ventana de una ventana.                                                               |
| [**GetWindowRgnBox**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Obtiene las dimensiones del rectángulo delimitador más ajustado para la región de ventana de una ventana.                   |
| [**GrayString**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Dibuja texto gris en una ubicación.                                                                              |
| [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Agrega un rectángulo a la región de actualización de una ventana.                                                               |
| [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Invalida el área de cliente dentro de una región.                                                                |
| [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Deshabilita o habilita el dibujo en una ventana.                                                                    |
| [**OutputProc**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Función de devolución de llamada usada con la [**función GrayString.**](/windows/desktop/api/Winuser/nf-winuser-graystringa) Se usa para dibujar una cadena.   |
| [**PaintDesktop**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Rellena la región de recorte en un contexto de dispositivo con un patrón.                                               |
| [**Volver a dibujarWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Actualiza una región en el área de cliente de una ventana.                                                                 |
| [**SetBkColor**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Establece el fondo en un valor de color.                                                                       |
| [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Establece el modo de combinación en segundo plano de un contexto de dispositivo.                                                           |
| [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Controla la acumulación de información de rectángulo delimitador para un contexto de dispositivo.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Establece el modo de combinación de primer plano.                                                                               |
| [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Establece la región de ventana de una ventana.                                                                         |
| [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Actualiza el área de cliente de una ventana.                                                                        |
| [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Valida el área de cliente dentro de un rectángulo.                                                               |
| [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Valida el área de cliente dentro de una región.                                                                  |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Devuelve un identificador a la ventana asociada a un contexto de dispositivo.                                            |



 

 

 




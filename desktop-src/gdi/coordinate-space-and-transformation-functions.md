---
description: Las siguientes funciones se usan con espacios de coordenadas y transformaciones.
ms.assetid: 3ebcabf2-9718-47b2-aba0-7cc28fa42e5a
title: Funciones de espacio de coordenadas y transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe24e78002393d7a840e99d33840dfa4ba0d9e2ac89d941f998261955683e13f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718085"
---
# <a name="coordinate-space-and-transformation-functions"></a>Funciones de espacio de coordenadas y transformación

Las siguientes funciones se usan con espacios de coordenadas y transformaciones.



| Función                                                                       | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ClientToScreen**](/windows/desktop/api/Winuser/nf-winuser-clienttoscreen)                                       | Convierte las coordenadas de área de cliente de un punto especificado en coordenadas de pantalla.                                                 |
| [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform)                                   | Concatena dos transformaciones de espacio del mundo a espacio de página.                                                                      |
| [**DPtoLP**](/windows/desktop/api/Wingdi/nf-wingdi-dptolp)                                                       | Convierte las coordenadas del dispositivo en coordenadas lógicas.                                                                            |
| [**GetCurrentPositionEx**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentpositionex)                           | Recupera la posición actual en coordenadas lógicas.                                                                           |
| [**GetDisplayAutoRotationPreferences**](/previous-versions//dn376360(v=vs.85)) | Obtiene las preferencias de orientación de la presentación.                                                                                 |
| [**GetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-getgraphicsmode)                                     | Recupera el modo gráfico actual para el contexto de dispositivo especificado.                                                            |
| [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)                                               | Recupera el modo de asignación actual.                                                                                              |
| [**GetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportextex)                                   | Recupera las extensiones x e y de la ventanilla actual para el contexto de dispositivo especificado.                                    |
| [**GetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getviewportorgex)                                   | Recupera las coordenadas X e y del origen de la ventanilla para el contexto de dispositivo especificado.                           |
| [**GetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindowextex)                                       | Recupera las extensiones x e y de la ventana para el contexto de dispositivo especificado.                                              |
| [**GetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getwindoworgex)                                       | Recupera las coordenadas X e y del origen de la ventana para el contexto de dispositivo especificado.                             |
| [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform)                                 | Recupera la transformación espacio del mundo actual en espacio de página.                                                                  |
| [**LPtoDP**](/windows/desktop/api/Wingdi/nf-wingdi-lptodp)                                                       | Convierte las coordenadas lógicas en coordenadas del dispositivo.                                                                            |
| [**MapWindowPoints**](/windows/desktop/api/Winuser/nf-winuser-mapwindowpoints)                                     | Convierte (asigna) un conjunto de puntos de un espacio de coordenadas relativo a una ventana en un espacio de coordenadas en relación con otra ventana. |
| [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform)                           | Cambia la transformación global de un contexto de dispositivo mediante el modo especificado.                                                  |
| [**OffsetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetviewportorgex)                             | Modifica el origen de la ventanilla para un contexto de dispositivo mediante los desplazamientos horizontal y vertical especificados.                           |
| [**OffsetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-offsetwindoworgex)                                 | Modifica el origen de la ventana para un contexto de dispositivo mediante los desplazamientos horizontal y vertical especificados.                             |
| [**ScaleViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scaleviewportextex)                               | Modifica la ventanilla de un contexto de dispositivo mediante las relaciones formadas por los multiplicandos y divisores especificados.                  |
| [**ScaleWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-scalewindowextex)                                   | Modifica la ventana de un contexto de dispositivo mediante las relaciones formadas por los multiplicandos y divisores especificados.                    |
| [**ScreenToClient**](/windows/desktop/api/Winuser/nf-winuser-screentoclient)                                       | Convierte las coordenadas de pantalla de un punto especificado de la pantalla en coordenadas de cliente.                                        |
| [**SetDisplayAutoRotationPreferences**](/previous-versions//dn376361(v=vs.85)) | Establece las preferencias de orientación de la pantalla.                                                                                 |
| [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode)                                     | Establece el modo gráfico para el contexto de dispositivo especificado.                                                                         |
| [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)                                               | Establece el modo de asignación del contexto de dispositivo especificado.                                                                           |
| [**SetViewportExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportextex)                                   | Establece las extensiones horizontales y verticales de la ventanilla para un contexto de dispositivo mediante los valores especificados.                     |
| [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex)                                   | Especifica qué punto de dispositivo se asigna al origen de la ventana (0,0).                                                                    |
| [**SetWindowExtEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindowextex)                                       | Establece las extensiones horizontal y vertical de la ventana para un contexto de dispositivo mediante los valores especificados.                       |
| [**SetWindowOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setwindoworgex)                                       | Especifica qué punto de ventana se asigna al origen de la ventanilla (0,0).                                                                  |
| [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)                                 | Establece una transformación lineal bidimensional entre el espacio del mundo y el espacio de página para el contexto de dispositivo especificado.                |



 

 

 

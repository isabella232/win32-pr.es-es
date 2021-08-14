---
description: "En la tabla siguiente se describe en qué subprocesos se pueden abrir los eventos de objeto InkOverlay. EventThreadsCursorButtonDownFires en el subproceso de entrada de lápizCursorButtonUpFires en el subproceso de entrada de lápizCursorDownFires en el subproceso de entrada de lápizCursorInRangeFires en el subproceso de entrada de lápizCursorOutOfRangeFires en el subproceso de entrada de lápizDoubleClick (solo Automation). Se activo en el subproceso de interfaz de usuario (UI) de la aplicaciónDoubleClick (solo biblioteca administrada). Se fires on the application's UI threadGestureFires on the ink threadMouseDownFires on the application's UI threadMouseMoveFires on the application's UI threadMouseUpFires on the application's UI threadMouseWheelFires en el subproceso de interfaz de usuario de la aplicaciónNewInAirPacketsFires en el subproceso de entrada de lápizNewPacketsFires en el subproceso de entrada de lápizPaintedFires en el subproceso de interfaz de usuario de la aplicaciónPaintingFires en el subproceso de interfaz de usuario de la aplicaciónSelectionChangedFires en el subproceso de entrada de lápiz, o en el subproceso que actualiza el objeto InkOverlay  Propiedad SelectionSelectionChangingFires en el subproceso de entrada de lápizSelectionMovedFires en el subproceso de entrada de lápizSelectionMovingFires en el subproceso de entrada de lápizSelectionResizedFires en el subproceso de entrada de lápizSelectionResizingFires en el subproceso de entrada de lápizStrokeFires en el subproceso de entrada de lápizStrokesDeletedFires en el subproceso de entrada de lápizStrokesDeletingFires en el subproceso inkSystemGestureFires en el subproceso de entrada de lápizTabletAddedFires en el subproceso de entrada de lápizTabletRemovedFires en el subproceso de entrada de lápiz "
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventos de objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ee197a14edf3ce0aa8595bdbcdb3ea2937d9cf863dcc6e95690088ed8ee96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218968"
---
# <a name="inkoverlay-object-events"></a>Eventos de objeto InkOverlay

En la tabla siguiente se describe en qué subprocesos se pueden abrir los eventos de objeto [**InkOverlay.**](inkoverlay-class.md)



| Evento                                                                             | Subprocesos                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (solo Automation).                  | Se activo en el subproceso de la interfaz de usuario (UI) de la aplicación<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (solo biblioteca administrada). | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Gesto**](inkoverlay-gesture.md)                                             | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Mousedown**](inkoverlay-mousedown.md)                                         | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Mousemove**](inkoverlay-mousemove.md)                                         | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Mousewheel**](inkoverlay-mousewheel.md)                                       | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                                             | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Pintura**](inkoverlay-painting.md)                                           | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Se ejecuta en el subproceso de entrada de lápiz o en el subproceso que actualiza la propiedad Selection del [**objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) [**InkOverlay.**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Golpe**](inkoverlay-stroke.md)                                               | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Tableta agregada**](inkoverlay-tabletadded.md)                                     | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Se activo en el subproceso de entrada de lápiz<br/>                                                                                                                                        |



 

 


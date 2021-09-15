---
description: 'En la tabla siguiente se describe en qué subprocesos se pueden abrir los eventos de objeto InkOverlay. EventThreadsCursorButtonDownFires en el subproceso de entrada de lápizCursorButtonUpFires en el subproceso inkCursorDownFires en el subproceso inkCursorInRangeFires en el subproceso de entrada de lápizCursorOutOfRangeFires en el subproceso de entrada de lápizDoubleClick (solo Automation). Se ejecuta en el subproceso de interfaz de usuario (UI) de la aplicaciónDoubleClick (solo biblioteca administrada). Se activo en el subproceso de interfaz de usuario de la aplicaciónGestureFires en el subproceso de entrada de lápizMouseDownFires en el subproceso de interfaz de usuario de la aplicaciónMouseMoveFires en el subproceso de interfaz de usuario de la aplicaciónMouseUpFires en el subproceso de interfaz de usuario de la aplicaciónMouseWheelFires en el subproceso de interfaz de usuario de la aplicaciónNewInAirPacketsFires en el subproceso de entrada de lápizNewPacketsFires en el subproceso de entrada de lápizPaintedFires en el subproceso de interfaz de usuario de la aplicaciónPaintingFires en el subproceso de interfaz de usuario de la aplicaciónSelectionChangedFires en el subproceso de entrada de lápiz, o en el subproceso que actualiza el objeto InkOverlay  Propiedad SelectionSelectionChangingFires en el subproceso de entrada de lápizSelectionMovedFires en el subproceso inkSelectionMovingFires en el subproceso inkSelectionResizedFires en el subproceso inkSelectionResizingFires en el subproceso inkStrokeFires on el subproceso de entrada de lápizStrokesDeletedFires en el subproceso de entrada de lápizStrokesDeletingFires en el subproceso inkSystemGestureFires en el subproceso inkTabletAddedFires en el subproceso de entrada de lápizTabletRemovedFires en el subproceso de entrada de lápiz '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventos de objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360263"
---
# <a name="inkoverlay-object-events"></a>Eventos de objeto InkOverlay

En la tabla siguiente se describe en qué subprocesos se pueden abrir los eventos de objeto [**InkOverlay.**](inkoverlay-class.md)



| Evento                                                                             | Subprocesos                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (solo Automation).                  | Se activo en el subproceso de interfaz de usuario (UI) de la aplicación<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (solo biblioteca administrada). | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Gesto**](inkoverlay-gesture.md)                                             | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Mousedown**](inkoverlay-mousedown.md)                                         | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Mousemove**](inkoverlay-mousemove.md)                                         | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Mousewheel**](inkoverlay-mousewheel.md)                                       | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Pintado**](inkoverlay-painted.md)                                             | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Pintura**](inkoverlay-painting.md)                                           | Se activo en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Se ejecuta en el subproceso de entrada de lápiz o en el subproceso que actualiza la propiedad Selection del [**objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) [**InkOverlay.**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Golpe**](inkoverlay-stroke.md)                                               | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**Tableta agregada**](inkoverlay-tabletadded.md)                                     | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Se dispara en el subproceso de entrada de lápiz<br/>                                                                                                                                        |



 

 


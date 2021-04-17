---
description: 'En la tabla siguiente se describen los subprocesos que pueden desencadenar los eventos del objeto InkOverlay. EventThreadsCursorButtonDownFires en el threadCursorButtonUpFires de entrada manuscrita en el threadCursorDownFires de entrada manuscrita en el threadCursorInRangeFires de entrada manuscrita en el threadCursorOutOfRangeFires de entrada manuscrita (solo automatización). Se activa en la interfaz de usuario (UI) de la aplicación threadDoubleClick (solo biblioteca administrada). Se activa en la interfaz de usuario threadGestureFires de la aplicación en el threadMouseDownFires de entrada de lápiz de la interfaz de usuario de la aplicación threadMouseMoveFires en la interfaz de usuario de la aplicación threadMouseUpFires en la interfaz de usuario de la aplicación threadMouseWheelFires en la interfaz de usuario de la aplicación threadNewInAirPacketsFires en el subproceso de entrada manuscrita threadNewPacketsFires en la interfaz de usuario de la aplicación threadPaintedFires o bien, en el subproceso, se actualiza la selección del objeto InkOverlay propertySelectionChangingFires en el threadSelectionMovedFires de entrada manuscrita en el threadSelectionMovingFires de entrada manuscrita en el threadSelectionResizedFires de entrada manuscrita en la entrada threadSelectionResizingFires threadStrokeFires de entrada manuscrita en el threadStrokesDeletedFires de entrada manuscrita en el threadStrokesDeletingFires de entrada manuscrita en el threadSystemGestureFires de entrada manuscrita en el threadTabletAddedFires de entrada manuscrita en el subproceso de entrada manuscrita '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: Eventos de objeto InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706956"
---
# <a name="inkoverlay-object-events"></a>Eventos de objeto InkOverlay

En la tabla siguiente se describen los subprocesos que pueden desencadenar los eventos del objeto [**InkOverlay**](inkoverlay-class.md) .



| Evento                                                                             | Subprocesos                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (solo automatización).                  | Se desencadena en el subproceso de la interfaz de usuario (IU) de la aplicación<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (solo biblioteca administrada). | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Gesto**](inkoverlay-gesture.md)                                             | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**Eventos**](inkoverlay-mousedown.md)                                         | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**MouseMove**](inkoverlay-mousemove.md)                                         | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Rueda**](inkoverlay-mousewheel.md)                                       | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**Representan**](inkoverlay-painted.md)                                             | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**Vuelva**](inkoverlay-painting.md)                                           | Se desencadena en el subproceso de interfaz de usuario de la aplicación<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Se desencadena en el subproceso de entrada manuscrita o en el subproceso que actualiza la propiedad de [**selección**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) del objeto [**InkOverlay**](inkoverlay-class.md)<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**Stroke**](inkoverlay-stroke.md)                                               | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | Se desencadena en el subproceso de entrada manuscrita<br/>                                                                                                                                        |



 

 


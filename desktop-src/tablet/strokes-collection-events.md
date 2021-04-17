---
description: En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos de la colección de trazos. EventThreadsStrokesAddedFires en el subproceso de entrada manuscrita o en el subproceso del llamador. Un evento StrokesAdded generado por la interacción del usuario con el objeto InkCollector, el objeto InkOverlay o el control InkPicture se activa en el subproceso de entrada manuscrita. StrokesRemovedFires en el subproceso de entrada manuscrita o en el subproceso del llamador. Un evento StrokesRemoved generado por la interacción del usuario con el objeto InkCollector, el objeto InkOverlay o el control InkPicture se activa en el subproceso de entrada manuscrita.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventos de la colección Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04388179c53a4b85c5333ae6061cdd7612967174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717153"
---
# <a name="strokes-collection-events"></a>Eventos de la colección Strokes

En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos de la colección de [**trazos**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .



| Evento                                               | Subprocesos                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**StrokesAdded**](inkstrokes-strokesadded.md)     | Se desencadena en el subproceso de entrada manuscrita o en el subproceso del llamador.<br/> Un evento [**StrokesAdded**](inkstrokes-strokesadded.md) generado por la interacción del usuario con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) se activa en el subproceso de entrada manuscrita.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Se desencadena en el subproceso de entrada manuscrita o en el subproceso del llamador.<br/> Un evento [**StrokesRemoved**](inkstrokes-strokesremoved.md) generado por la interacción del usuario con el objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) se activa en el subproceso de entrada manuscrita.<br/> |



 

 

 

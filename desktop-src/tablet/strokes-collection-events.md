---
description: En la tabla siguiente se describen los subprocesos en los que se pueden establecer los eventos de colección Strokes. EventThreadsStrokesAddedFires en el subproceso de entrada de lápiz o en el subproceso del autor de la llamada. Un evento StrokesAdded generado por la interacción del usuario con el objeto InkCollector, el objeto InkOverlay o el control InkPicture se genera en el subproceso ink. StrokesRemovedFires en el subproceso de entrada de lápiz o en el subproceso del autor de la llamada. Un evento StrokesRemoved generado por la interacción del usuario con el objeto InkCollector, el objeto InkOverlay o el control InkPicture, se genera en el subproceso ink.
ms.assetid: f9503c3b-6c43-442c-af43-3415ad17626f
title: Eventos de colección de trazos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24be819f63fa29cd0d650ce27f760984ca6d917886fe5f45e1ec72cf4c9fe2ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589785"
---
# <a name="strokes-collection-events"></a>Eventos de colección de trazos

En la tabla siguiente se describen los subprocesos en los que se pueden establecer los eventos de colección [**Strokes.**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))



| Evento                                               | Subprocesos                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Trazos agregados**](inkstrokes-strokesadded.md)     | Se ejecuta en el subproceso de entrada de lápiz o en el subproceso del autor de la llamada.<br/> Un [**evento StrokesAdded**](inkstrokes-strokesadded.md) generado por la interacción del usuario con el objeto [**InkCollector,**](inkcollector-class.md) el [**objeto InkOverlay**](inkoverlay-class.md) o el control [InkPicture](inkpicture-control-reference.md) se genera en el subproceso ink.<br/>     |
| [**StrokesRemoved**](inkstrokes-strokesremoved.md) | Se ejecuta en el subproceso de entrada de lápiz o en el subproceso del autor de la llamada.<br/> Un [**evento StrokesRemoved**](inkstrokes-strokesremoved.md) generado por la interacción del usuario con el objeto [**InkCollector,**](inkcollector-class.md) el [**objeto InkOverlay**](inkoverlay-class.md) o el control [InkPicture,](inkpicture-control-reference.md) se genera en el subproceso ink.<br/> |



 

 

 

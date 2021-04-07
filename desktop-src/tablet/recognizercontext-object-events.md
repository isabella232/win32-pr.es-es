---
description: En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos del objeto RecognizerContext. EventThreadsRecognitionFires en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del objeto RecognizerContext. RecognitionWithAlternatesFires en el subproceso de reconocimiento en segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002498"
---
# <a name="recognizercontext-object-events"></a>Eventos de objeto RecognizerContext

En la tabla siguiente se describen los subprocesos en los que se pueden activar los eventos del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .



| Evento                                                                               | Subprocesos                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconocimiento**](inkrecognizercontext-recognition.md)                             | Se desencadena en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) .<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se desencadena en el subproceso de reconocimiento en segundo plano.<br/>                                                                                                                                                               |



 

 

 





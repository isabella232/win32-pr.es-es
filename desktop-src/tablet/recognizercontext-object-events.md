---
description: En la tabla siguiente se describen los subprocesos en los que se pueden activo los eventos de objeto RecognizerContext. EventThreadsRecognitionFires en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del objeto RecognizerContext. RecognitionWithAlternatesFires en el subproceso de reconocimiento en segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467150"
---
# <a name="recognizercontext-object-events"></a>Eventos de objeto RecognizerContext

En la tabla siguiente se describen los subprocesos en los que se pueden activo los eventos de objeto [**RecognizerContext.**](inkrecognizercontext-class.md)



| Evento                                                                               | Subprocesos                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconocimiento**](inkrecognizercontext-recognition.md)                             | Se ejecuta en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del [**objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) [**RecognizerContext.**](inkrecognizercontext-class.md)<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se ejecuta en el subproceso de reconocimiento en segundo plano.<br/>                                                                                                                                                               |



 

 

 





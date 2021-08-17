---
description: En la tabla siguiente se describen los subprocesos en los que se pueden activo los eventos de objeto RecognizerContext. EventThreadsRecognitionFires en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del objeto RecognizerContext. RecognitionWithAlternatesFires en el subproceso de reconocimiento en segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091445"
---
# <a name="recognizercontext-object-events"></a>Eventos de objeto RecognizerContext

En la tabla siguiente se describen los subprocesos en los que se pueden activo los eventos de objeto [**RecognizerContext.**](inkrecognizercontext-class.md)



| Evento                                                                               | Subprocesos                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconocimiento**](inkrecognizercontext-recognition.md)                             | Se ejecuta en el subproceso de reconocimiento en segundo plano o en el subproceso que llama al método Recognize del [**objeto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) [**RecognizerContext.**](inkrecognizercontext-class.md)<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Se ejecuta en el subproceso de reconocimiento en segundo plano.<br/>                                                                                                                                                               |



 

 

 





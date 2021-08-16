---
title: Clase StreamSelectOperation
description: Registra un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetMuteAsync y proporciona un método que devuelve los resultados de la operación. | Clase StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- StreamSelectOperation class Media Streaming API
- StreamSelectOperation class Media Streaming API , descrito
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161434aad9c4eb20960950ba2dd1979c9caaa2ccc5bbe3c2683ee3e4f839a0b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461565"
---
# <a name="streamselectoperation-class"></a>Clase StreamSelectOperation

Registra un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) y proporciona un método que devuelve los resultados de la operación.

**StreamSelectOperation** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase StreamSelectOperation** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Devuelve los resultados de la operación asincrónica iniciada [**por SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).<br/> |



 

### <a name="properties"></a>Propiedades

La **clase StreamSelectOperation** tiene estas propiedades.



| Propiedad                                                        | Tipo de acceso           | Descripción                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completed**](streamselectoperation-completed.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85))<br/> |



 

 


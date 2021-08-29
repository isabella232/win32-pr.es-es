---
title: Propiedad PlaybackOperation.Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de MediaRenderer.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Propiedad completada Media Streaming API
- Propiedad completada Media Streaming API, interfaz PlaybackOperation
- Interfaz PlaybackOperation Media Streaming API, propiedad Completed
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65721977b535a799d3dfa679b026b2d1d06b3eb9d449e487ceaeeeacb135d625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034513"
---
# <a name="playbackoperationcompleted-property"></a>Propiedad PlaybackOperation.Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción [**de MediaRenderer.**](mediarenderer.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





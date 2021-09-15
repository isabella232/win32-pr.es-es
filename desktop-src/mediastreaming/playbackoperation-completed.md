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
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571672"
---
# <a name="playbackoperationcompleted-property"></a>Propiedad PlaybackOperation.Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de [**MediaRenderer.**](mediarenderer.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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

 

 





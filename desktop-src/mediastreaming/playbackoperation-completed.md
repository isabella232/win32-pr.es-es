---
title: Propiedad PlaybackOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de MediaRenderer.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz PlaybackOperation
- Interfaz PlaybackOperation API de streaming de multimedia, propiedad Completed
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714285"
---
# <a name="playbackoperationcompleted-property"></a>Propiedad PlaybackOperation. Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por uno de los métodos de reproducción de [**MediaRenderer**](mediarenderer.md) .

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





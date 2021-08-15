---
title: GetTransportInformationOperation Completed, propiedad
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetTransportInformationAsync.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Propiedad completada Media Streaming API
- Propiedad completada Media Streaming API, interfaz GetTransportInformationOperation
- Interfaz GetTransportInformationOperation De Media Streaming API, propiedad Completed
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 389d7b281c10458e854407f9ce02bd2656fe6d4b16574408d75ae06ccc06d7f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735788"
---
# <a name="gettransportinformationoperationcompleted-property"></a>GetTransportInformationOperation::Completed, propiedad

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetTransportInformationAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

 
---
title: Propiedad CreateMediaRendererOperation.Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por CreateMediaRendererAsync o CreateMediaRendererFromBasicDeviceAsync.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Propiedad completada Media Streaming API
- Propiedad completada Media Streaming API, interfaz CreateMediaRendererOperation
- CreateMediaRendererOperation interface Media Streaming API , propiedad Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86f2a0f33bfe00b65dc6e2e8a77d1e29e0ad4ea05888d6dba86797898bc8cfb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952785"
---
# <a name="createmediarendereroperationcompleted-property"></a>Propiedad CreateMediaRendererOperation.Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) o [**CreateMediaRendererFromBasicDeviceAsync.**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md)

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateMediaRendererOperation**](createmediarendereroperation.md)
</dt> </dl>

 

 





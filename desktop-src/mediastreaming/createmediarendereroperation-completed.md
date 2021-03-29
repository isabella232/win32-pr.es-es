---
title: Propiedad CreateMediaRendererOperation. Completed
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por CreateMediaRendererAsync o CreateMediaRendererFromBasicDeviceAsync.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Propiedad completada API de streaming de multimedia
- Propiedad completada API de streaming multimedia, interfaz CreateMediaRendererOperation
- Interfaz CreateMediaRendererOperation API de streaming de multimedia, propiedad Completed
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783953"
---
# <a name="createmediarendereroperationcompleted-property"></a>Propiedad CreateMediaRendererOperation. Completed

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) o [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CreateMediaRendererOperation**](createmediarendereroperation.md)
</dt> </dl>

 

 





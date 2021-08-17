---
title: GetStreamPropertiesOperation.Completed, propiedad
description: Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetStreamPropertiesAsync.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Propiedad completada Media Streaming API
- Propiedad completada Media Streaming API, interfaz GetStreamPropertiesOperation
- Interfaz GetStreamPropertiesOperation de Media Streaming API, propiedad Completed
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6fc6982866ed97f70467d13cb5e899d94a1459266ca0149d12400d154aad784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100670"
---
# <a name="getstreampropertiesoperationcompleted-property"></a>GetStreamPropertiesOperation.Completed, propiedad

Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetStreamPropertiesAsync.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a>Valor de propiedad

Controlador de eventos.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 

 
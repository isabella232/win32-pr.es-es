---
title: Método GetPositionInformationOperation.GetResults
description: Devuelve los resultados de la operación asincrónica iniciada por GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz GetPositionInformationOperation
- Interfaz GetPositionInformationOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e924227c37318a788f9c30aea5e5125a40c69175ac7c4449a54ebcc4cf61326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721065"
---
# <a name="getpositioninformationoperationgetresults-method"></a>Método GetPositionInformationOperation.GetResults

Devuelve los resultados de la operación asincrónica iniciada [**por GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Referencia a una [**estructura PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) que contiene los resultados de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la [**propiedad Completed.**](getpositioninformationoperation-completed.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 


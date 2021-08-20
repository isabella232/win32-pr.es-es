---
title: Método GetMuteOperation.GetResults
description: Devuelve los resultados de la operación asincrónica iniciada por GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz GetMuteOperation
- Interfaz GetMuteOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972414"
---
# <a name="getmuteoperationgetresults-method"></a>Método GetMuteOperation.GetResults

Devuelve los resultados de la operación asincrónica iniciada [**por GetMuteAsync.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Valor de exclusión mutua. Un valor true indica que el audio está muted actualmente. Un valor de false indica que el audio no está silenciado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la [**propiedad Completed.**](getmuteoperation-completed.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 


---
title: Método GetTransportInformationOperation GetResults
description: Devuelve los resultados de la operación asincrónica iniciada por GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz GetTransportInformationOperation
- Interfaz GetTransportInformationOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbcc6345a09d0553df240c57e50b4498618be76cc75814f268892aa6e0b4dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100639"
---
# <a name="gettransportinformationoperationgetresults-method"></a>Método GetTransportInformationOperation::GetResults

Devuelve los resultados de la operación asincrónica iniciada [**por GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Referencia a una [**estructura TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) que contiene los resultados de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la [**propiedad Completed.**](gettransportinformationoperation-completed.md)

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 


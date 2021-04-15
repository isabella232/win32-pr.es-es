---
title: GetTransportInformationOperation GetResults (método)
description: Devuelve los resultados de la operación asincrónica iniciada por GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Método GetResults API de streaming de multimedia
- Método GetResults API de streaming multimedia, interfaz GetTransportInformationOperation
- GetTransportInformationOperation interface media streaming API, GetResults (método)
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420657"
---
# <a name="gettransportinformationoperationgetresults-method"></a>GetTransportInformationOperation:: GetResults (método)

Devuelve los resultados de la operación asincrónica iniciada por [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de out, retval\]
</dt> <dd>

Referencia a una estructura [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) que contiene los resultados de la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la propiedad [**completed**](gettransportinformationoperation-completed.md) .

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 


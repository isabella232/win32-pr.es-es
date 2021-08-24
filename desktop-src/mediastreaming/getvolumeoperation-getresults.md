---
title: Método GetVolumeOperation.GetResults
description: Devuelve los resultados de la operación asincrónica iniciada por GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz GetVolumeOperation
- Interfaz GetVolumeOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e58188a0d8b0d2ed13a9cb7d7486f440f4a1303ca32208371690965f976339d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011855"
---
# <a name="getvolumeoperationgetresults-method"></a>Método GetVolumeOperation.GetResults

Devuelve los resultados de la operación asincrónica iniciada [**por GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Volumen. Valor entre 0 y 100. 0 indica el volumen mínimo y 100 indica el volumen máximo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Comentarios

Normalmente, se llama al método **GetResults** desde el controlador de eventos que se registró estableciendo la [**propiedad Completed.**](getvolumeoperation-completed.md)

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetVolumeOperation**](getvolumeoperation.md)
</dt> </dl>

 


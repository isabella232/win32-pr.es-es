---
description: Establece el ejemplo para el origen de la secuencia multimedia.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: MÉTODO IMFMediaStreamSourceSampleRequest::SetSample
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 80430e7902f4511e85c1b472f967aec6b6cc690f1d98ca14f5c883b600e1b250
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957865"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a>MÉTODO IMFMediaStreamSourceSampleRequest::SetSample

Establece el ejemplo para el origen de la secuencia multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ En\]
</dt> <dd>

Ejemplo del origen de la secuencia multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaStreamSourceSampleRequest**](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 





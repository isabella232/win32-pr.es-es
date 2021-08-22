---
title: Método GetStreamPropertiesOperation.GetResults
description: Devuelve los resultados de la operación asincrónica iniciada por GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- Método GetResults de Media Streaming API
- Método GetResults de Media Streaming API, interfaz GetStreamPropertiesOperation
- Interfaz GetStreamPropertiesOperation de Media Streaming API, método GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3520cc44919e9c606c6625c75193b5f1ab54f4005cc098316bd8769ad0e0fe7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735826"
---
# <a name="getstreampropertiesoperationgetresults-method"></a>Método GetStreamPropertiesOperation.GetResults

Devuelve los resultados de la operación asincrónica iniciada [**por GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetStreamPropertiesOperation**](getstreampropertiesoperation.md)
</dt> </dl>

 


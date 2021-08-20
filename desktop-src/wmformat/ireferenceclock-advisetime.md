---
title: Método IReferenceClock AdviseTime
description: El método AdviseTime solicita una notificación asincrónica de que ha transcurrido un tiempo.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Método AdviseTime windows Media Format
- Método AdviseTime windows Media Format , IReferenceClock (interfaz)
- IReferenceClock interface windows Media Format , AdviseTime method
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b648c1c1305503f049b3c02669d1fa3c49be428d31c0cd292801b3541a25cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655372"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock::AdviseTime (método)

El **método AdviseTime** solicita una notificación asincrónica de que ha transcurrido un tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdviseTime(
  [in]  REFERENCE_TIME rtBaseTime,
  [in]  REFERENCE_TIME rtStreamTime,
  [in]  HEVENT         hEvent,
  [out] DWORD          *pdwAdviseCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtBaseTime* \[ En\]
</dt> <dd>

Tiempo de referencia base, en unidades de 100 nanosegundos.

</dd> <dt>

*rtStreamTime* \[ En\]
</dt> <dd>

Tiempo de desplazamiento de flujo, en unidades de 100 nanosegundos.

</dd> <dt>

*hEvent* \[ En\]
</dt> <dd>

Controlar un evento creado por el autor de la llamada. Este evento se señalará cuando transcurra el tiempo especificado.

</dd> <dt>

*pdwAdviseCookie* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud. Esto se usa para identificar esta llamada a **AdviseTime** en el futuro, por ejemplo, para cancelar la solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | El *parámetro pdwAdviseCookie* es **NULL.**<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Error no especificado.<br/>                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IReferenceClock (interfaz)**](ireferenceclock.md)
</dt> </dl>

 

 






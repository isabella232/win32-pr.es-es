---
title: IReferenceClock AdviseTime, método
description: El método AdviseTime solicita una notificación asincrónica de que ha transcurrido una hora.
ms.assetid: 8f3f8713-b53c-4110-ac7a-724bbc49368e
keywords:
- Método AdviseTime formato de Windows Media
- Método AdviseTime formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método AdviseTime
topic_type:
- apiref
api_name:
- IReferenceClock.AdviseTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fa91338b4bff8f925f00e7159a36089e0de0aa8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105720093"
---
# <a name="ireferenceclockadvisetime-method"></a>IReferenceClock:: AdviseTime (método)

El método **AdviseTime** solicita una notificación asincrónica de que ha transcurrido una hora.

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

*rtBaseTime* \[ de\]
</dt> <dd>

Tiempo de referencia base, en unidades de 100-nanosegundos.

</dd> <dt>

*rtStreamTime* \[ de\]
</dt> <dd>

Tiempo de desplazamiento de flujo, en unidades de 100-nanosegundos.

</dd> <dt>

*hEvent* \[ de\]
</dt> <dd>

Identificador de un evento creado por el autor de la llamada. Este evento se señalará cuando transcurra la hora especificada.

</dd> <dt>

*pdwAdviseCookie* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un identificador para la solicitud. Se usa para identificar esta llamada a **AdviseTime** en el futuro, por ejemplo, para cancelar la solicitud.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                             |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>                        |
| <dl> <dt>**\_puntero E**</dt> </dl> | El parámetro *pdwAdviseCookie* es **null**.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Error no especificado.<br/>                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 






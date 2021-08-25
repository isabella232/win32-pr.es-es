---
title: Método IReferenceClock GetTime
description: El método GetTime recupera la hora de referencia actual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Método GetTime windows Media Format
- Método GetTime windows Media Format , interfaz IReferenceClock
- IReferenceClock interface windows Media Format , GetTime (método)
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055445"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock::GetTime (método)

El **método GetTime** recupera la hora de referencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* \[ out\]
</dt> <dd>

Puntero a una variable que recibe la hora actual, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | El *parámetro pTime* es **NULL.**<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IReferenceClock (interfaz)**](ireferenceclock.md)
</dt> </dl>

 

 






---
title: Método IReferenceClock GetTime
description: El método GetTime recupera la hora de referencia actual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Formato multimedia de windows del método GetTime
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
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572185"
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



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IReferenceClock (interfaz)**](ireferenceclock.md)
</dt> </dl>

 

 






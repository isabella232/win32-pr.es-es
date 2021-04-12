---
title: IReferenceClock GetTime (método)
description: El método GetTime recupera la hora de referencia actual.
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- Método GetTime formato de Windows Media
- Método GetTime formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método GetTime
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419737"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock:: GetTime (método)

El método **getTime** recupera la hora de referencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTime* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe la hora actual, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                               | Descripción                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se ha llevado a cabo de forma correcta.<br/>              |
| <dl> <dt>**\_puntero E**</dt> </dl> | El parámetro *pTime* es **null**.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 






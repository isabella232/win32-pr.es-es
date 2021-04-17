---
description: Valor HRESULT que indica si el objeto aceptará ejemplos. Si el valor es S \_ OK, el objeto aceptará ejemplos. De lo contrario, rechaza los ejemplos.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Miembro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670749"
---
# <a name="coutputqueuem_hr-member"></a>Miembro COutputQueue:: m \_ HR

Valor **HRESULT** que indica si el objeto aceptará ejemplos. Si el valor es S \_ OK, el objeto aceptará ejemplos. De lo contrario, rechaza los ejemplos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT m_hr;
```



## <a name="remarks"></a>Observaciones

Esta variable miembro se utiliza para coordinar las actividades entre subprocesos. Si el PIN de entrada de nivel inferior rechaza un ejemplo o si el objeto comienza a vaciarse, el valor se establece en S \_ false o en un código de error. El objeto no proporcionará más muestras hasta que se complete el vaciado o hasta que se llame al método [**COutputQueue:: RESET**](coutputqueue-reset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 





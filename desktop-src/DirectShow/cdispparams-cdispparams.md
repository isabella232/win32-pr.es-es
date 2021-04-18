---
description: Método de constructor.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructor CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680499"
---
# <a name="cdispparamscdispparams-constructor"></a>Constructor CDispParams. CDispParams

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nArgs* 
</dt> <dd>

Número de argumentos pasados al método o a la propiedad.

</dd> <dt>

*pArgs* 
</dt> <dd>

Puntero a la lista de argumentos. En la lista, cada argumento se almacena con su tipo variante.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDispParams**](cdispparams.md)
</dt> </dl>

 

 





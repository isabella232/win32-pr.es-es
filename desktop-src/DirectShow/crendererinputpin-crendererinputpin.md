---
description: El método CRendererInputPin es un método de constructor.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Constructor CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671705"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Constructor CRendererInputPin. CRendererInputPin

El `CRendererInputPin` método es un método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRenderer* 
</dt> <dd>

Puntero al objeto [**CBaseRenderer**](cbaserenderer.md) que implementa el filtro.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor **HRESULT** .

</dd> <dt>

*Nombre* 
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene el identificador del PIN.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CRendererInputPin**](crendererinputpin.md)
</dt> </dl>

 

 





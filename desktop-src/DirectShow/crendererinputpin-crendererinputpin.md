---
description: El método CRendererInputPin es un método de constructor.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Constructor CRendererInputPin.CRendererInputPin (Renbase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062380"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a>Constructor CRendererInputPin.CRendererInputPin

El `CRendererInputPin` método es un método constructor.

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

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un **valor HRESULT.**

</dd> <dt>

*Nombre* 
</dt> <dd>

Puntero a una cadena de caracteres anchos que contiene el identificador de pin.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 





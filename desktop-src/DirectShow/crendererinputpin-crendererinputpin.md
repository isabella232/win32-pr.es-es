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
ms.openlocfilehash: 2b6970b056706e7443cc38793a9c050d4f93c5ebd86556ce58aff23d4e9e83e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079325"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 





---
description: El método CompleteConnect completa una conexión a un pin de salida. Este método invalida el método CBasePin::CompleteConnect.
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Método CRendererInputPin.CompleteConnect (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061713"
---
# <a name="crendererinputpincompleteconnect-method"></a>Método CRendererInputPin.CompleteConnect

El `CompleteConnect` método completa una conexión a un pin de salida. Este método invalida el [**método CBasePin::CompleteConnect.**](cbasepin-completeconnect.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CRendererInputPin (clase)**](crendererinputpin.md)
</dt> </dl>

 

 





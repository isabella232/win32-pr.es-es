---
description: 'Método CDynamicOutputPin.CompleteConnect: el método CompleteConnect completa una conexión a un pin de entrada.'
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Método CDynamicOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061740"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a>Método CDynamicOutputPin.CompleteConnect

El `CompleteConnect` método completa una conexión a un pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBaseOutputPin::CompleteConnect.**](cbaseoutputpin-completeconnect.md) Para admitir reconexiones dinámicas, este método confirma el asignador si el filtro está activo. En la clase base, las conexiones solo pueden producirse cuando se detiene el filtro, por lo que el asignador siempre se confirma en el método [**CBaseOutputPin::Active.**](cbaseoutputpin-active.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 





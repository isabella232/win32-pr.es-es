---
description: El método DecideAllocator selecciona un asignador de memoria.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Método CBaseOutputPin. DecideAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660795"
---
# <a name="cbaseoutputpindecideallocator-method"></a>CBaseOutputPin. DecideAllocator, método

El `DecideAllocator` método selecciona un asignador de memoria.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) del PIN de entrada.

</dd> <dt>

*pAlloc* 
</dt> <dd>

Dirección de una variable que recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Se llama a este método al final del proceso de conexión del PIN. Realiza los pasos siguientes:

1.  Llama al método [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) para recuperar los requisitos de búfer del PIN de entrada, si existe.
2.  Llama al método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) para solicitar un asignador del PIN de entrada. Si el PIN de entrada no proporciona un asignador, el PIN de salida crea uno llamando al método de la clase [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) .
3.  Llama al método de clase [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que establece las propiedades de asignador. Este es un método virtual puro; la clase derivada debe implementarla.
4.  Llama al método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) , que notifica a la clavija de entrada que se está usando el asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 





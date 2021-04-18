---
description: 'El método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin:: GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin. GetAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679260"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>CTransInPlaceInputPin. GetAllocator, método

El `GetAllocator` método recupera el asignador de memoria propuesto por este pin. Este método implementa el método [**IMemInputPin:: GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Recibe un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                          | Descripción                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                 | Correcto.<br/>                   |
| <dl> <dt>**VFW \_ E \_ no \_ asignador**</dt> </dl> | No hay ningún asignador disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

Si el PIN de salida del filtro está conectado, este método solicita un asignador del PIN de entrada del filtro de nivel inferior.

Si el PIN de salida del filtro no está conectado, este método crea un asignador temporal. Más adelante, cuando el PIN de salida esté conectado, el filtro volverá a conectar el PIN de entrada y renegociará el asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 





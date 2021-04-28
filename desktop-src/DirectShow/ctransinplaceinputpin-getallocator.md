---
description: 'Método CTransInPlaceInputPin.GetAllocator: el método GetAllocator recupera el asignador de memoria propuesto por este pin. Este método implementa el método IMemInputPin::GetAllocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin.GetAllocator (Transip.h)
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
ms.openlocfilehash: 2472630d69119f33653d831386af615718274d99
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084663"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Método CTransInPlaceInputPin.GetAllocator

El `GetAllocator` método recupera el asignador de memoria propuesto por este pin. Este método implementa el [**método IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

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

Recibe un puntero a la interfaz [**IMemAllocator del**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                          | Descripción                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Correcto.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | No hay ningún asignador disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Si el pin de salida del filtro está conectado, este método solicita un asignador del pin de entrada del filtro de bajada.

Si el pin de salida del filtro no está conectado, este método crea un asignador temporal. Más adelante, cuando el pin de salida esté conectado, el filtro volverá a conectar el pin de entrada y volverá a negociar el asignador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 





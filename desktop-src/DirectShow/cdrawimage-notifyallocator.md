---
description: El método NotifyAllocator informa al objeto CDrawImage de si el asignador de la conexión es un objeto CImageAllocator.
ms.assetid: cc1604e7-f755-4a7a-9294-6fd06bb434d4
title: Método CDrawImage. NotifyAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7bab7d1d00b70317a7cbb0b79f8a430a603a757
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680947"
---
# <a name="cdrawimagenotifyallocator-method"></a>CDrawImage. NotifyAllocator, método

El `NotifyAllocator` método informa al objeto **CDrawImage** de si el asignador de la conexión es un objeto [**CImageAllocator**](cimageallocator.md) .

## <a name="syntax"></a>Sintaxis


```C++
void NotifyAllocator(
   BOOL bUsingImageAllocator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bUsingImageAllocator* 
</dt> <dd>

Valor booleano que indica el tipo de asignador que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método después de que los pin acepten un asignador. Si el filtro sabe que el asignador es un objeto **CImageAllocator** , debe llamar a este método con el valor **true**. (Normalmente, el filtro solo lo sabrá si posee el asignador en cuestión). De lo contrario, debería llamar a este método con el valor **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::D rawImage**](cdrawimage-drawimage.md)
</dt> </dl>

 

 





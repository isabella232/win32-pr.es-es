---
description: El método NotifyMediaType notifica al objeto CDrawImage del tipo de medio actual.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Método CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680946"
---
# <a name="cdrawimagenotifymediatype-method"></a>CDrawImage. NotifyMediaType, método

El `NotifyMediaType` método notifica al objeto **CDrawImage** del tipo de medio actual.

## <a name="syntax"></a>Sintaxis


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntero a un objeto [**CMediaType**](cmediatype.md) o **null** para borrar el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método cada vez que cambie el tipo de medio. Normalmente esto se produce cuando el PIN se conecta por primera vez y después de un cambio de formato dinámico.

El objeto **CDrawImage** almacena el puntero *pMediaType* en la variable miembro **m \_ pMediaType** . Por consiguiente, si el autor de la llamada necesita liberar el objeto **CMediaType** , debe actualizar el objeto **CDrawImage** llamando de nuevo a este método, ya sea con un puntero nuevo o con un valor **null** . De lo contrario, se puede producir un error cuando el objeto **CDrawImage** intenta hacer referencia al puntero anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 





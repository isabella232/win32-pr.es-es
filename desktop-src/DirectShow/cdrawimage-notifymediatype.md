---
description: El método NotifyMediaType notifica al objeto CDrawImage del tipo de medio actual.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Método CDrawImage.NotifyMediaType (Winutil.h)
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
ms.openlocfilehash: 3df1f904bb5c2acfc328e8779da6135f901de9601cea6735de21b2e76aeea9c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656796"
---
# <a name="cdrawimagenotifymediatype-method"></a>Método CDrawImage.NotifyMediaType

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

Puntero a un [**objeto CMediaType**](cmediatype.md) o **NULL** para borrar el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El filtro propietario debe llamar a este método siempre que cambie el tipo de medio. Normalmente esto sucede cuando el pin se conecta por primera vez y después de un cambio de formato dinámico.

El **objeto CDrawImage** almacena el *puntero pMediaType* en la variable **miembro m \_ pMediaType.** Por lo tanto, si el autor de la llamada necesita liberar el objeto **CMediaType,** debe actualizar el objeto **CDrawImage** llamando de nuevo a este método, ya sea con un nuevo puntero o con un **valor NULL.** De lo contrario, se puede producir un error **cuando el objeto CDrawImage** intenta hacer referencia al puntero antiguo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 





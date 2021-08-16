---
description: El método RemoveI quita el elemento en la posición especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList.RemoveI (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac3277f30e959e42cf2fd2d1aeeb13f81cb17515abb8434a8ae13406d244aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823742"
---
# <a name="cbaselistremovei-method"></a>Método CBaseList.RemoveI

El `RemoveI` método quita el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Valor POSITION que indica el elemento que se quitará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero al elemento.

## <a name="remarks"></a>Comentarios

Este método elimina el nodo de la lista, pero no elimina el elemento contenido en ese nodo.

Si *pos* es **NULL,** el método devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseList (clase)**](cbaselist.md)
</dt> </dl>

 

 





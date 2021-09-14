---
description: El método GetSourceRect recupera el rectángulo de origen actual.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Método CDrawImage.GetSourceRect (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061288"
---
# <a name="cdrawimagegetsourcerect-method"></a>Método CDrawImage.GetSourceRect

El `GetSourceRect` método recupera el rectángulo de origen actual.

## <a name="syntax"></a>Sintaxis


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntero a una **estructura RECT** que recibe el rectángulo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDrawImage (clase)**](cdrawimage.md)
</dt> </dl>

 

 





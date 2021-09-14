---
description: Recupera el identificador de eventos. Este operador no se admite como un valor L.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Método HANDLE DE USOEvent.operator (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161648"
---
# <a name="cameventoperator-handle-method"></a>Método HANDLE de CAMEvent.operator

Recupera el identificador de eventos. Este operador no se admite como un valor L.

## <a name="syntax"></a>Sintaxis


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro DEEVENT::m \_ hEvent.**](camevent-m-hevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 





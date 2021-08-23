---
description: Recupera el identificador de evento. Este operador no se admite como valor L.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Método HANDLE DE CAMEvent.operator (Wxutil.h)
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
ms.openlocfilehash: afc3bcc1044d3d14b7ebf77ce12027fb3b772185f62b917fce7b74fbb3fa7e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689335"
---
# <a name="cameventoperator-handle-method"></a>Método HANDLE de CAMEvent.operator

Recupera el identificador de evento. Este operador no se admite como valor L.

## <a name="syntax"></a>Sintaxis


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro CAMEvent::m \_ hEvent.**](camevent-m-hevent.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMEvent**](camevent.md)
</dt> </dl>

 

 





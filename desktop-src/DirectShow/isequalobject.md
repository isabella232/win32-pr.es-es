---
description: La función IsEqualObject comprueba si dos interfaces están en el mismo objeto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Función IsEqualObject (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e385cf887dceddcdc470b908d46f59405f573ab47837b26f8453ce6154eb0d72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817464"
---
# <a name="isequalobject-function"></a>Función IsEqualObject

La `IsEqualObject` función comprueba si dos interfaces están en el mismo objeto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFirst* 
</dt> <dd>

Puntero a una interfaz.

</dd> <dt>

*pSecond* 
</dt> <dd>

Puntero a la otra interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si las interfaces están en el mismo objeto o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 





---
description: Cambia la marca de des dirty para la secuencia actual.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Método CPersistStream.SetDirty (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a00de873f33cedd1451ebebd0ec21f1dfaa83690923712d867ec4a8d34d502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909305"
---
# <a name="cpersiststreamsetdirty-method"></a>Método CPersistStream.SetDirty

Cambia la marca de des dirty para la secuencia actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fDirty* 
</dt> <dd>

Nueva marca desnuciada para esta secuencia. **TRUE** significa que los datos no se han guardado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 





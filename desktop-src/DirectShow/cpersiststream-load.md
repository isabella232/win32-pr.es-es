---
description: Carga los datos del filtro desde una secuencia determinada.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Método CPersistStream.Load (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d65ff2d2ba95f66e6153aa78a9ce376ed144ac24ce8945c1fbc678e9f6894802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813355"
---
# <a name="cpersiststreamload-method"></a>Método CPersistStream.Load

Carga los datos del filtro desde una secuencia determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStm* 
</dt> <dd>

Puntero a la secuencia desde la que se va a cargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Esta función miembro implementa el **método IPersistStream::Load.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pstream.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPersistStream (clase)**](cpersiststream.md)
</dt> </dl>

 

 





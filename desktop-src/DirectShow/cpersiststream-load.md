---
description: Carga los datos del filtro desde una secuencia determinada.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Método CPersistStream. Load (pStream. h)
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
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670998"
---
# <a name="cpersiststreamload-method"></a>CPersistStream. Load (método)

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

Puntero a la secuencia de la que se va a cargar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método **IPersistStream:: Load** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 





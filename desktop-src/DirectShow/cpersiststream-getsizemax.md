---
description: Recupera el tamaño máximo de bytes necesario para la secuencia actual, incluido el número de versión.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Método CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671001"
---
# <a name="cpersiststreamgetsizemax-method"></a>CPersistStream. GetSizeMax, método

Recupera el tamaño máximo de bytes necesario para la secuencia actual, incluido el número de versión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PCB* 
</dt> <dd>

Puntero al tamaño en bytes necesario para guardar este flujo, incluido el número de versión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método **IPersistStream:: GetSizeMax** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 





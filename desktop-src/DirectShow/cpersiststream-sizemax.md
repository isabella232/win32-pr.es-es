---
description: Recupera el tamaño máximo de bytes necesario para la secuencia actual, sin incluir el número de versión.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Método CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670995"
---
# <a name="cpersiststreamsizemax-method"></a>CPersistStream. SizeMax, método

Recupera el tamaño máximo de bytes necesario para la secuencia actual, sin incluir el número de versión.

## <a name="syntax"></a>Sintaxis


```C++
virtual int SizeMax();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes necesarios para los datos, sin incluir el número de versión.

## <a name="remarks"></a>Observaciones

La versión predeterminada devuelve cero; se debe invalidar para proporcionar algún otro valor adecuado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PStream. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPersistStream**](cpersiststream.md)
</dt> </dl>

 

 





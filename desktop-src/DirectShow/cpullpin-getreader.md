---
description: El método GetReader devuelve un puntero a la interfaz IAsyncReader del terminal de salida.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Método CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671385"
---
# <a name="cpullpingetreader-method"></a>CPullPin. GetReader, método

El `GetReader` método devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del terminal de salida.

## <a name="syntax"></a>Sintaxis


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

## <a name="remarks"></a>Observaciones

La interfaz devuelta tiene un recuento de referencias pendiente. El llamador debe liberar la interfaz.

El método no comprueba el valor del puntero de interfaz antes de llamar a **AddRef**, por lo que no debe llamarlo hasta que se haya llamado correctamente al método [**CPullPin:: Connect**](cpullpin-connect.md) . De lo contrario, el puntero de interfaz podría ser **null** y llamar a **AddRef** producirá una excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPullPin**](cpullpin.md)
</dt> </dl>

 

 





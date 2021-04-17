---
description: El método Reset restablece el objeto para que pueda recibir más datos.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Método COutputQueue. Reset (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678973"
---
# <a name="coutputqueuereset-method"></a>COutputQueue. Reset (método)

El `Reset` método restablece el objeto para que pueda recibir más datos.

## <a name="syntax"></a>Sintaxis


```C++
void Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método restablece la variable miembro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) a S \_ OK. El objeto puede volver a recibir ejemplos de medios; por ejemplo, después de una operación de vaciado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Outputq. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 





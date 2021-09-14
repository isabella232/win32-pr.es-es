---
description: El método GetPositions recupera la posición actual y la posición de detenerse, con respecto a la duración total de la secuencia. Este método implementa el método IMediaSeeking::GetPositions.
ms.assetid: 51e45bc3-ae30-4b05-b9d9-684c1b028f51
title: Método CPosPassThru.GetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0852199e8e143ce5b0348c3b79afd495a5a47627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255471"
---
# <a name="cpospassthrugetpositions-method"></a>Método CPosPassThru.GetPositions

El `GetPositions` método recupera la posición actual y la posición de detenerse, con respecto a la duración total de la secuencia. Este método implementa el [**método IMediaSeeking::GetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPositions(
   LONGLONG *pCurrent,
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que recibe la posición actual, en unidades del formato de hora actual.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que recibe la posición de detenerse, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





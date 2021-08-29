---
description: 'Método CPosPassThru.GetDuration: el método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking::GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0a7ca3a2ce97605b34a8379e262df0a35da01a93fbfa0a7e995b209ade6ee763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108295"
---
# <a name="cpospassthrugetduration-method"></a>Método CPosPassThru.GetDuration

El `GetDuration` método recupera la duración de la secuencia. Este método implementa el [**método IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDuration* 
</dt> <dd>

Puntero a una variable que recibe la duración, en unidades del formato de hora actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> </dl>

 

 





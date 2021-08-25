---
description: 'Método CPosPassThru.SetPositions: el método SetPositions establece la posición actual y la posición de detenerse. Este método implementa el método IMediaSeeking::SetPositions.'
ms.assetid: d4425221-e20f-4e51-8a33-a74fa21f9117
title: Método CPosPassThru.SetPositions (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetPositions
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d5ed5a25c5ceb4cbe96571ef83945fdf5edd1bbd373de875f7339c13c1b43dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909195"
---
# <a name="cpospassthrusetpositions-method"></a>Método CPosPassThru.SetPositions

El `SetPositions` método establece la posición actual y la posición de detenerse. Este método implementa el [**método IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPositions(
   LONGLONG *pCurrent,
   DWORD    dwCurrentFlags,
   LONGLONG *pStop,
   DWORD    dwStopFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntero a una variable que especifica la posición actual, en unidades del formato de hora actual.

</dd> <dt>

*dwCurrentFlags* 
</dt> <dd>

Combinación bit a bit de marcas. Consulte [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que especifica la hora de detenerse, en unidades del formato de hora actual.

</dd> <dt>

*dwStopFlags* 
</dt> <dd>

Combinación bit a bit de marcas. Consulte [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para obtener más información.

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

 

 





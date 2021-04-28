---
description: 'Método CPosPassThru.GetTimeFormat: el método GetTimeFormat recupera el formato de hora actual. Este método implementa el método IMediaSeeking::GetTimeFormat.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Método CPosPassThru.GetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 903d1c6163d4cad5c5b9ca22213b02542bb3da49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085593"
---
# <a name="cpospassthrugettimeformat-method"></a>Método CPosPassThru.GetTimeFormat

El `GetTimeFormat` método recupera el formato de hora actual. Este método implementa el [**método IMediaSeeking::GetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a una variable que recibe un GUID de formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **valor HRESULT** del pin conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> <dt>

[**GUID de formato de hora**](time-format-guids.md)
</dt> </dl>

 

 





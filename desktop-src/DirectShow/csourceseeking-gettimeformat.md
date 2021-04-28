---
description: 'Método CSourceSeeking.GetTimeFormat: el método GetTimeFormat recupera el formato de hora actual. Este método implementa el método IMediaSeeking::GetTimeFormat.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Método CSourceSeeking.GetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085223"
---
# <a name="csourceseekinggettimeformat-method"></a>Método CSourceSeeking.GetTimeFormat

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

Puntero a una variable que recibe un GUID de formato de hora. Consulte [**GUID de formato de hora.**](time-format-guids.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Valor de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





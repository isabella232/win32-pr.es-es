---
description: 'Método CPosPassThru.SetTimeFormat: el método SetTimeFormat establece el formato de hora. Este método implementa el método IMediaSeeking::SetTimeFormat.'
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Método CPosPassThru.SetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085473"
---
# <a name="cpospassthrusettimeformat-method"></a>Método CPosPassThru.SetTimeFormat

El método SetTimeFormat establece el formato de hora. Este método implementa el [**método IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a un GUID de formato de hora.

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

 

 





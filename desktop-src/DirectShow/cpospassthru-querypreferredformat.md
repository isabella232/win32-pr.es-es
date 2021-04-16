---
description: 'El método QueryPreferredFormat recupera el formato de hora preferido para la secuencia. Este método implementa el método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Método CPosPassThru. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680219"
---
# <a name="cpospassthruquerypreferredformat-method"></a>CPosPassThru. QueryPreferredFormat, método

El `QueryPreferredFormat` método recupera el formato de hora preferido para la secuencia. Este método implementa el método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a una variable que recibe un GUID con formato de hora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor **HRESULT** del PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CPosPassThru**](cpospassthru.md)
</dt> <dt>

[**GUID de formato de hora**](time-format-guids.md)
</dt> </dl>

 

 





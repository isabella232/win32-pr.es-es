---
description: El método QueryPreferredFormat recupera el formato de hora preferido para la secuencia. Este método implementa el método IMediaSeeking::QueryPreferredFormat.
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Método CPosPassThru.QueryPreferredFormat (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070059"
---
# <a name="cpospassthruquerypreferredformat-method"></a>Método CPosPassThru.QueryPreferredFormat

El `QueryPreferredFormat` método recupera el formato de hora preferido para la secuencia. Este método implementa el método [**IMediaSeeking::QueryPreferredFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)

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

Puntero a una variable que recibe un GUID de formato de hora.

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
</dt> <dt>

[**GUID de formato de hora**](time-format-guids.md)
</dt> </dl>

 

 





---
description: El método QueryPreferredFormat recupera el formato de hora preferido del objeto. Este método implementa el método IMediaSeeking::QueryPreferredFormat.
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Método CSourceSeeking.QueryPreferredFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fb311181adf1e36a8f1e46a467cf801de0dcc6d1caaf09a890eb06e43726d04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053945"
---
# <a name="csourceseekingquerypreferredformat-method"></a>Método CSourceSeeking.QueryPreferredFormat

El `QueryPreferredFormat` método recupera el formato de hora preferido del objeto. Este método implementa el [**método IMediaSeeking::QueryPreferredFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)

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

Puntero a una variable que recibe un GUID de formato de hora. Consulte [**GUID de formato de hora**](time-format-guids.md).

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
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





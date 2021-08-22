---
description: El método IsUsingTimeFormat determina si un formato de hora especificado es el formato actualmente en uso. Este método implementa el método IMediaSeeking::IsUsingTimeFormat.
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Método CPosPassThru.IsUsingTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64c240a0b1c269dde57e07e50bcbdbbd4d5d7e03d24a4e6d263662947f3d65de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954014"
---
# <a name="cpospassthruisusingtimeformat-method"></a>Método CPosPassThru.IsUsingTimeFormat

El `IsUsingTimeFormat` método determina si un formato de hora especificado es el formato actualmente en uso. Este método implementa el [**método IMediaSeeking::IsUsingTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUsingTimeFormat(
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
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CPosPassThru (clase)**](cpospassthru.md)
</dt> <dt>

[**GUID de formato de hora**](time-format-guids.md)
</dt> </dl>

 

 





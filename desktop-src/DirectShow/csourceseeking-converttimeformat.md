---
description: 'Método CSourceSeeking.ConvertTimeFormat: el método ConvertTimeFormat convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking::ConvertTimeFormat.'
ms.assetid: d0cb44fa-30c1-41b4-92a4-7169161e3140
title: Método CSourceSeeking.ConvertTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba5c6808e091f48baac7d8928e327f45773e13a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973845"
---
# <a name="csourceseekingconverttimeformat-method"></a>Método CSourceSeeking.ConvertTimeFormat

El `ConvertTimeFormat` método convierte de un formato de hora a otro. Este método implementa el [**método IMediaSeeking::ConvertTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertTimeFormat(
         LONGLONG *pTarget,
   const GUID     *pTargetFormat,
         LONGLONG Source,
   const GUID     *pSourceFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTarget* 
</dt> <dd>

Puntero a una variable que recibe la hora convertida.

</dd> <dt>

*pTargetFormat* 
</dt> <dd>

Puntero al GUID del formato de destino. Si **es NULL,** se usa el formato actual. Consulte [**GUID de formato de hora**](time-format-guids.md).

</dd> <dt>

*Origen* 
</dt> <dd>

Valor de tiempo que se va a convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntero al GUID de formato de hora del formato que se convertirá. Si **es NULL,** se usa el formato actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                                  | Descripción                          |
|----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido<br/>          |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Observaciones

El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos). Este método devuelve E INVALIDARG, excepto en el caso trivial en el que \_ *pTargetFormat* y *pSourceFormat* especifican TIME \_ FORMAT MEDIA \_ \_ TIME.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





---
description: 'Método CPosPassThru.ConvertTimeFormat: el método ConvertTimeFormat se convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking::ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru.ConvertTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ConvertTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2382d36899bf7e3ac85e217502a878497274604ced4b77cf7acbc1465586c487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954124"
---
# <a name="cpospassthruconverttimeformat-method"></a>Método CPosPassThru.ConvertTimeFormat

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

Puntero al GUID de formato de hora del formato de destino. Si **es NULL,** se usa el formato actual.

</dd> <dt>

*Origen* 
</dt> <dd>

Valor de hora que se va a convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntero al GUID de formato de hora del formato que se convertirá. Si **es NULL,** se usa el formato actual.

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

 

 





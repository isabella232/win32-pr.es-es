---
description: 'El método ConvertTimeFormat convierte de un formato de hora a otro. Este método implementa el método IMediaSeeking:: ConvertTimeFormat.'
ms.assetid: e766d112-ee41-4c64-a735-b6317093518a
title: Método CPosPassThru. ConvertTimeFormat (Ctlutil. h)
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
ms.openlocfilehash: bcce3e24c46e3e59c6bad6b4fbd60b139806de73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680473"
---
# <a name="cpospassthruconverttimeformat-method"></a>CPosPassThru. ConvertTimeFormat, método

El `ConvertTimeFormat` método convierte de un formato de hora a otro. Este método implementa el método [**IMediaSeeking:: ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat) .

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

Puntero al GUID del formato de hora del formato de destino. Si es **null**, se usa el formato actual.

</dd> <dt>

*Origen* 
</dt> <dd>

Valor de hora que se va a convertir.

</dd> <dt>

*pSourceFormat* 
</dt> <dd>

Puntero al GUID del formato de hora del formato que se va a convertir. Si es **null**, se usa el formato actual.

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

 

 





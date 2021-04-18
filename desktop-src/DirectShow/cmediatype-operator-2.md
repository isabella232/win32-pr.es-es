---
description: Este operador sobrecarga el operador de asignación para copiar un tipo de medio.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: Operator = método (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690866"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a>CMediaType. CMediaType:: Operator = método (mtype. h)

Este operador sobrecarga el operador de asignación para copiar un tipo de medio.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtype* \[ CLI\]
</dt> <dd>

Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una referencia al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





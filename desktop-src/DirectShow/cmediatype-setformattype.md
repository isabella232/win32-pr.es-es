---
description: El método SetFormatType especifica el tipo de formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Método CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671223"
---
# <a name="cmediatypesetformattype-method"></a>CMediaType. SetFormatType, método

El método ' ' SetFormatType especifica el tipo de formato.

## <a name="syntax"></a>Sintaxis


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pformattype* 
</dt> <dd>

Puntero a un **GUID** que especifica el tipo de formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método establece el miembro **formatType** . El tipo de formato define el diseño del bloque de formato. Por ejemplo, si el tipo de formato es FORMAT \_ info, el bloque de formato debe contener una estructura **VIDEOINFOHEADER** . Para establecer el bloque de formato, llame al método [**CMediaType:: SetFormat**](cmediatype-setformat.md) . El autor de la llamada es responsable de asegurarse de que el bloque de formato coincide con el tipo de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 


``

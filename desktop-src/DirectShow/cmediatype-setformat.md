---
description: El método SetFormat inicializa el bloque de formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Método CMediaType. SetFormat (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680483"
---
# <a name="cmediatypesetformat-method"></a>CMediaType. SetFormat, método

El `SetFormat` método inicializa el bloque de formato.

## <a name="syntax"></a>Sintaxis


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a un bloque de memoria que contiene el bloque de formato.

</dd> <dt>

*length* 
</dt> <dd>

Longitud del bloque de formato, en bytes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto, o **false** si se produjo un error.

## <a name="remarks"></a>Observaciones

Este método asigna memoria para el bloque de formato y copia el búfer especificado por *pFormat* en el nuevo bloque de formato. Si el tipo de medio ya contiene un bloque de formato, se libera el anterior. El método también establece el miembro **cbFormat** de la estructura de **\_ \_ tipo de medio am** .

Para establecer el tipo de formato, llame al método [**CMediaType:: SetFormatType**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





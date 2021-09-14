---
description: El método SetFormat inicializa el bloque de formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Método CMediaType.SetFormat (Mtype.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362495"
---
# <a name="cmediatypesetformat-method"></a>Método CMediaType.SetFormat

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

Devuelve **TRUE si** se realiza correctamente o **FALSE** si se produjo un error.

## <a name="remarks"></a>Observaciones

Este método asigna memoria para el bloque de formato y copia el búfer especificado por *pFormat* en el nuevo bloque de formato. Si el tipo de medio ya contiene un bloque de formato, se libera el anterior. El método también establece el **miembro cbFormat** de la **estructura AM MEDIA \_ \_ TYPE.**

Para establecer el tipo de formato, llame [**al método CMediaType::SetFormatType.**](cmediatype-setformattype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





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
ms.openlocfilehash: 99726a466b6bf273b654a5d459fa2391a75882f1adee64b981d91a514a988b88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108455"
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

## <a name="remarks"></a>Comentarios

Este método asigna memoria para el bloque de formato y copia el búfer especificado por *pFormat* en el nuevo bloque de formato. Si el tipo de medio ya contiene un bloque de formato, se libera el anterior. El método también establece el **miembro cbFormat** de la **estructura AM MEDIA \_ \_ TYPE.**

Para establecer el tipo de formato, llame [**al método CMediaType::SetFormatType.**](cmediatype-setformattype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





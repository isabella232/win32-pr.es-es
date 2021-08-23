---
description: El método SetFormatType especifica el tipo de formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Método CMediaType.SetFormatType (Mtype.h)
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
ms.openlocfilehash: f6a0582a882ffe40a9bd889ff48e70a52a4048bad57e01077263e607f13d9898
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954424"
---
# <a name="cmediatypesetformattype-method"></a>Método CMediaType.SetFormatType

El método ''SetFormatType especifica el tipo de formato.

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

## <a name="remarks"></a>Comentarios

Este método establece el **miembro formattype.** El tipo de formato define el diseño del bloque de formato. Por ejemplo, si el tipo de formato es FORMAT \_ VideoInfo, el bloque de formato debe contener una **estructura VIDEOINFOHEADER.** Para establecer el bloque de formato, llame [**al método CMediaType::SetFormat.**](cmediatype-setformat.md) El autor de la llamada es responsable de asegurarse de que el bloque de formato coincide con el tipo de formato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 


``

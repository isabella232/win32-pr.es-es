---
description: Obtenga información sobre el método del constructor CMediaType.CMediaType (Mtype.h). Este método usa el parámetro 'majortype'.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: 'Constructor CMediaType.CMediaType (Mtype.h): parámetro majortype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b1ebf3cec41c4180a4dcad4a5a7c273996f70bfdb6d052127ff71dd1b929238c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073999"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Constructor CMediaType.CMediaType (Mtype.h): parámetro majortype

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*majortype* 
</dt> <dd>

Puntero a un GUID de tipo **principal.** El constructor inicializa el GUID de tipo principal en este valor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El constructor llama al [**método CMediaType::InitMediaType para**](cmediatype-initmediatype.md) inicializar el tipo de medio.

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype.h (incluir Secuencias.h)                                                                                     |
| Biblioteca | Strmbase.lib (compilaciones comerciales); Strmbasd.lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





---
description: 'Constructor CMediaType.CMediaType (Mtype.h): método constructor.'
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Constructor CMediaType.CMediaType (Mtype.h): parámetros cmtype y phr'
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
ms.openlocfilehash: 2f686d1338073c65ce3e5bc3871ae8f4a5b9102e78d7678d5bcf6f77a565397d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792955"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Constructor CMediaType.CMediaType (Mtype.h)

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cmtype* \[ Ref\]
</dt> <dd>

Referencia a un `CMediaType` objeto . El constructor copia el tipo de medio en el nuevo objeto, incluido el bloque de formato, si lo hay.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT. Este parámetro puede ser un **puntero NULL.** De lo contrario, el autor de la llamada debe establecer el valor en S \_ OK antes de llamar al constructor. Si se produce un error en el constructor, establece el valor en un código de error.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El constructor llama al [**método CMediaType::InitMediaType para**](cmediatype-initmediatype.md) inicializar el tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





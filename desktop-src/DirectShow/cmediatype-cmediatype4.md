---
description: Método de constructor.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Constructor CMediaType. CMediaType (mtype. h)
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
ms.openlocfilehash: 776d59550d09396cc248937be611f2b4ec3699df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689938"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Constructor CMediaType. CMediaType (mtype. h)

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cmtype* \[ CLI\]
</dt> <dd>

Referencia a un `CMediaType` objeto. El constructor copia el tipo de archivo multimedia en el nuevo objeto, incluido el bloque de formato, si existe.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT. Este parámetro puede ser un puntero **nulo** . De lo contrario, el autor de la llamada debe establecer el valor en es \_ correcto antes de llamar al constructor. Si se produce un error en el constructor, establece el valor en un código de error.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El constructor llama al método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de archivo multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





---
description: Obtenga información sobre el método CMediaType. CMediaType constructor (mtype. h). Este método usa los parámetros ' mtype ' y ' PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: 'Constructor CMediaType. CMediaType (mtype. h): parámetros mtype y PHR'
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105670279"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Constructor CMediaType. CMediaType (mtype. h): parámetros mtype y PHR

Método de constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtype* \[ CLI\]
</dt> <dd>

Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . El constructor copia el tipo de archivo multimedia en el nuevo objeto, incluido el bloque de formato, si existe.

</dd> <dt>

*phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT. Este parámetro puede ser un puntero **nulo** . De lo contrario, el autor de la llamada debe establecer el valor en es \_ correcto antes de llamar al constructor. Si se produce un error en el constructor, establece el valor en un código de error.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El constructor llama al método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de archivo multimedia.

## <a name="requirements"></a>Requisitos

| Requisito                   | Value                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado  | Mtype. h (incluir streams. h)                                                                                     |
| Biblioteca | Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





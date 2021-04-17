---
description: Obtenga información sobre el método CMediaType. CMediaType constructor (mtype. h). Este método usa el parámetro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: 'Constructor CMediaType. CMediaType (mtype. h): parámetro majortype'
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
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678864"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a>Constructor CMediaType. CMediaType (mtype. h): parámetro majortype

Método de constructor.

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

Puntero a un **GUID** de tipo principal. El constructor inicializa el GUID de tipo principal en este valor.

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

 

 





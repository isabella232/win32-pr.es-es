---
description: Obtenga información sobre el método del constructor CMediaType.CMediaType (Mtype.h). Este método usa los parámetros "mtype" y "phr".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: 'Constructor CMediaType.CMediaType (Mtype.h): parámetros mtype y phr'
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
ms.openlocfilehash: 0c399073794f025122e1cfade3f15b3a96784f28e171482e4dcfb7bcec6a8271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084485"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Constructor CMediaType.CMediaType (Mtype.h): parámetros mtype y phr

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mtype* \[ Ref\]
</dt> <dd>

Referencia a una [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) El constructor copia el tipo de medio en el nuevo objeto, incluido el bloque de formato, si lo hubiera.

</dd> <dt>

*Phr* 
</dt> <dd>

Puntero a una variable que recibe un valor HRESULT. Este parámetro puede ser un **puntero NULL.** De lo contrario, el autor de la llamada debe establecer el valor en S \_ OK antes de llamar al constructor. Si se produce un error en el constructor, establece el valor en un código de error.

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

 

 





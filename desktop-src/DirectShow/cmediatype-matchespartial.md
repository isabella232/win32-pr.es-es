---
description: El método MatchesPartial determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Método CMediaType.MatchesPartial (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6049ad4526d8776b25e81fe4d75b727196f8fa1251a1959662cca71b161fbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073979"
---
# <a name="cmediatypematchespartial-method"></a>Método CMediaType.MatchesPartial

El método determina si este tipo de medio coincide con un tipo de medio especificado `MatchesPartial` parcialmente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppartial* 
</dt> <dd>

Puntero al tipo de medio que se debe coincidir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** los tipos de medios coinciden. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

El tipo de medio especificado por *ppartial* puede tener un valor de GUID NULL para el tipo \_ principal, subtipo o tipo de formato. No se prueban los miembros \_ con valores NULL guid. (En efecto, GUID \_ NULL actúa como un carácter comodín). Los miembros con valores distintos de GUID \_ NULL deben coincidir para que el tipo de medio coincida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





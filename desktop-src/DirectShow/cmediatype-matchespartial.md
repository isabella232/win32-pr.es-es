---
description: El método MatchesPartial determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Método CMediaType. MatchesPartial (mtype. h)
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
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671311"
---
# <a name="cmediatypematchespartial-method"></a>CMediaType. MatchesPartial, método

El `MatchesPartial` método determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.

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

Puntero al tipo de medio que debe coincidir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si los tipos de medios coinciden. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

El tipo de medio especificado por *ppartial* puede tener un valor de GUID \_ null para el tipo principal, el subtipo o el tipo de formato. \_No se prueba ningún miembro con valores NULL de GUID. (En efecto, GUID \_ ) NULL actúa como comodín). Los miembros con valores distintos \_ del GUID null deben coincidir para que el tipo de medio coincida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





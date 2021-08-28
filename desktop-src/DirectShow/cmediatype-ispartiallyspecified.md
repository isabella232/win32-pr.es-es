---
description: El método IsPartiallySpecified determina si el tipo de medio está parcialmente definido. Un tipo de medio es parcial si el tipo principal, subtipo o tipo de formato es GUID \_ NULL.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType.IsPartiallySpecified (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c2e7bdbbc43195222b4054f71ec05ebe3c8a7e15ac8c634d57fba61e45bf319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084475"
---
# <a name="cmediatypeispartiallyspecified-method"></a>CMediaType.IsPartiallySpecified (método)

El `IsPartiallySpecified` método determina si el tipo de medio está parcialmente definido. Un tipo de medio es *parcial si* el tipo principal, subtipo o tipo de formato es GUID \_ NULL.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el tipo de medio se especifica parcialmente. De lo contrario, **devuelve FALSE**.

## <a name="remarks"></a>Comentarios

El [**método IPin::Conectar**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) puede aceptar tipos de medios parciales.

La implementación no prueba realmente el subtipo. Si hay un tipo de formato especificado, el tipo de medio no se considera parcial, incluso si el subtipo es GUID \_ NULL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype.h (incluir Secuencias.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMediaType (clase)**](cmediatype.md)
</dt> </dl>

 

 





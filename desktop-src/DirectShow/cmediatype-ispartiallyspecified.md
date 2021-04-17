---
description: El método IsPartiallySpecified determina si el tipo de medio se define parcialmente. Un tipo de medio es parcial si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType. IsPartiallySpecified (mtype. h)
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
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680697"
---
# <a name="cmediatypeispartiallyspecified-method"></a>CMediaType. IsPartiallySpecified, método

El `IsPartiallySpecified` método determina si el tipo de medio se define parcialmente. Un tipo de medio es *parcial* si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el tipo de medio se especifica parcialmente. De lo contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

El método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) puede aceptar tipos de medios parciales.

La implementación no prueba realmente el subtipo. Si hay un tipo de formato especificado, el tipo de medio no se considera parcial, incluso si el subtipo es GUID \_ null.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Mtype. h (incluir streams. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMediaType**](cmediatype.md)
</dt> </dl>

 

 





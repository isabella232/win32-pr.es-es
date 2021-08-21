---
description: El método CheckMediaType determina si el filtro acepta un tipo de medio específico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Método CBaseRenderer.CheckMediaType (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8de57346138b4683f59cfa612f01fff1ef3d8fd9aceec9b34daee49bfa74ebbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157985"
---
# <a name="cbaserenderercheckmediatype-method"></a>Método CBaseRenderer.CheckMediaType

El `CheckMediaType` método determina si el filtro acepta un tipo de medio específico.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el tipo de medio propuesto es aceptable. De lo contrario, devuelve S \_ FALSE o un código de error.

## <a name="remarks"></a>Comentarios

El pin de entrada llama a este método desde su propio [**método CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md) La clase derivada debe implementar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





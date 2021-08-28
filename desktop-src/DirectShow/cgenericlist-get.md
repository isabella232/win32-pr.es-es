---
description: El método Get recupera el elemento en la posición especificada.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Método CGenericList.Get (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dae90872ea607571b215aafe3f9f35a645cd50d140dcbad0783369ce2189c881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813775"
---
# <a name="cgenericlistget-method"></a>CGenericList.Get (método)

El `Get` método recupera el elemento en la posición especificada.

## <a name="syntax"></a>Sintaxis


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pos* 
</dt> <dd>

Indicador de posición del elemento que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a un objeto de tipo **OBJECT** (el tipo de plantilla).

## <a name="remarks"></a>Comentarios

Si *pos* es **NULL,** el método devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxlist.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CGenericList (clase)**](cgenericlist.md)
</dt> </dl>

 

 





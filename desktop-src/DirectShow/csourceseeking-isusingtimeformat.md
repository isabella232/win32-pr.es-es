---
description: El método IsUsingTimeFormat determina si un formato de hora especificado es el formato actualmente en uso.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking.IsUsingTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361362"
---
# <a name="csourceseekingisusingtimeformat-method"></a>Método CSourceSeeking.IsUsingTimeFormat

El `IsUsingTimeFormat` método determina si un formato de hora especificado es el formato actualmente en uso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntero a un GUID de formato de hora. Consulte [**GUID de formato de hora**](time-format-guids.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El formato especificado no es el formato actual.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | El formato especificado es el formato actual.<br/>     |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL.<br/>                      |



 

## <a name="remarks"></a>Observaciones

El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





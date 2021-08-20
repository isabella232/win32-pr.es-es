---
description: Se llama al método SetMediaType cuando el tipo de medio se establece en uno de los pines del filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Método CTransformFilter.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc9331a532f6748de4e03c6972fdd555e4d5e11516d946bbd131da9acab364c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584945"
---
# <a name="ctransformfiltersetmediatype-method"></a>Método CTransformFilter.SetMediaType

Se `SetMediaType` llama al método cuando el tipo de medio se establece en uno de los pines del filtro.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*direction* 
</dt> <dd>

Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) DEL PIN, especificando un pin en el filtro (entrada o salida).

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los [**métodos CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) y [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) llaman a este método cuando se establece el tipo de medio de un pin. Este método no hace nada en la clase base, pero la clase derivada puede invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 





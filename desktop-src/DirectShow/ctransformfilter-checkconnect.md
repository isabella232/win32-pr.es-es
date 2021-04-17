---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660302"
---
# <a name="ctransformfiltercheckconnect-method"></a>CTransformFilter. CheckConnect, método

El `CheckConnect` método determina si una conexión de PIN es adecuada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dir* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica el PIN del filtro que realiza la conexión.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Los métodos [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) y [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) llaman a este método durante el proceso de conexión del PIN. Este método no hace nada en la clase base. La clase derivada puede invalidarla. Por ejemplo, la clase derivada podría consultar el otro PIN para una interfaz determinada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 





---
description: 'Método CTransformFilter.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Método CTransformFilter.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: a148e9edbc1cef42ecc2d1158dd18afcc908cf4d7549912b52f363aaa54cedb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953634"
---
# <a name="ctransformfiltercheckconnect-method"></a>Método CTransformFilter.CheckConnect

El `CheckConnect` método determina si una conexión de pin es adecuada.

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

Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) DEL PIN, especificando qué pin en el filtro está realizando la conexión.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los [**métodos CTransformInputPin::CheckConnect**](ctransforminputpin-checkconnect.md) y [**CTransformOutputPin::CheckConnect**](ctransformoutputpin-checkconnect.md) llaman a este método durante el proceso de conexión de pin. Este método no hace nada en la clase base. La clase derivada puede invalidarla. Por ejemplo, la clase derivada podría consultar el otro pin para una interfaz determinada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 





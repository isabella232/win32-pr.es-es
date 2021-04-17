---
description: La función GetInterface recupera un puntero de interfaz.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface (función) (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680767"
---
# <a name="getinterface-function"></a>GetInterface (función)

La `GetInterface` función recupera un puntero de interfaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntero a la interfaz **IUnknown** .

</dd> <dt>

*PPV* 
</dt> <dd>

Dirección de un puntero a la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro realiza un incremento seguro para subprocesos del recuento de referencias. Para recuperar la interfaz y agregar una referencia, llame a esta función desde su implementación de reemplazo del método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>ComBase. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funciones auxiliares de COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 





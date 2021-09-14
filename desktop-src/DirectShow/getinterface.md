---
description: La función GetInterface recupera un puntero de interfaz.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Función GetInterface (Combase.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061127"
---
# <a name="getinterface-function"></a>Función GetInterface

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

*Punk* 
</dt> <dd>

Puntero a **la interfaz IUnknown.**

</dd> <dt>

*Ppv* 
</dt> <dd>

Dirección de un puntero a la interfaz recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro realiza un incremento seguro para subprocesos del recuento de referencias. Para recuperar la interfaz y agregar una referencia, llame a esta función desde la implementación reemplazada del método **INonDelegatingUnknown::NonDelegatingQueryInterface.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones auxiliares COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 





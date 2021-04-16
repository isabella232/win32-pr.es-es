---
description: 'El método Block bloquea o desbloquea el flujo de datos desde el código PIN. Este método implementa el método IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Método CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b10e9dfd43f3ad98adf8f6abb0eb7c2223d5970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671759"
---
# <a name="cdynamicoutputpinblock-method"></a>CDynamicOutputPin. Block (método)

El `Block` método bloquea o desbloquea el flujo de datos desde el código PIN. Este método implementa el método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

Marca que indica si se debe bloquear o desbloquear el código PIN. Debe ser uno de los siguientes valores: 

Cero: Desbloquea el flujo de datos desde el código PIN.

\_ \_ \_ \_ Bloquear bloque de control de flujo: bloquear flujo de datos desde el código PIN.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador de un objeto de evento o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                                        | El PIN ya está desbloqueado.<br/>                     |
| <dl> <dt>**S \_ correcto**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argumento no válido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ PIN \_ ya \_ bloqueados**</dt> </dl>                   | El PIN ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**\_ \_ el PIN VFW \_ ya está \_ bloqueado \_ en \_ este \_ subproceso**</dt> </dl> | El PIN ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener más información sobre este método, vea [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Internamente, este método llama a uno de los métodos protegidos siguientes:

-   Bloquear (asincrónico): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Bloquear (sincrónico): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Desbloquear: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

El desbloqueo siempre se realiza sincrónicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 





---
description: El método Block bloquea o desbloquea el flujo de datos del pin. Este método implementa el método IPinFlowControl::Block.
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Método CDynamicOutputPin.Block (Amfilter.h)
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
ms.openlocfilehash: 6cc0a601ee1adbff9254baeff029c26d0cea359c7b2770b4d518bad916aca09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074289"
---
# <a name="cdynamicoutputpinblock-method"></a>Método CDynamicOutputPin.Block

El `Block` método bloquea o desbloquea el flujo de datos del pin. Este método implementa el [**método IPinFlowControl::Block.**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block)

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

Marca que indica si se va a bloquear o desbloquear el pin. Debe ser uno de los siguientes valores: 

Cero: desbloquee el flujo de datos del pin.

BLOQUE \_ DE CONTROL DE FLUJO DE PIN DE \_ \_ \_ AM: bloquee el flujo de datos del pin.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador de un objeto de evento o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                                                    | Descripción                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                                        | El pin ya está desbloqueado.<br/>                     |
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Correcto.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argumento no válido.<br/>                             |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA \_ ESTÁ \_ BLOQUEADO**</dt> </dl>                   | El pin ya está bloqueado en otro subproceso.<br/>     |
| <dl> <dt>**EL PIN \_ DE VFW E \_ YA ESTÁ BLOQUEADO EN ESTE \_ \_ \_ \_ \_ SUBPROCESO**</dt> </dl> | El pin ya está bloqueado en el subproceso que realiza la llamada.<br/> |



 

## <a name="remarks"></a>Comentarios

Para obtener más información sobre este método, vea [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Internamente, este método llama a uno de los métodos protegidos siguientes:

-   Bloquear (asincrónico): [ **CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Bloquear (sincrónico): [ **CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Desbloquear: [ **CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

El desbloqueo siempre se realiza de forma sincrónica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 





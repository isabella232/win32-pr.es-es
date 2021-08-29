---
description: El método Flushing notifica a la clase base que el pin se ha iniciado o detenido el vaciado.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Método CBaseStreamControl.Flushing (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da25983f26a89d5b264ec616e887d465f0851e3c901e2f1fac1dbab0c48be5bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103185"
---
# <a name="cbasestreamcontrolflushing-method"></a>CBaseStreamControl.Flushing (método)

El método notifica a la clase base que el pin se ha `Flushing` iniciado o detenido el vaciado.

## <a name="syntax"></a>Sintaxis


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bInProgress* 
</dt> <dd>

Especifica un valor booleano que indica si el pin se va a vaciar. Use el valor **TRUE cuando** el pin comienza una operación de vaciado y **FALSE** cuando finaliza una operación de vaciado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El pin debe llamar a este método desde sus [**métodos IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) [**e IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) Especifique **TRUE** en **BeginFlush** y **FALSE** en **EndFlush.**

Este método hace que [**el método CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) deje de esperar. Mientras se vacía el pin, **CheckStreamState** siempre devuelve STREAM \_ DISCARDING.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseStreamControl (clase)**](cbasestreamcontrol.md)
</dt> </dl>

 

 





---
description: El método de vaciado notifica a la clase base que el PIN se ha iniciado o detenido el vaciado.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: CBaseStreamControl. Flush (método) (Strmctl. h)
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
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671283"
---
# <a name="cbasestreamcontrolflushing-method"></a>CBaseStreamControl. Flush (método)

El `Flushing` método notifica a la clase base que el PIN se ha iniciado o detenido.

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

Especifica un valor booleano que indica si el PIN se está vaciando. Use el valor **true** cuando el PIN comienza una operación de vaciado y **false** cuando el PIN finaliza una operación de vaciado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El PIN debe llamar a este método desde sus métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) . Especifique **true** en **BeginFlush** y **false** en **EndFlush**.

Este método hace que el método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) deje de esperar. Mientras se está vaciando el PIN, **CheckStreamState** siempre devuelve el \_ descartado de la transmisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 





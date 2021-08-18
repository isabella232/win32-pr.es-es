---
description: El método BreakConnect libera el pin de entrada de una conexión.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer.BreakConnect (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cefaa91578f397a5ce967dc9cb6200acbe45f016e81f4552b9d185ad9ffa2609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044065"
---
# <a name="cbaserendererbreakconnect-method"></a>Método CBaseRenderer.BreakConnect

El `BreakConnect` método libera la clavija de entrada de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                         | Descripción                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>             | El pin no estaba conectado.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Correcto.<br/>                    |
| <dl> <dt>**VFW \_ E \_ NOT \_ STOPPED**</dt> </dl> | El filtro sigue activo.<br/> |



 

## <a name="remarks"></a>Comentarios

El pin de entrada del filtro llama a este método desde dentro de su propio `BreakConnect` método. (Para obtener más información, [**vea CBasePin::BreakConnect).**](cbasepin-breakconnect.md) El filtro realiza alguna contabilidad interna, como restablecer la marca de fin de flujo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Renbase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseRenderer (clase)**](cbaserenderer.md)
</dt> </dl>

 

 





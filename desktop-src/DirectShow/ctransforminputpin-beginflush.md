---
description: El método BeginFlush comienza una operación de vaciado. Este método implementa el método IPin::BeginFlush.
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Método CTransformInputPin.BeginFlush (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8199543491c27272cea96e994e9fc301c0ed53e2783fb2abff5677241c75dde4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053615"
---
# <a name="ctransforminputpinbeginflush-method"></a>Método CTransformInputPin.BeginFlush

El `BeginFlush` método comienza una operación de vaciado. Este método implementa el [**método IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin de salida no está conectado.<br/> |



 

## <a name="remarks"></a>Comentarios

Este método llama al método [**CBaseInputPin::BeginFlush del**](cbaseinputpin-beginflush.md) pin. A continuación, llama al método [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) del filtro para entregar la llamada de nivel inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 





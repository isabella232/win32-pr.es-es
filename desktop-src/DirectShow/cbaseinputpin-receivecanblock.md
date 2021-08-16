---
description: El método ReceiveCanBlock determina si las llamadas al método IMemInputPin::Receive pueden bloquearse. Este método implementa el método IMemInputPin::ReceiveCanBlock.
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Método CBaseInputPin.ReceiveCanBlock (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveCanBlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ece7243c145d34ed06e29b2a29ae9847e682981337b96a47976c20eb76272d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823857"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>Método CBaseInputPin.ReceiveCanBlock

El `ReceiveCanBlock` método determina si las llamadas al método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) pueden bloquearse. Este método implementa el [**método IMemInputPin::ReceiveCanBlock.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** El valor posible incluye los enumerados en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El pin no se bloqueará en una llamada a **Receive**.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | El pin podría bloquearse en una llamada a **Receive**.<br/>    |



 

## <a name="remarks"></a>Comentarios

Devuelve S FALSE si se garantiza que las llamadas al \_ **método Receive** no se bloqueen. De lo contrario, devuelva S \_ OK o un código de error. Si el **método Receive** llama a **Receive** en un pin de bajada, el pin de bajada podría bloquearse; `ReceiveCanBlock` debe tener en cuenta ese factor.

Un filtro ascendente puede usar este método para determinar su estrategia de subprocesos. Si el **método Receive** puede bloquearse, el filtro ascendente podría decidir usar un subproceso de trabajo que almacena en búfer los datos. Consulte la [**clase COutputQueue**](coutputqueue.md) para obtener una implementación de esta estrategia.

En la clase base, este método devuelve S OK cuando se cumple alguna \_ de las siguientes condiciones:

-   El filtro no tiene ningún pin de salida.
-   Un pin de entrada conectado a este filtro indica que podría bloquearse.
-   Un pin de entrada conectado a este filtro no admite la [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseInputPin (clase)**](cbaseinputpin.md)
</dt> </dl>

 

 





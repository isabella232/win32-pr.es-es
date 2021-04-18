---
description: 'El método ReceiveCanBlock determina si las llamadas al método IMemInputPin:: Receive podrían bloquearse. Este método implementa el método IMemInputPin:: ReceiveCanBlock.'
ms.assetid: db96e389-e1bc-4b38-8d0a-a20f0d3a4460
title: Método CBaseInputPin. ReceiveCanBlock (Amfilter. h)
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
ms.openlocfilehash: 93c80d6c8f834b45381b89e80d2e0acc392bf25a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661303"
---
# <a name="cbaseinputpinreceivecanblock-method"></a>CBaseInputPin. ReceiveCanBlock, método

El `ReceiveCanBlock` método determina si las llamadas al método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) podrían bloquearse. Este método implementa el método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveCanBlock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.



| Código devuelto                                                                             | Descripción                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | El PIN no se bloqueará en una llamada a **Receive**.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>    | El PIN podría bloquearse en una llamada a **Receive**.<br/>    |



 

## <a name="remarks"></a>Observaciones

Devuelve S \_ false si se garantiza que las llamadas al método **Receive** no se bloquean. De lo contrario, devuelve \_ un código de error o correcto. Si el método **Receive** llama a **Receive** en un PIN de nivel inferior, el PIN de bajada podría bloquearse; `ReceiveCanBlock` debe tener en cuenta este factor.

Un filtro de nivel superior puede utilizar este método para determinar su estrategia de subprocesos. Si el método **Receive** podría bloquearse, el filtro de nivel superior podría decidir usar un subproceso de trabajo que almacene en búfer los datos. Vea la clase [**COutputQueue**](coutputqueue.md) para obtener una implementación de esta estrategia.

En la clase base, este método devuelve S \_ OK cuando se cumple alguna de las siguientes condiciones:

-   El filtro no tiene clavijas de salida.
-   Un PIN de entrada conectado a este filtro indica que podría bloquearse.
-   Un PIN de entrada conectado a este filtro no admite la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 





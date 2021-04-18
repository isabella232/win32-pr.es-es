---
description: El método CompleteConnect completa una conexión de PIN.
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter. CompleteConnect (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdc9d1d5567cda2e4b0fd4a351136405493ef61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661260"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>CTransInPlaceFilter. CompleteConnect, método

El `CompleteConnect` método completa una conexión de PIN.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*direction* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica el PIN del filtro que realiza la conexión.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                             |
| <dl> <dt>**VFW \_ E \_ no \_ en el \_ gráfico**</dt> </dl> | El filtro no está en un gráfico de filtros.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) .

El comportamiento del filtro depende del orden de las conexiones del PIN:

-   Si el PIN de entrada se conecta primero, la conexión utiliza un asignador temporal. Cuando el PIN de salida está conectado, el filtro vuelve a conectar el PIN de entrada. Al volver a conectar el PIN de entrada, el filtro de nivel superior vuelve a negociar el asignador. En ese momento, el PIN de entrada propone un asignador del filtro de nivel inferior. Para obtener más información, vea [**CTransInPlaceInputPin:: GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Si el PIN de salida se conecta en primer lugar, el PIN de salida no selecciona ningún asignador. Cuando el PIN de entrada está conectado, negocia un asignador para ambas conexiones. Si los tipos de medios de entrada y salida no son los mismos, el filtro vuelve a conectar el PIN de salida con el tipo de entrada.

El filtro realiza todas las reconexiones de PIN llamando al método [**CBaseFilter:: ReconnectPin**](cbasefilter-reconnectpin.md) . A su vez, el método **ReconnectPin** llama al método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 





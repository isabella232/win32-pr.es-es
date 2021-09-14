---
description: 'Método CTransInPlaceFilter.CompleteConnect: el método CompleteConnect completa una conexión de pin.'
ms.assetid: 0c02c455-dbd0-4606-b1b1-f965c2a5805b
title: Método CTransInPlaceFilter.CompleteConnect (Transip.h)
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
ms.openlocfilehash: d9cc0bc839a4e35c4ce896acdf50da10f0c2bb0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255315"
---
# <a name="ctransinplacefiltercompleteconnect-method"></a>Método CTransInPlaceFilter.CompleteConnect

El `CompleteConnect` método completa una conexión de pin.

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

Miembro del tipo [**enumerado \_ DIRECCIÓN**](/windows/win32/api/strmif/ne-strmif-pin_direction) DEL PIN, especificando qué pin en el filtro está realizando la conexión.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **HRESULT**. Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                           | Descripción                                     |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                             |
| <dl> <dt>**VFW \_ E NO ESTÁ EN \_ \_ \_ GRAPH**</dt> </dl> | El filtro no está en un gráfico de filtros.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CTransformFilter::CompleteConnect.**](ctransformfilter-completeconnect.md)

El comportamiento del filtro depende del orden de las conexiones de pin:

-   Si el pin de entrada está conectado primero, la conexión usa un asignador temporal. Cuando el pin de salida está conectado, el filtro vuelve a conectar el pin de entrada. Volver a conectar el pin de entrada hace que el filtro ascendente vuelva a negociar el asignador. En ese momento, el pin de entrada propone un asignador del filtro de nivel inferior. Para obtener más información, [**vea CTransInPlaceInputPin::GetAllocator**](ctransinplaceinputpin-getallocator.md).
-   Si el pin de salida está conectado primero, el pin de salida no selecciona un asignador. Cuando el pin de entrada está conectado, negocia un asignador para ambas conexiones. Si los tipos de medios de entrada y salida no son los mismos, el filtro vuelve a conectar el pin de salida mediante el tipo de entrada.

El filtro realiza todas las reconexiones de anclar llamando al [**método CBaseFilter::ReconnectPin.**](cbasefilter-reconnectpin.md) A **su vez,** el método ReconnectPin llama al método [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) en el administrador de gráficos de filtros.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceFilter (clase)**](ctransinplacefilter.md)
</dt> </dl>

 

 





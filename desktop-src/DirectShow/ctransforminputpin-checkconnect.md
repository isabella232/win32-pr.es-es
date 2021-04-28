---
description: 'Método CTransformInputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Método CTransformInputPin.CheckConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e981254677c2e0a361a0a21f125f734ff1403db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095093"
---
# <a name="ctransforminputpincheckconnect-method"></a>Método CTransformInputPin.CheckConnect

El `CheckConnect` método determina si una conexión de pin es adecuada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                               | Descripción                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Correcto<br/>             |
| <dl> <dt>**DIRECCIÓN NO VÁLIDA DE VFW \_ E \_ \_**</dt> </dl> | Dirección de anclado incorrecta<br/> |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::CheckConnect.**](cbasepin-checkconnect.md) Llama al método [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve S \_ OK en la clase base. La clase derivada puede invalidar el **método CTransformFilter::CheckConnect** para realizar comprobaciones adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 





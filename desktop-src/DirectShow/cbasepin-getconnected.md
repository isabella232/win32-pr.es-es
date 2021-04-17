---
description: El método GetConnected recupera el PIN conectado a este pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Método CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660699"
---
# <a name="cbasepingetconnected-method"></a>CBasePin. GetConnected, método

El `GetConnected` método recupera el PIN conectado a este pin.

## <a name="syntax"></a>Sintaxis


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) de otro PIN.

## <a name="remarks"></a>Observaciones

Si el PIN no está conectado, este método devuelve **null**. Llame al método [**CBasePin:: IsConnected**](cbasepin-isconnected.md) para determinar si el PIN está conectado.

El método no llama a **AddRef** en la interfaz **IPin** , por lo que el llamador no debe liberar la interfaz.

## <a name="examples"></a>Ejemplos

Dado que el recuento de referencias no se incrementa en el puntero devuelto, puede encadenar las llamadas de método juntas:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Este modelo de codificación es muy práctico. pero como se muestra en el ejemplo, debe tener cuidado de no desreferenciar un puntero **nulo** cuando el PIN esté desconectado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 





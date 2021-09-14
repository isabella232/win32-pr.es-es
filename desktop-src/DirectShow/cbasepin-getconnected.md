---
description: El método GetConnected recupera el pin conectado a este pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Método CBasePin.GetConnected (Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246855"
---
# <a name="cbasepingetconnected-method"></a>Método CBasePin.GetConnected

El `GetConnected` método recupera el pin conectado a este pin.

## <a name="syntax"></a>Sintaxis


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.

## <a name="remarks"></a>Observaciones

Si el pin no está conectado, este método devuelve **NULL.** Llame al [**método CBasePin::IsConnected**](cbasepin-isconnected.md) para determinar si el pin está conectado.

El método no llama a **AddRef en** la **interfaz IPin,** por lo que el autor de la llamada no debe liberar la interfaz.

## <a name="examples"></a>Ejemplos

Dado que el recuento de referencias no se incrementa en el puntero devuelto, puede encadenar llamadas de método juntas:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Este patrón de codificación es muy conveniente; pero, como se muestra en el ejemplo, debe tener cuidado de no desreferenciar un puntero **NULL** cuando la marca no está conectada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 





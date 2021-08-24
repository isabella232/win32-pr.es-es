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
ms.openlocfilehash: 8bac5bc971f67c7678d2160cadb452995165638db4bb44d2ed1c89b3ab08f882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526845"
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

## <a name="remarks"></a>Comentarios

Si el pin no está conectado, este método devuelve **NULL.** Llame al [**método CBasePin::IsConnected**](cbasepin-isconnected.md) para determinar si el pin está conectado.

El método no llama a **AddRef en** la **interfaz IPin,** por lo que el autor de la llamada no debe liberar la interfaz.

## <a name="examples"></a>Ejemplos

Dado que el recuento de referencias no se incrementa en el puntero devuelto, puede encadenar llamadas a métodos:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Este patrón de codificación es muy práctico; pero, como se muestra en el ejemplo, debe tener cuidado de no desreferenciar un puntero **NULL** cuando la marca no está conectada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 





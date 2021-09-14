---
description: Se llama al método ChangeStart cuando cambia la posición inicial.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Método CSourceSeeking.ChangeStart (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973847"
---
# <a name="csourceseekingchangestart-method"></a>Método CSourceSeeking.ChangeStart

Se `ChangeStart` llama al método cuando cambia la posición inicial.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

El [**método CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) llama a este método si cambia la posición inicial. Este método es virtual puro; la clase derivada debe implementarla. Después de una operación de búsqueda, las marcas de tiempo deben reiniciarse desde cero. Las horas de los medios deben reflejar la nueva hora de inicio. En el ejemplo siguiente se muestra una posible implementación:


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





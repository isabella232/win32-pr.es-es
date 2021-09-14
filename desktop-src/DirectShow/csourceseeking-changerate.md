---
description: Se llama al método ChangeRate cuando cambia la velocidad de reproducción.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Método CSourceSeeking.ChangeRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973848"
---
# <a name="csourceseekingchangerate-method"></a>Método CSourceSeeking.ChangeRate

Se `ChangeRate` llama al método cuando cambia la velocidad de reproducción.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

El [**método CSourceSeeking::SetRate**](csourceseeking-setrate.md) llama a este método, que la clase derivada debe implementar. El **método SetRate** actualiza la variable miembro [**CSourceSeeking::m \_ dRateSeeking,**](csourceseeking-m-drateseeking.md) pero no valida el nuevo valor. Siempre se debe rechazar una tasa de cero. Las tasas inferiores a cero indican una reproducción negativa. La mayoría de los filtros no admiten tasas negativas.

En el ejemplo siguiente se muestra una posible implementación:


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
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

 

 





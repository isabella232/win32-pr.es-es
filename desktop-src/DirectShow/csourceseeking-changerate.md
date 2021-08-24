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
ms.openlocfilehash: ee74c8eb39fbebab1e58442c3b12f8342610ed792f4eb80ee70e5f44c3cca236
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633945"
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

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





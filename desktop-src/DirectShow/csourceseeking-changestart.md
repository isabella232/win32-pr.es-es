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
ms.openlocfilehash: 7f7c0d9a86d33d13c95295c5ef1ef46a3e6c02371d1b6520572750450320b1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073369"
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

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CSourceSeeking (clase)**](csourceseeking.md)
</dt> </dl>

 

 





---
description: Se llama al método ChangeStop cuando cambia la posición de detenerse.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Método CSourceSeeking.ChangeStop (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09473b5bbe20c6c31748f0079594424f7e0afa62e2594ff1cc80f33cb1f5e6bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103125"
---
# <a name="csourceseekingchangestop-method"></a>CSourceSeeking.ChangeStop (método)

Se `ChangeStop` llama al método cuando cambia la posición de detenerse.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

El [**método CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) llama a este método si cambia la posición de detenerse. Este método es virtual puro; la clase derivada debe implementarla. En el ejemplo siguiente se muestra una posible implementación:


```C++
HRESULT CMyStream::ChangeStop( )
{
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

 

 





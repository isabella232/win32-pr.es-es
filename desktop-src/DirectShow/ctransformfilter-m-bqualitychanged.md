---
description: Marca que indica si la calidad ha cambiado.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: CTransformFilter::m_bQualityChanged miembro (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246669"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Miembro CTransformFilter::m \_ bQualityChanged

Marca que indica si la calidad ha cambiado. La primera vez que el filtro quita un ejemplo, envía un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al administrador de gráficos de filtros y establece esta marca en **TRUE.** No envía este evento de nuevo hasta que el filtro se detiene y se reinicia, incluso si sigue colocando muestras mientras tanto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 





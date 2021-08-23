---
description: Marca que indica si la calidad ha cambiado.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: Miembro CTransformFilter::m_bQualityChanged (Transfrm.h)
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
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953614"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Miembro CTransformFilter::m \_ bQualityChanged

Marca que indica si la calidad ha cambiado. La primera vez que el filtro quita una muestra, envía un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al administrador de gráficos de filtros y establece esta marca en **TRUE.** No envía este evento de nuevo hasta que el filtro se detiene y se reinicia, aunque siga colocando muestras mientras tanto.

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

 

 





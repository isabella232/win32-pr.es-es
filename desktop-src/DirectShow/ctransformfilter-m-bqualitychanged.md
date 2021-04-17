---
description: Marca que indica si ha cambiado la calidad.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Miembro CTransformFilter:: m_bQualityChanged (Transfrm. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680827"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Miembro bQualityChanged CTransformFilter:: m \_

Marca que indica si ha cambiado la calidad. La primera vez que el filtro quita un ejemplo, envía un evento [**de \_ \_ cambio de calidad EC**](ec-quality-change.md) al administrador de gráficos de filtro y establece esta marca en **true**. No envía este evento de nuevo hasta que el filtro se detenga y se reinicie, incluso si continúa quitando muestras mientras tanto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 





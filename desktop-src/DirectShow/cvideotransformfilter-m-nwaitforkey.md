---
description: Número máximo actual de fotogramas Delta que se van a quitar.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Miembro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678944"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Miembro nWaitForKey CVideoTransformFilter:: m \_

Número máximo actual de fotogramas Delta que se van a quitar. Aunque esta variable es mayor que cero, el filtro quitará los fotogramas hasta que llegue a un fotograma clave. Para cada fotograma que se quita, el filtro reduce esta variable en uno, lo que impide que el filtro Quite un número excesivo de fotogramas. Después de 30 fotogramas Delta en una fila sin fotogramas clave, el filtro comenzará a entregar fotogramas de nuevo.

## <a name="syntax"></a>Sintaxis


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 





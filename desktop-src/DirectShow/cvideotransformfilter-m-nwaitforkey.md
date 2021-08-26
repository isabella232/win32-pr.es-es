---
description: Número máximo actual de fotogramas delta que se quitarán.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: CVideoTransformFilter::m_nWaitForKey miembro (Vtrans.h)
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
ms.openlocfilehash: 83cb78b233385e502d6508212492c54865aca28990ae079e4bf588776bd83fe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998545"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Miembro CVideoTransformFilter::m \_ nWaitForKey

Número máximo actual de fotogramas delta que se quitarán. Aunque esta variable es mayor que cero, el filtro quitará fotogramas hasta que llegue a un fotograma clave. Para cada fotograma que se quita, el filtro disminuye esta variable en uno, lo que impide que el filtro descime un número excesivo de fotogramas. Después de 30 fotogramas delta en una fila sin fotogramas clave, el filtro comenzará a entregar fotogramas de nuevo.

## <a name="syntax"></a>Sintaxis


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Vtrans.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 





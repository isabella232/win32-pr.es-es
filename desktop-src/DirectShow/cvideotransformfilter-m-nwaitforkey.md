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
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266479"
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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CVideoTransformFilter (clase)**](cvideotransformfilter.md)
</dt> </dl>

 

 




